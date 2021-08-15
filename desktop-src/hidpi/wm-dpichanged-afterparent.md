---
title: WM_DPICHANGED_AFTERPARENT mensaje (Winuser.h)
description: Para las ventanas de nivel superior por monitor v2, este mensaje se envía a todos los HWND del árbol HWDN secundario de la ventana que está experimentando un cambio de PPP. | WM_DPICHANGED_AFTERPARENT mensaje (Winuser.h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT mensaje Valores altos de PPP
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d47f303db19438f1e7e2cd77df60ddace76bec791bb1789bed47e3f09d8a197c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759368"
---
# <a name="wm_dpichanged_afterparent-message"></a>Mensaje \_ AFTERPARENT DE WM PPPCHANGED \_

Para las ventanas de nivel superior por monitor [v2,](dpi-awareness-context.md) este mensaje se envía a todos los HWND del árbol HWDN secundario de la ventana que está experimentando un cambio de PPP. Este mensaje se produce después de que la ventana de nivel superior recibe [**WM \_ PPPCHANGED**](wm-dpichanged.md)y recorre el árbol secundario desde arriba hacia abajo.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este valor no se usa y será cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este valor no se usa y será cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El sistema no usa y omite este valor.

## <a name="remarks"></a>Comentarios

No hay ningún control predeterminado de este mensaje en [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Este mensaje solo se envía cuando la ventana de nivel superior tiene un contexto de reconocimiento de PPP de PMv2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**WM \_ PPPCHANGED**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ PPPCHANGED \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

