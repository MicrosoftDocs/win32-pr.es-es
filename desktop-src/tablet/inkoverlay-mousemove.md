---
description: Se produce cuando el puntero del mouse se mueve sobre el objeto InkCollector o InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Evento InkOverlay. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ddefd5f3b3f75b03488f74bdbd4aee222a89d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278856"
---
# <a name="inkoverlaymousemove-event"></a>Evento InkOverlay. MouseMove

Se produce cuando el puntero del mouse se mueve sobre el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Sintaxis


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Botón* \[ de de\]
</dt> <dd>

Botón del mouse que se presionó.

</dd> <dt>

*Desplazamiento* \[ de\]
</dt> <dd>

Estado de la tecla Mayús.

</dd> <dt>

*PX* \[ de\]
</dt> <dd>

Coordenada x, en píxeles, de un clic del mouse.

</dd> <dt>

*py* \[ de\]
</dt> <dd>

Coordenada y, en píxeles, de un clic del mouse.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Indica si se debe cancelar el evento para el control primario. El valor predeterminado es **false**, que especifica que no se debe cancelar el evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Las propiedades *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no tiene en cuenta el lápiz y este tipo de aplicación solo entiende píxeles.

 

> [!Note]  
> Algunos controles dependen de una relación específica entre los eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)y [**MouseUp**](inkcollector-mouseup.md) . La cancelación de algunos de estos eventos puede tener resultados imprevistos.

 

Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEMouseMove.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Enumeración InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeración InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




