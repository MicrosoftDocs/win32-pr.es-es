---
title: CDN_INITDONE de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando el sistema ha terminado de organizar los controles del cuadro de diálogo. El sistema mueve los controles estándar para hacer espacio para los controles del cuadro de diálogo secundario.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- CDN_INITDONE de diálogo de código de notificación
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6594c161d57a5d0772679477ee9bce2cda28ba12
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549840"
---
# <a name="cdn_initdone-notification-code"></a>Código de notificación \_ INITDONE de CDN

\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md). Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]

Enviado por un cuadro de **diálogo** Abrir o Guardar **como** de estilo explorador cuando el sistema ha terminado de organizar los controles del cuadro de diálogo. El sistema mueve los controles estándar para hacer espacio para los controles del cuadro de diálogo secundario.

El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación \_ INITDONE de CDN.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**

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

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

