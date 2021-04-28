---
description: 'Evento InkPicture.Stroke: se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.'
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: Evento InkPicture.Stroke (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b181c8dc46348c76bd9c2d015d4a97c1f6911ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113703"
---
# <a name="inkpicturestroke-event"></a>Evento InkPicture.Stroke

Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.

## <a name="syntax"></a>Sintaxis


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento Stroke.**

</dd> <dt>

*Trazo* \[ En\]
</dt> <dd>

Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar la colección del trazo; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo distribución (dispinterfaces) de **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador DE DISPID \_ ICEStroke.

El **evento Stroke** tiene lugar cuando se está en modo de selección o borrado, no solo al insertar la entrada de lápiz. Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

> [!Note]  
> El **evento Stroke** tiene lugar cuando el usuario termina de dibujar un trazo, no cuando se agrega un trazo a la colección [InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Cuando el usuario empieza a dibujar por primera vez un trazo, se agrega inmediatamente a la colección InkStrokes; sin embargo, el **evento Stroke** no se produce hasta que se completa el trazo. Por lo tanto, pueden existir trazos en la colección InkStrokes que el **controlador de** eventos Stroke no ha visto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**StrokesAdded Event \[ InkPicture Control\]**](inkpicture-strokesadded.md)
</dt> <dt>

[**StrokesDeleted Event \[ InkPicture (Control InkPicture)\]**](inkpicture-strokesdeleted.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

