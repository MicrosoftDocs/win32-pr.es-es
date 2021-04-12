---
title: Mensaje de WM_CAP_GET_USER_DATA (VFW. h)
description: El \_ mensaje de datos del usuario Cap get de WM \_ \_ \_ recupera un \_ valor de datos PTR largo asociado a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- Mensaje de WM_CAP_GET_USER_DATA de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535020"
---
# <a name="wm_cap_get_user_data-message"></a>\_Mensaje de \_ datos de usuario de obtención de Cap de \_ WM \_

El mensaje de **\_ \_ datos del \_ usuario \_ Cap get de WM** recupera un valor de datos **\_ ptr largo** asociado a una ventana de captura. Puede enviar este mensaje explícitamente o mediante la macro [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor devuelto

Devuelve un valor previamente guardado mediante el mensaje [**de \_ \_ datos del \_ usuario \_ del conjunto de límites de WM**](wm-cap-set-user-data.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





