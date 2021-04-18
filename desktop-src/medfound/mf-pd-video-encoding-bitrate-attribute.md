---
description: Especifica la velocidad de bits de codificación de vídeo de la presentación, en bits por segundo. Este atributo se aplica a los descriptores de presentación.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: MF_PD_VIDEO_ENCODING_BITRATE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707237"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>MF \_ PD \_ \_ atributo de velocidad de bits de codificación de vídeo \_

Especifica la velocidad de bits de codificación de vídeo de la presentación, en bits por segundo. Este atributo se aplica a los descriptores de presentación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Algunos formatos tienen esquemas de codificación más complejos que no se pueden resumir mediante este atributo. En el caso de los archivos de formato de sistema avanzado (ASF), los atributos siguientes describen colectivamente la velocidad de bits de codificación:

-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ de \_ velocidad de bits máxima**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**\_velocidad de \_ \_ \_ bits promedio de \_ datos \_ ASF SD EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**\_velocidad de \_ \_ bits de \_ datos Max SD ASF EXTSTRMPROP máx \_ \_ .**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**\_velocidad de \_ bits de ASF SD ASF \_ STREAMBITRATES \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)

Los formatos de terceros pueden usar otros atributos personalizados.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




