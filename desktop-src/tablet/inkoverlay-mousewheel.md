---
description: 'Evento InkOverlay.MouseWheel: se produce cuando la rueda del mouse se mueve mientras el objeto InkCollector o InkOverlay tiene el foco.'
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: Evento InkOverlay.MouseWheel (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468dbdac09fd40144768e8342791d5712a570bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116893"
---
# <a name="inkoverlaymousewheel-event"></a><span data-ttu-id="9f643-103">Evento InkOverlay.MouseWheel</span><span class="sxs-lookup"><span data-stu-id="9f643-103">InkOverlay.MouseWheel event</span></span>

<span data-ttu-id="9f643-104">Se produce cuando la rueda del mouse se mueve mientras el [**objeto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="9f643-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f643-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f643-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="9f643-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f643-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f643-107">*Botón* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9f643-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f643-108">Botón del mouse que se presionó.</span><span class="sxs-lookup"><span data-stu-id="9f643-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="9f643-109">*Mayús* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9f643-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f643-110">Estado de la tecla MAYÚS.</span><span class="sxs-lookup"><span data-stu-id="9f643-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="9f643-111">*Delta* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9f643-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f643-112">Recuento con firma del número de detents que ha girado la rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="9f643-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="9f643-113">Un paso es una muesca de la rueda del mouse.</span><span class="sxs-lookup"><span data-stu-id="9f643-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="9f643-114">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9f643-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f643-115">Coordenada x, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="9f643-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="9f643-116">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9f643-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f643-117">Coordenada y, en píxeles, de un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="9f643-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="9f643-118">*Cancelar* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9f643-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f643-119">Si el evento se debe cancelar para el control primario.</span><span class="sxs-lookup"><span data-stu-id="9f643-119">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="9f643-120">El valor predeterminado es **FALSE,** que especifica que no se debe cancelar el evento.</span><span class="sxs-lookup"><span data-stu-id="9f643-120">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f643-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f643-121">Return value</span></span>

<span data-ttu-id="9f643-122">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="9f643-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f643-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f643-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f643-124">Las propiedades *pX* y *pY* están en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="9f643-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="9f643-125">Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.</span><span class="sxs-lookup"><span data-stu-id="9f643-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="9f643-126">Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="9f643-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f643-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f643-127">Requirements</span></span>



| <span data-ttu-id="9f643-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f643-128">Requirement</span></span> | <span data-ttu-id="9f643-129">Valor</span><span class="sxs-lookup"><span data-stu-id="9f643-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f643-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f643-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9f643-131">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9f643-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9f643-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f643-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9f643-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9f643-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9f643-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f643-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f643-135"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9f643-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9f643-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f643-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f643-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f643-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9f643-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f643-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f643-139">**InkOverlay (clase)**</span><span class="sxs-lookup"><span data-stu-id="9f643-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="9f643-140">**InkMouseButton (enumeración)**</span><span class="sxs-lookup"><span data-stu-id="9f643-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="9f643-141">**InkShiftKeyModifierFlags (Enumeración)**</span><span class="sxs-lookup"><span data-stu-id="9f643-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




