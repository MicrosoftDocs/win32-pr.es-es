---
title: NM_CUSTOMDRAW de notificación (vista de lista) (Commctrl.h)
description: Enviado por un control de vista de lista para notificar a sus ventanas primarias sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- NM_CUSTOMDRAW (vista de lista) de código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30af8dc61f9bb12d524f2b3f6ac58fb1adecebf66b4ad4477756e17f9a621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018882"
---
# <a name="nm_customdraw-list-view-notification-code"></a>Código \_ de notificación DE NM CUSTOMDRAW (vista de lista)

Enviado por un control de vista de lista para notificar a sus ventanas primarias sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) que contiene información sobre la operación de dibujo. El primer miembro de esta estructura, **nmcd**, es un puntero a una [**estructura NMCUSTOMDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) El **miembro dwItemSpec** de la estructura a la que **apunta nmcd** contiene el identificador del elemento que se está dibujando y el miembro **lItemlParam** contiene sus datos definidos por la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor que puede devolver la aplicación depende de la fase de dibujo actual. El **miembro dwDrawStage** de la estructura [**NMCUSTOMDRAW asociada**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) contiene un valor que especifica la fase de dibujo. Debe devolver uno de los siguientes valores.



| Código devuelto                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | El control se dibujará a sí mismo. No enviará ningún código de notificación [DE NM \_ CUSTOMDRAW](nm-customdraw.md) adicional para este ciclo de pintura. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ DOERASE**</dt> </dl>           | Windows Vista. El control solo pintará el fondo. <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | El control notificará al elemento primario las operaciones de dibujo relacionadas con elementos. Enviará códigos de [notificación NM \_ CUSTOMDRAW](nm-customdraw.md) antes y después de dibujar elementos. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | El control notificará al elemento primario después de borrar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | El control notificará al elemento primario después de pintar un elemento. Esto sucede cuando **dwDrawStage** es igual a PREPAINT de \_ CDDS.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | La aplicación especificó una nueva fuente para el elemento; el control usará la nueva fuente. Para obtener más información sobre cómo cambiar las fuentes, vea [Cambio de fuentes y colores.](custom-draw.md) Esto sucede cuando **dwDrawStage** es igual a \_ ITEMPREPAINT de CDDS.<br/>                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versión 4.71.](common-control-versions.md) La aplicación recibirá un código de control [NM \_ CUSTOMDRAW](nm-customdraw.md) con **dwDrawStage** establecido en CDDS \_ ITEMPREPAINT CDDS SUBITEM antes de dibujar cada subelemento de vista \| \_ de lista. A continuación, puede especificar la fuente y el color de cada subelemento por separado o devolver [**CDRF \_ DODEFAULT**](cdrf-constants.md) para el procesamiento predeterminado. Esto sucede cuando **dwDrawStage** es igual a \_ ITEMPREPAINT de CDDS.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | La aplicación ha dibujado el elemento manualmente. El control no dibujará el elemento. Esto sucede cuando **dwDrawStage** es igual a \_ ITEMPREPAINT de CDDS.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | Windows Vista. El control no dibujará el rectángulo de foco. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentarios

[Versión 5.80.](common-control-versions.md) Si cambia la fuente devolviendo [**CDRF \_ NEWFONT,**](cdrf-constants.md)el control de vista de lista podría mostrar texto recortado. Este comportamiento es necesario para la compatibilidad con versiones anteriores de los controles comunes. Si desea cambiar la fuente de un control de vista de lista, se obtienen mejores resultados si envía un mensaje [**\_ SETVERSION**](ccm-setversion.md) de CCM con el valor *wParam* establecido en 5 antes de agregar cualquier elemento al control.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





