---
description: Se usa para definir mensajes privados para su uso por parte de clases de ventana privadas, normalmente con el formato WM \_ User + x, donde x es un valor entero.
ms.assetid: 4115c587-fcb4-4170-9948-fe33bcb8742a
title: WM_USER (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1efd6f2e79180b7dc627281829539d20f5fa74d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082087"
---
# <a name="wm_user"></a><span data-ttu-id="eee1c-103">usuario de WM \_</span><span class="sxs-lookup"><span data-stu-id="eee1c-103">WM\_USER</span></span>

<span data-ttu-id="eee1c-104">Se usa para definir mensajes privados para su uso por parte de clases de ventana privadas, normalmente con el formato **WM \_ User** + *x*, donde *x* es un valor entero.</span><span class="sxs-lookup"><span data-stu-id="eee1c-104">Used to define private messages for use by private window classes, usually of the form **WM\_USER**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                         0x0400
```

## <a name="remarks"></a><span data-ttu-id="eee1c-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eee1c-105">Remarks</span></span>

<span data-ttu-id="eee1c-106">A continuación se muestran los intervalos de números de mensaje.</span><span class="sxs-lookup"><span data-stu-id="eee1c-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="eee1c-107">Intervalo</span><span class="sxs-lookup"><span data-stu-id="eee1c-107">Range</span></span>                                                        | <span data-ttu-id="eee1c-108">Significado</span><span class="sxs-lookup"><span data-stu-id="eee1c-108">Meaning</span></span>                                                        |
|--------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="eee1c-109">de 0 a **WM \_ usuario** – 1</span><span class="sxs-lookup"><span data-stu-id="eee1c-109">0 through **WM\_USER** –1</span></span><br/>                         | <span data-ttu-id="eee1c-110">Mensajes reservados para su uso por el sistema.</span><span class="sxs-lookup"><span data-stu-id="eee1c-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="eee1c-111">**WM \_ USUARIO** a través de 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="eee1c-111">**WM\_USER** through 0x7FFF</span></span><br/>                       | <span data-ttu-id="eee1c-112">Mensajes enteros para su uso por las clases de ventana privadas.</span><span class="sxs-lookup"><span data-stu-id="eee1c-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="eee1c-113">[**WM \_ APLICACIÓN**](wm-app.md) (0x8000) a través de 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="eee1c-113">[**WM\_APP**](wm-app.md) (0x8000) through 0xBFFF</span></span><br/> | <span data-ttu-id="eee1c-114">Mensajes disponibles para que las usen las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="eee1c-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="eee1c-115">0xC000 a 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="eee1c-115">0xC000 through 0xFFFF</span></span><br/>                             | <span data-ttu-id="eee1c-116">Mensajes de cadena para su uso por parte de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="eee1c-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="eee1c-117">Mayor que 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="eee1c-117">Greater than 0xFFFF</span></span><br/>                               | <span data-ttu-id="eee1c-118">Reservado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="eee1c-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="eee1c-119">El sistema define los números de mensaje en el primer intervalo (del 0 al **\_ usuario de WM** -1).</span><span class="sxs-lookup"><span data-stu-id="eee1c-119">Message numbers in the first range (0 through **WM\_USER** –1) are defined by the system.</span></span> <span data-ttu-id="eee1c-120">El sistema reserva los valores de este intervalo que no se definen explícitamente.</span><span class="sxs-lookup"><span data-stu-id="eee1c-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="eee1c-121">Los números de mensajes del segundo intervalo **( \_ usuario de WM** a través de 0x7FFF) se pueden definir y usar en una aplicación para enviar mensajes dentro de una clase de ventana privada.</span><span class="sxs-lookup"><span data-stu-id="eee1c-121">Message numbers in the second range (**WM\_USER** through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="eee1c-122">Estos valores no se pueden usar para definir mensajes que sean significativos en una aplicación porque algunas clases de ventana predefinidas ya definen valores en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="eee1c-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="eee1c-123">Por ejemplo, las clases de control predefinidas como **Button**, **Edit**, **ListBox** y **ComboBox** pueden utilizar estos valores.</span><span class="sxs-lookup"><span data-stu-id="eee1c-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="eee1c-124">Los mensajes de este intervalo no se deben enviar a otras aplicaciones a menos que las aplicaciones se hayan diseñado para intercambiar mensajes y adjuntar el mismo significado a los números de mensaje.</span><span class="sxs-lookup"><span data-stu-id="eee1c-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="eee1c-125">Los números de mensaje en el tercer intervalo (de 0x8000 a 0xBFFF) están disponibles para que las aplicaciones lo usen como mensajes privados.</span><span class="sxs-lookup"><span data-stu-id="eee1c-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="eee1c-126">Los mensajes de este intervalo no entran en conflicto con los mensajes del sistema.</span><span class="sxs-lookup"><span data-stu-id="eee1c-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="eee1c-127">Los números de mensaje del cuarto intervalo (de 0xC000 a 0xFFFF) se definen en tiempo de ejecución cuando una aplicación llama a la función [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar un número de mensaje para una cadena.</span><span class="sxs-lookup"><span data-stu-id="eee1c-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="eee1c-128">Todas las aplicaciones que registran la misma cadena pueden usar el número de mensaje asociado para intercambiar mensajes.</span><span class="sxs-lookup"><span data-stu-id="eee1c-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="eee1c-129">Sin embargo, el número de mensaje real no es una constante y no se puede suponer que sea el mismo entre distintas sesiones.</span><span class="sxs-lookup"><span data-stu-id="eee1c-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="eee1c-130">El sistema reserva los números de mensaje del quinto intervalo (mayor que 0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="eee1c-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="eee1c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eee1c-131">Requirements</span></span>



| <span data-ttu-id="eee1c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="eee1c-132">Requirement</span></span> | <span data-ttu-id="eee1c-133">Value</span><span class="sxs-lookup"><span data-stu-id="eee1c-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee1c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eee1c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eee1c-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eee1c-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eee1c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eee1c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eee1c-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eee1c-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eee1c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eee1c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee1c-139"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eee1c-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eee1c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="eee1c-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="eee1c-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="eee1c-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eee1c-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="eee1c-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="eee1c-143">**aplicación de WM \_**</span><span class="sxs-lookup"><span data-stu-id="eee1c-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="eee1c-144">**Vista**</span><span class="sxs-lookup"><span data-stu-id="eee1c-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eee1c-145">Mensajes y colas de mensajes</span><span class="sxs-lookup"><span data-stu-id="eee1c-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 
