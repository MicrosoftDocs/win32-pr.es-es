---
description: Se produce cuando se reconoce un gesto específico de la aplicación.
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: InkCollector. gesto evento (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb68add1a3fbba5781624f1df98c3a637745b95a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705553"
---
# <a name="inkcollectorgesture-event"></a><span data-ttu-id="8bc03-103">InkCollector. gesto (evento)</span><span class="sxs-lookup"><span data-stu-id="8bc03-103">InkCollector.Gesture event</span></span>

<span data-ttu-id="8bc03-104">Se produce cuando se reconoce un gesto específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bc03-104">Occurs when an application-specific gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bc03-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="8bc03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bc03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bc03-107">*Cursor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8bc03-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc03-108">El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="8bc03-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="8bc03-109">*Trazos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8bc03-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc03-110">La colección [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que el reconocedor devolvió como el gesto.</span><span class="sxs-lookup"><span data-stu-id="8bc03-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="8bc03-111">*Gestos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8bc03-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc03-112">Matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , en orden de confianza, del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="8bc03-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="8bc03-113">Para obtener más información sobre la estructura de variante, vea [usar la biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="8bc03-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bc03-114">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8bc03-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc03-115">**Variante \_ TRUE** si se debe cancelar este gesto; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="8bc03-115">**VARIANT\_TRUE** if this gesture should be cancelled; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bc03-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bc03-116">Return value</span></span>

<span data-ttu-id="8bc03-117">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="8bc03-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bc03-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bc03-118">Remarks</span></span>

<span data-ttu-id="8bc03-119">Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICEGesture.</span><span class="sxs-lookup"><span data-stu-id="8bc03-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="8bc03-120">Cuando la propiedad [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) se establece en [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), el tiempo de espera entre el momento en que un usuario agrega un gesto y el momento en que se produce el evento de **gesto** es un valor fijo que no se puede modificar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="8bc03-120">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="8bc03-121">El reconocimiento de gestos es más rápido en el modo **InkAndGesture** .</span><span class="sxs-lookup"><span data-stu-id="8bc03-121">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="8bc03-122">Para evitar la recopilación de entradas manuscritas en modo [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="8bc03-122">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="8bc03-123">Establezca [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) en [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="8bc03-123">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="8bc03-124">Elimine el trazo en el evento [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="8bc03-124">Delete the stroke in the [**Stroke**](inkcollector-stroke.md) event.</span></span>
-   <span data-ttu-id="8bc03-125">Procesa el gesto en el evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="8bc03-125">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="8bc03-126">Para evitar el flujo de tinta mientras se gesturing, establezca la propiedad [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) en **false**.</span><span class="sxs-lookup"><span data-stu-id="8bc03-126">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="8bc03-127">Además de cuando se inserta la entrada de lápiz, el evento de **gesto** se desencadena cuando se está en modo de selección o de borrado.</span><span class="sxs-lookup"><span data-stu-id="8bc03-127">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="8bc03-128">Usted es responsable de realizar el seguimiento del modo de edición y debe tener en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="8bc03-128">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="8bc03-129">Para reconocer gestos, debe usar un objeto o un control que pueda recopilar entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="8bc03-129">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="8bc03-130">Los gestos de aplicación se definen como gestos que se admiten en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bc03-130">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="8bc03-131">Para que se produzca este evento, el objeto o el control deben tener interés en un conjunto de gestos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bc03-131">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="8bc03-132">Para establecer el interés de los objetos o controles en un conjunto de gestos, llame al método [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) del objeto o control.</span><span class="sxs-lookup"><span data-stu-id="8bc03-132">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="8bc03-133">Para obtener una lista de gestos de aplicación específicos, vea el tipo de enumeración [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="8bc03-133">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bc03-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bc03-134">Requirements</span></span>



| <span data-ttu-id="8bc03-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bc03-135">Requirement</span></span> | <span data-ttu-id="8bc03-136">Value</span><span class="sxs-lookup"><span data-stu-id="8bc03-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bc03-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bc03-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8bc03-138">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8bc03-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8bc03-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bc03-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8bc03-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8bc03-140">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8bc03-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bc03-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bc03-142"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8bc03-142"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8bc03-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bc03-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bc03-144"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bc03-144"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8bc03-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bc03-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc03-146">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="8bc03-146">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="8bc03-147">**Enumeración InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="8bc03-147">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="8bc03-148">**Método SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="8bc03-148">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="8bc03-149">Usar gestos</span><span class="sxs-lookup"><span data-stu-id="8bc03-149">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

