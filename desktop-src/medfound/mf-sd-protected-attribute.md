---
description: Indica si una secuencia contiene contenido protegido.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: MF_SD_PROTECTED atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae6cf92b3ada6309de7e92a722db38c88ce94a8af88aa6cc0176f738ff194b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474062"
---
# <a name="mf_sd_protected-attribute"></a>Atributo MF \_ SD \_ PROTECTED

Indica si una secuencia contiene contenido protegido.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de flujo. Si el valor del atributo es **TRUE,** la secuencia contiene contenido protegido. Si el valor es **FALSE** o el atributo no está establecido, la secuencia contiene contenido sin formato.

En lugar de comprobar cada secuencia para este atributo, puede pasar un descriptor de presentación a la [**función MFRequireProtectedEnvironment.**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) Esta función comprueba si el descriptor de presentación contiene secuencias protegidas.

Un origen de medios debe establecer este atributo en el descriptor de secuencia si el contenido requiere la ruta de acceso multimedia protegida (PMP).

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="examples"></a>Ejemplos


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos de descriptor de flujo](stream-descriptor-attributes.md)
</dt> </dl>

 

 




