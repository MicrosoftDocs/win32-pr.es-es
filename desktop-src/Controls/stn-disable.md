---
title: Código de notificación de STN_DISABLE (Winuser. h)
description: '\_Se envía el código de notificación de deshabilitación de STN cuando se deshabilita un control estático.'
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- STN_DISABLE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2763fce96b043ec6aebf5339a9f93d6fdf4a8abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149982"
---
# <a name="stn_disable-notification-code"></a>STN \_ deshabilitar código de notificación

\_Se envía el código de notificación de deshabilitación de STN cuando se deshabilita un control estático. El control estático debe tener el estilo [**SS \_ Notify**](static-control-styles.md) para recibir este código de notificación. La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
STN_DISABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control estático. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control estático.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[\_habilitación de STN](stn-enable.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Controles estáticos](static-controls.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

