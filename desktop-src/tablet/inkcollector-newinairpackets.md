---
description: 'Evento InkCollector.NewInAirPackets: se produce cuando se ve un paquete en el aire.'
ms.assetid: e8eacdec-0381-435f-b453-24dca1c507c9
title: Evento InkCollector.NewInAirPackets (Msiguaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5709ae0b468aa6ab49516accf4037695268788
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110133"
---
# <a name="inkcollectornewinairpackets-event"></a><span data-ttu-id="4fbb9-103">Evento InkCollector.NewInAirPackets</span><span class="sxs-lookup"><span data-stu-id="4fbb9-103">InkCollector.NewInAirPackets event</span></span>

<span data-ttu-id="4fbb9-104">Se produce cuando se ve un paquete en el aire.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fbb9-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="4fbb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fbb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fbb9-107">*Cursor* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4fbb9-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb9-108">Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento NewInAirPackets.**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb9-109">*PacketCount* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4fbb9-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb9-110">Número de paquetes en aire recibidos.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="4fbb9-111">*PacketData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4fbb9-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb9-112">Cuando este método devuelve un resultado, contiene una matriz que contiene los datos seleccionados para el paquete.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-112">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="4fbb9-113">Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="4fbb9-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fbb9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fbb9-114">Return value</span></span>

<span data-ttu-id="4fbb9-115">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fbb9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fbb9-116">Remarks</span></span>

<span data-ttu-id="4fbb9-117">Se crea un paquete en el aire cuando un usuario mueve un lápiz cerca de la tableta y el cursor está dentro de la ventana del objeto del recopilador de entrada de lápiz o el usuario mueve un mouse dentro de la ventana asociada del objeto del recopilador de lápiz.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="4fbb9-118">**Los eventos NewInAirPackets** se generan rápidamente y el controlador de eventos debe ser rápido o el rendimiento sufra.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="4fbb9-119">Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE \_ DISPID ICENewInAirPackets.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="4fbb9-120">El **evento NewInAirPackets** se desencadena incluso cuando está en modo de selección o borrado, no solo al insertar entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="4fbb9-121">Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="4fbb9-122">La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="4fbb9-123">Para establecer qué propiedades están contenidas en esta matriz, use la [**propiedad DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) del objeto de recopilador de lápiz.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="4fbb9-124">La matriz que devuelve *el parámetro PacketData* contiene los datos de esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="4fbb9-125">Aunque puede modificar los datos del paquete, estas modificaciones no se conservan ni se usan.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4fbb9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fbb9-126">Requirements</span></span>



| <span data-ttu-id="4fbb9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fbb9-127">Requirement</span></span> | <span data-ttu-id="4fbb9-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4fbb9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbb9-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fbb9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4fbb9-130">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="4fbb9-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4fbb9-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fbb9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4fbb9-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4fbb9-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4fbb9-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fbb9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fbb9-134"><dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb9-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4fbb9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fbb9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fbb9-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb9-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4fbb9-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4fbb9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fbb9-138">**InkCollector (clase)**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="4fbb9-139">**Propiedad DesiredPacketDescription**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="4fbb9-140">**Evento NewPackets**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="4fbb9-141">**IInkCursor (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




