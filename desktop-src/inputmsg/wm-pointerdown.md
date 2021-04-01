---
title: Mensaje WM_POINTERDOWN
description: Se envía cuando un puntero hace contacto sobre el área de cliente de una ventana.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8ac000
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERDOWN
topic_type:
- apiref
api_name:
- WM_POINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 051e7f0aa08305e4c38d7eefec94483fd11f3bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150678"
---
# <a name="wm_pointerdown-message"></a><span data-ttu-id="1c674-104">Mensaje WM_POINTERDOWN</span><span class="sxs-lookup"><span data-stu-id="1c674-104">WM_POINTERDOWN message</span></span>

<span data-ttu-id="1c674-105">Se envía cuando un puntero hace contacto sobre el área de cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="1c674-105">Posted when a pointer makes contact over the client area of a window.</span></span> <span data-ttu-id="1c674-106">Este mensaje de entrada se dirige a la ventana en la que el puntero hace contacto y el puntero se captura implícitamente en la ventana para que la ventana siga recibiendo entradas para el puntero hasta que se interrumpa el contacto.</span><span class="sxs-lookup"><span data-stu-id="1c674-106">This input message targets the window over which the pointer makes contact, and the pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="1c674-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1c674-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="1c674-108">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="1c674-108">\[!Important\]</span></span>  
> <span data-ttu-id="1c674-109">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="1c674-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="1c674-110">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="1c674-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="1c674-111">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="1c674-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="1c674-112">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1c674-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDOWN                   0x0246
```



## <a name="parameters"></a><span data-ttu-id="1c674-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c674-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c674-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c674-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c674-115">Contiene información sobre el puntero.</span><span class="sxs-lookup"><span data-stu-id="1c674-115">Contains information about the pointer.</span></span> <span data-ttu-id="1c674-116">Use las siguientes macros para recuperar información del parámetro wParam.</span><span class="sxs-lookup"><span data-stu-id="1c674-116">Use the following macros to retrieve information from the wParam parameter.</span></span>

-   <span data-ttu-id="1c674-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): el identificador de puntero.</span><span class="sxs-lookup"><span data-stu-id="1c674-117">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): the pointer identifier.</span></span>
-   <span data-ttu-id="1c674-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje representa la primera entrada generada por un nuevo puntero.</span><span class="sxs-lookup"><span data-stu-id="1c674-118">[**IS_POINTER_NEW_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message represents the first input generated by a new pointer.</span></span>
-   <span data-ttu-id="1c674-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje fue generado por un puntero durante su duración.</span><span class="sxs-lookup"><span data-stu-id="1c674-119">[**IS_POINTER_INRANGE_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer during its lifetime.</span></span> <span data-ttu-id="1c674-120">Esta marca no se establece en mensajes que indican que el puntero tiene el intervalo de detección izquierdo</span><span class="sxs-lookup"><span data-stu-id="1c674-120">This flag is not set on messages that indicate that the pointer has left detection range</span></span>
-   <span data-ttu-id="1c674-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si este mensaje fue generado por un puntero que está en contacto con la superficie de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1c674-121">[**IS_POINTER_INCONTACT_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether this message was generated by a pointer that is in contact with the window surface.</span></span> <span data-ttu-id="1c674-122">Esta marca no se establece en los mensajes que indican un puntero de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="1c674-122">This flag is not set on messages that indicate a hovering pointer.</span></span>
-   <span data-ttu-id="1c674-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indica que este puntero se ha designado como principal.</span><span class="sxs-lookup"><span data-stu-id="1c674-123">[**IS_POINTER_PRIMARY_WPARAM**](/previous-versions/windows/desktop/api)(wParam): indicates that this pointer has been designated as primary.</span></span>
-   <span data-ttu-id="1c674-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción principal.</span><span class="sxs-lookup"><span data-stu-id="1c674-124">[**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a primary action.</span></span>
    -   <span data-ttu-id="1c674-125">Es análogo a un botón primario del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="1c674-125">This is analogous to a mouse left button down.</span></span>
    -   <span data-ttu-id="1c674-126">Un puntero táctil tendrá este conjunto cuando esté en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="1c674-126">A touch pointer will have this set when it is in contact with the digitizer surface.</span></span>
    -   <span data-ttu-id="1c674-127">Un puntero de pluma tendrá este conjunto cuando esté en contacto con la superficie del digitalizador sin presionar ningún botón.</span><span class="sxs-lookup"><span data-stu-id="1c674-127">A pen pointer will have this set when it is in contact with the digitizer surface with no buttons pressed.</span></span>
-   <span data-ttu-id="1c674-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una acción secundaria.</span><span class="sxs-lookup"><span data-stu-id="1c674-128">[**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there is a secondary action.</span></span>
    -   <span data-ttu-id="1c674-129">Es análogo a un botón secundario del mouse hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="1c674-129">This is analogous to a mouse right button down.</span></span>
    -   <span data-ttu-id="1c674-130">Un puntero de pluma tendrá este conjunto cuando esté en contacto con la superficie del digitalizador con el botón de barril del lápiz presionado.</span><span class="sxs-lookup"><span data-stu-id="1c674-130">A pen pointer will have this set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>
-   <span data-ttu-id="1c674-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si hay una o varias acciones terciarias basadas en el tipo de puntero; las aplicaciones que desean responder a las acciones terciarias deben recuperar información específica del tipo de puntero para determinar qué botones terciarios se presionan.</span><span class="sxs-lookup"><span data-stu-id="1c674-131">[**IS_POINTER_THIRDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether there are one or more tertiary actions based on the pointer type; applications that wish to respond to tertiary actions must retrieve information specific to the pointer type to determine which tertiary buttons are pressed.</span></span> <span data-ttu-id="1c674-132">Por ejemplo, una aplicación puede determinar los Estados de los botones de un lápiz mediante una llamada a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y el examen de las marcas que especifican los Estados de los botones.</span><span class="sxs-lookup"><span data-stu-id="1c674-132">For example, an application can determine the buttons states of a pen by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>
-   <span data-ttu-id="1c674-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): marca que indica si el puntero especificado tardó la cuarta acción.</span><span class="sxs-lookup"><span data-stu-id="1c674-133">[**IS_POINTER_FOURTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a flag that indicates whether the specified pointer took fourth action.</span></span> <span data-ttu-id="1c674-134">Las aplicaciones que deseen responder a las cuarta acciones deben recuperar información específica del tipo de puntero para determinar si se presiona el botón del primer Mouse extendido (XButton1).</span><span class="sxs-lookup"><span data-stu-id="1c674-134">Applications that wish to respond to fourth actions must retrieve information specific to the pointer type to determine if the first extended mouse (XButton1) button is pressed.</span></span>
-   <span data-ttu-id="1c674-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): [**marca**](pointer-flags-contants.md) que indica si el puntero especificado tardó la quinta acción.</span><span class="sxs-lookup"><span data-stu-id="1c674-135">[**IS_POINTER_FIFTHBUTTON_WPARAM**](/previous-versions/windows/desktop/api)(wParam): a [**flag**](pointer-flags-contants.md) that indicates whether the specified pointer took fifth action.</span></span> <span data-ttu-id="1c674-136">Las aplicaciones que deseen responder a las Quinta acciones deben recuperar información específica del tipo de puntero para determinar si se presiona el botón secundario del mouse (XButton2).</span><span class="sxs-lookup"><span data-stu-id="1c674-136">Applications that wish to respond to fifth actions must retrieve information specific to the pointer type to determine if the second extended mouse (XButton2) button is pressed.</span></span>

    <span data-ttu-id="1c674-137">Consulte [**marcadores de puntero**](pointer-flags-contants.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="1c674-137">See [**Pointer Flags**](pointer-flags-contants.md) for more details.</span></span>

    > [!Note]  
    > <span data-ttu-id="1c674-138">Un puntero que mantiene el mouse no tiene ninguna de las marcas de botón establecidas.</span><span class="sxs-lookup"><span data-stu-id="1c674-138">A hovering pointer has none of the button flags set.</span></span> <span data-ttu-id="1c674-139">Esto es análogo a un movimiento del mouse sin presionar los botones del mouse.</span><span class="sxs-lookup"><span data-stu-id="1c674-139">This is analogous to a mouse move with no mouse buttons down.</span></span> <span data-ttu-id="1c674-140">Una aplicación puede determinar los Estados de los botones de un lápiz que mantiene el mouse, por ejemplo, llamando a [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) y examinando las marcas que especifican los Estados de los botones.</span><span class="sxs-lookup"><span data-stu-id="1c674-140">An application can determine the buttons states of a hovering pen, for example, by calling [**GetPointerPenInfo**](/previous-versions/windows/desktop/api) and examining the flags that specify button states.</span></span>

     

</dd> <dt>

<span data-ttu-id="1c674-141">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c674-141">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c674-142">Contiene la ubicación del punto del puntero.</span><span class="sxs-lookup"><span data-stu-id="1c674-142">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="1c674-143">Dado que el puntero puede establecer contacto con el dispositivo a través de un área no trivial, esta ubicación de punto puede ser una simplificación de un área de puntero más compleja.</span><span class="sxs-lookup"><span data-stu-id="1c674-143">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="1c674-144">Siempre que sea posible, una aplicación debe usar la información de área de puntero completa en lugar de la ubicación del punto.</span><span class="sxs-lookup"><span data-stu-id="1c674-144">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="1c674-145">Utilice las siguientes macros para recuperar las coordenadas físicas de la pantalla del punto.</span><span class="sxs-lookup"><span data-stu-id="1c674-145">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="1c674-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): la coordenada X (punto horizontal).</span><span class="sxs-lookup"><span data-stu-id="1c674-146">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="1c674-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): la coordenada Y (punto vertical).</span><span class="sxs-lookup"><span data-stu-id="1c674-147">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c674-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c674-148">Return value</span></span>

<span data-ttu-id="1c674-149">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="1c674-149">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="1c674-150">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="1c674-150">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c674-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c674-151">Remarks</span></span>

> <span data-ttu-id="1c674-152">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="1c674-152">\[!Important\]</span></span>  
> <span data-ttu-id="1c674-153">Cuando una ventana pierde la captura de un puntero y recibe la notificación [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , normalmente no recibirá ninguna notificación adicional.</span><span class="sxs-lookup"><span data-stu-id="1c674-153">When a window loses capture of a pointer and it receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it typically will not receive any further notifications.</span></span> <span data-ttu-id="1c674-154">Por esta razón, es importante que no realice suposiciones basadas en WM_POINTERUP de WM_POINTERDOWN emparejadas uniformemente  / [](wm-pointerup.md) o [**WM_POINTERENTER**](wm-pointerenter.md) / notificaciones [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="1c674-154">For this reason, it is important that you not make any assumptions based on evenly paired **WM_POINTERDOWN**/[**WM_POINTERUP**](wm-pointerup.md) or [**WM_POINTERENTER**](wm-pointerenter.md)/[**WM_POINTERLEAVE**](wm-pointerleave.md) notifications.</span></span>

 

<span data-ttu-id="1c674-155">Cada puntero tiene un identificador de puntero único durante su duración.</span><span class="sxs-lookup"><span data-stu-id="1c674-155">Each pointer has a unique pointer identifier during its lifetime.</span></span> <span data-ttu-id="1c674-156">La duración de un puntero comienza cuando se detecta por primera vez.</span><span class="sxs-lookup"><span data-stu-id="1c674-156">The lifetime of a pointer begins when it is first detected.</span></span>

<span data-ttu-id="1c674-157">Si se detecta un puntero de desplazamiento, se genera un mensaje de [**WM_POINTERENTER**](wm-pointerenter.md) .</span><span class="sxs-lookup"><span data-stu-id="1c674-157">A [**WM_POINTERENTER**](wm-pointerenter.md) message is generated if a hovering pointer is detected.</span></span> <span data-ttu-id="1c674-158">Se genera un mensaje de **WM_POINTERDOWN** seguido de un mensaje de **WM_POINTERENTER** si se detecta un puntero que no tiene el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="1c674-158">A **WM_POINTERDOWN** message followed by a **WM_POINTERENTER** message is generated if a non-hovering pointer is detected.</span></span>

<span data-ttu-id="1c674-159">Durante su duración, un puntero puede generar una serie de mensajes de [**WM_POINTERUPDATE**](wm-pointerupdate.md) mientras se mantiene el mouse o el contacto.</span><span class="sxs-lookup"><span data-stu-id="1c674-159">During its lifetime, a pointer may generate a series of [**WM_POINTERUPDATE**](wm-pointerupdate.md) messages while it is hovering or in contact.</span></span>

<span data-ttu-id="1c674-160">La duración de un puntero finaliza cuando ya no se detecta.</span><span class="sxs-lookup"><span data-stu-id="1c674-160">The lifetime of a pointer ends when it is no longer detected.</span></span> <span data-ttu-id="1c674-161">Esto genera un mensaje de [**WM_POINTERLEAVE**](wm-pointerleave.md) .</span><span class="sxs-lookup"><span data-stu-id="1c674-161">This generates a [**WM_POINTERLEAVE**](wm-pointerleave.md) message.</span></span>

<span data-ttu-id="1c674-162">Cuando se anula un puntero, se establece [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) .</span><span class="sxs-lookup"><span data-stu-id="1c674-162">When a pointer is aborted, [**POINTER_FLAG_CANCELED**](pointer-flags-contants.md) is set.</span></span>

<span data-ttu-id="1c674-163">También se puede generar un mensaje [**WM_POINTERLEAVE**](wm-pointerleave.md) cuando un puntero no capturado se mueve fuera de los límites de una ventana.</span><span class="sxs-lookup"><span data-stu-id="1c674-163">A [**WM_POINTERLEAVE**](wm-pointerleave.md) message may also be generated when a non-captured pointer moves outside the bounds of a window.</span></span>

<span data-ttu-id="1c674-164">Para obtener la posición horizontal y vertical de un puntero, use lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1c674-164">To obtain the horizontal and vertical position of a pointer, use the following:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="1c674-165">Para convertir el parámetro lParam en una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) , use la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) .</span><span class="sxs-lookup"><span data-stu-id="1c674-165">To convert the lParam parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure, use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro.</span></span>

<span data-ttu-id="1c674-166">Para recuperar más información asociada con el mensaje, utilice la función [**GetPointerInfo**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="1c674-166">To retrieve further information associated with the message, use the [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span>

<span data-ttu-id="1c674-167">Para determinar los Estados clave del modificador de teclado asociados a este mensaje, utilice la función [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) .</span><span class="sxs-lookup"><span data-stu-id="1c674-167">To determine the keyboard modifier key states associated with this message, use the [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) function.</span></span> <span data-ttu-id="1c674-168">Por ejemplo, para detectar que se presionó la tecla ALT, compruebe si GetKeyState (VK_MENU) &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="1c674-168">For example, to detect that the ALT key was pressed, check whether GetKeyState(VK_MENU) &lt; 0.</span></span>

<span data-ttu-id="1c674-169">Tenga en cuenta que si la aplicación no procesa este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o varios mensajes [**WM_GESTURE**](../wintouch/wm-gesture.md) si la secuencia de entrada de este y, posiblemente, otros punteros se reconocen como un gesto.</span><span class="sxs-lookup"><span data-stu-id="1c674-169">Note that if the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages if the sequence of input from this and, possibly, other pointers is recognized as a gesture.</span></span> <span data-ttu-id="1c674-170">Si no se reconoce un gesto, **DefWindowProc** puede generar la entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="1c674-170">If a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="1c674-171">Si una aplicación usa selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.</span><span class="sxs-lookup"><span data-stu-id="1c674-171">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

<span data-ttu-id="1c674-172">Cuando una ventana pierde la captura de un puntero y recibe la notificación [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) , normalmente no recibirá más notificaciones.</span><span class="sxs-lookup"><span data-stu-id="1c674-172">When a window loses capture of a pointer and receives the [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) notification, it will typically not receive any further notifications.</span></span> <span data-ttu-id="1c674-173">Por lo tanto, es importante que una ventana no haga ninguna suposición de su estado de puntero, con independencia de si recibe notificaciones de entrada o salida con pareja uniforme.</span><span class="sxs-lookup"><span data-stu-id="1c674-173">Therefore, it is important that a window does not make any assumptions of its pointer status, regardless of whether it receives evenly paired DOWN / UP or ENTER / LEAVE notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="1c674-174">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1c674-174">Examples</span></span>

<span data-ttu-id="1c674-175">En el ejemplo de código siguiente se muestra cómo usar [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)y [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)para recuperar la información pertinente asociada al mensaje **WM_POINTERDOWN** .</span><span class="sxs-lookup"><span data-stu-id="1c674-175">The following code example shows how to use [**IS_POINTER_FIRSTBUTTON_WPARAM**](/previous-versions/windows/desktop/api), [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam), [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam), and [**IS_POINTER_SECONDBUTTON_WPARAM**](/previous-versions/windows/desktop/api)to retrieve the relevant information associated with the **WM_POINTERDOWN** message.</span></span>


```
int xPos = GET_X_LPARAM(lParam);
int yPos = GET_Y_LPARAM(lParam);

if (IS_POINTER_PRIMARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse left button down
}
else if (IS_POINTER_SECONDARYBUTTON_WPARAM(wParam))
{
    // process pointer down, similar to mouse right button down
}
```



<span data-ttu-id="1c674-176">En el ejemplo de código siguiente se muestra cómo usar [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para recuperar el identificador de puntero del mensaje de **WM_POINTERDOWN** .</span><span class="sxs-lookup"><span data-stu-id="1c674-176">The following code example shows how to use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to retrieve the pointer id from the **WM_POINTERDOWN** message.</span></span>


```
POINTER_INFO pointerInfo;
UINT32       pointerId = GET_POINTERID_WPARAM(wParam);

// Retrieve common pointer information
if (!GetPointerInfo(pointerId, &amp;pointerInfo))
{
    // failure, call GetLastError()
}
else
{
    // success, process pointerInfo
}
```



<span data-ttu-id="1c674-177">En el ejemplo de código siguiente se muestra cómo administrar distintos tipos de puntero, como dispositivos táctiles, de lápiz o de punteros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="1c674-177">The following code example shows how to handle different pointer type such as touch, pen, or default pointing devices.</span></span>


```
POINTER_TOUCH_INFO   touchInfo;
POINTER_PEN_INFO     penInfo;
POINTER_INFO         pointerInfo;
UINT32               pointerId = GET_POINTERID_WPARAM(wParam);
POINTER_TYPE         pointerType = PT_POINTER;

// default to unhandled to enable call to DefWindowProc
fHandled = FALSE;

if (!GetPointerType(pointerId, &amp;pointerType))
{
    // failure, call GetLastError()
    // set PT_POINTER to fall to default case below
    pointerType = PT_POINTER;
}

switch (pointerType)
{
case PT_TOUCH:
    // Retrieve touch information
    if (!GetPointerTouchInfo(pointerId, &amp;touchInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process touchInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
case PT_PEN:
    // Retrieve pen information
    if (!GetPointerPenInfo(pointerId, &amp;penInfo))
    {
        // failure, call GetLastError()
    }
    else
    {
        // success, process penInfo
        // mark as handled to skip call to DefWindowProc
        fHandled = TRUE;
    }
    break;
default:
    if (!GetPointerInfo(pointerId, &amp;pointerInfo)) 
    {
        // failure.
    } 
    else 
    {
        // success, proceed with pointerInfo.
        fHandled = HandleGenericPointerMessage(&amp;pointerInfo);
    }
    break;
}

```



## <a name="requirements"></a><span data-ttu-id="1c674-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c674-178">Requirements</span></span>



| <span data-ttu-id="1c674-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c674-179">Requirement</span></span> | <span data-ttu-id="1c674-180">Value</span><span class="sxs-lookup"><span data-stu-id="1c674-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c674-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c674-181">Minimum supported client</span></span><br/> | <span data-ttu-id="1c674-182">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c674-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="1c674-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c674-183">Minimum supported server</span></span><br/> | <span data-ttu-id="1c674-184">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c674-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1c674-185">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c674-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c674-186"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c674-186"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c674-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c674-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c674-188">Mensajes</span><span class="sxs-lookup"><span data-stu-id="1c674-188">Messages</span></span>](messages.md)
</dt> <dt>

<span data-ttu-id="1c674-189">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1c674-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1c674-190">**Marcas de puntero**</span><span class="sxs-lookup"><span data-stu-id="1c674-190">**Pointer Flags**</span></span>](pointer-flags-contants.md)
</dt> <dt>

[<span data-ttu-id="1c674-191">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-191">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-192">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-192">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-193">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-193">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-194">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-194">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-195">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-195">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-196">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-197">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-198">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-199">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="1c674-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="1c674-200">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

