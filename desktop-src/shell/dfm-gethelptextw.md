---
description: 'DFM_GETHELPTEXTW mensaje: permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda.'
title: DFM_GETHELPTEXTW mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097043"
---
# <a name="dfm_gethelptextw-message"></a>Mensaje \_ GETHELPTEXTW de DFM

Permite que el objeto de devolución de llamada especifique una cadena de texto de ayuda.


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*idCmd \_ cchMax* \[ en\]
</dt> <dd>

La palabra de orden bajo de este parámetro contiene el identificador del comando. La palabra de orden superior contiene el número de caracteres del *búfer pszText.*

</dd> <dt>

*pszText* \[ out\]
</dt> <dd>

Cadena Unicode terminada en NULL que contiene el texto de ayuda.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada en función de cómo se construya el objeto de menú contextual predeterminado. Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX es**](dfm-invokecommandex.md) una versión extendida de este mensaje y proporciona más información a la devolución de llamada. Use **DFM \_ INVOKECOMMANDEX si** la información adicional proporcionada por esa interfaz es necesaria en la implementación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DFM \_ GETHELPTEXTW** (Unicode)<br/>                                          |



 

 




