---
description: Se produce cuando se reconoce un gesto del sistema.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.Sysevento temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717071"
---
# <a name="inkpicturesystemgesture-event"></a>InkPicture.Sysevento temGesture

Se produce cuando se reconoce un gesto del sistema.

## <a name="syntax"></a>Sintaxis


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ de de\]
</dt> <dd>

El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **SystemGesture** .

</dd> <dt>

*ID.* \[ en\]
</dt> <dd>

Valor del gesto del sistema.

</dd> <dt>

*X* \[ en\]
</dt> <dd>

Coordenada x de la ubicación del gesto.

</dd> <dt>

*Y* \[ en\]
</dt> <dd>

Coordenada y de la ubicación del gesto.

</dd> <dt>

*Modificador* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*Carácter* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*CursorMode* \[ de\]
</dt> <dd>

Valor que indica si el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está en modo normal o en modo de borrador. 1 es para el modo normal y 2 para el modo de borrador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Los gestos del sistema proporcionan información sobre el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que se usa para crear el gesto. También proporcionan accesos directos a combinaciones de eventos del mouse y son maneras de detectar eventos del mouse con menos impacto en el rendimiento.

Por ejemplo, en lugar de buscar un par de eventos de evento [**MouseUp del \[ control \] InkPicture**](inkpicture-mouseup.md)Event InkPicture / [**\[ \] control**](inkpicture-mousedown.md) de eventos sin que se produzcan otros eventos del mouse en Between, puede buscar los gestos del sistema TAP o RightTap.

Otro ejemplo, en lugar de realizar escuchas de eventos [**MouseDown \[ \]**](inkpicture-mousedown.md)del control InkPicture del evento / [**MouseMove \[ \]**](inkpicture-mousemove.md) en el control InkPicture y obtener numerosos mensajes del **\[ \] control InkPicture del evento MouseMove** , puede ver los gestos del sistema de arrastrar o RightDrag siempre y cuando no esté interesado en las coordenadas (x, y) de cada posición del mouse. Esto le permite recibir un solo mensaje en lugar de numerosos mensajes del **\[ \] control InkPicture del evento MouseMove** .

Para obtener una lista de gestos específicos del sistema, vea el tipo de enumeración [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Para obtener más información acerca de los gestos del sistema, consulte [uso de gestos](using-gestures.md) y [entradas de comandos en Tablet PC](/previous-versions//dd314533(v=vs.85)).

Este método de evento se define en las interfaces de solo distribución (dispinterfaces) **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** con el identificador DISPID \_ ICESystemGesture.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Enumeración InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[Usar gestos](using-gestures.md)
</dt> </dl>

 

