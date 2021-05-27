---
title: CDN_SELCHANGE de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando cambia la selección en el cuadro de lista que muestra el contenido de la carpeta o directorio abierto actualmente.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE cuadros de diálogo de código de notificación
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c21aa9dda117c74707b3c890ad96e017b45bcc0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549230"
---
# <a name="cdn_selchange-notification-code"></a>Código de notificación \_ SELCHANGE de CDN

\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el Cuadro [de diálogo de elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]

Enviado por un  cuadro de diálogo Abrir o Guardar **como** de estilo explorador cuando cambia la selección en el cuadro de lista que muestra el contenido de la carpeta o directorio abierto actualmente.

El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación \_ SELCHANGE de CDN.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**

Para obtener el nombre del archivo o carpeta recién seleccionados, el procedimiento de enlace puede enviar el mensaje [**\_ GETFILEPATH**](cdm-getfilepath.md) o [**\_ CDM GETSPEC**](cdm-getspec.md) de CDM al cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluye Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GETFILEPATH de CDM \_**](cdm-getfilepath.md)
</dt> <dt>

[**GETSPEC de CDM \_**](cdm-getspec.md)
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

