---
title: CDM_GETFOLDERIDLIST mensaje (Commdlg.h)
description: Recupera la dirección de la lista de identificadores de elemento correspondiente a la carpeta que un cuadro de diálogo Abrir o Guardar como del estilo explorador tiene abierto actualmente.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST cuadro de diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3ffff4f80dc21ed685e589ed4780b43592c2d2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549710"
---
# <a name="cdm_getfolderidlist-message"></a>Mensaje \_ GETFOLDERIDLIST de CDM

\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]

Recupera la dirección de la lista de identificadores de  elemento correspondiente a la carpeta que un cuadro de diálogo Abrir o Guardar **como** del estilo explorador tiene abierto actualmente. El cuadro de diálogo debe haber sido creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tamaño, en bytes, del búfer *lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al búfer que recibe la lista de identificadores de elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el tamaño, en bytes, de la lista de identificadores de elemento. Este es el número de bytes copiados en el búfer o el tamaño de búfer necesario si el búfer es demasiado pequeño.

Si se produce un error, el valor devuelto es menor que cero.

## <a name="remarks"></a>Comentarios

La macro correspondiente es la siguiente:

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

