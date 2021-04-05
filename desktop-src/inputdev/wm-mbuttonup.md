---
title: Mensaje de WM_MBUTTONUP (Winuser. h)
description: Se envía cuando el usuario suelta el botón central del mouse mientras el cursor está en el área de cliente de una ventana.
ms.assetid: fb8dee71-11bd-4405-855d-a5d120442271
keywords:
- Entrada de mouse y teclado de mensaje de WM_MBUTTONUP
topic_type:
- apiref
api_name:
- WM_MBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce7eb6b84c227934b5351a27ff8884fa78946ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079233"
---
# <a name="wm_mbuttonup-message"></a><span data-ttu-id="00666-104">Mensaje de MBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="00666-104">WM\_MBUTTONUP message</span></span>

<span data-ttu-id="00666-105">Se envía cuando el usuario suelta el botón central del mouse mientras el cursor está en el área de cliente de una ventana.</span><span class="sxs-lookup"><span data-stu-id="00666-105">Posted when the user releases the middle mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="00666-106">Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor.</span><span class="sxs-lookup"><span data-stu-id="00666-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="00666-107">De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.</span><span class="sxs-lookup"><span data-stu-id="00666-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="00666-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="00666-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MBUTTONUP                    0x0208
```



## <a name="parameters"></a><span data-ttu-id="00666-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00666-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00666-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00666-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00666-111">Indica si varias claves virtuales están inactivas.</span><span class="sxs-lookup"><span data-stu-id="00666-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="00666-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="00666-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="00666-113">Value</span><span class="sxs-lookup"><span data-stu-id="00666-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="00666-114">Significado</span><span class="sxs-lookup"><span data-stu-id="00666-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="00666-115"><dt>**MK \_**</dt> <dt>0X0008</dt> de control</span><span class="sxs-lookup"><span data-stu-id="00666-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="00666-116">La tecla CTRL está presionada.</span><span class="sxs-lookup"><span data-stu-id="00666-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="00666-117"><dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="00666-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="00666-118">El botón primario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="00666-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="00666-119"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="00666-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="00666-120">El botón central del mouse está presionado.</span><span class="sxs-lookup"><span data-stu-id="00666-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="00666-121"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="00666-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="00666-122">El botón secundario del mouse está inactivo.</span><span class="sxs-lookup"><span data-stu-id="00666-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="00666-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="00666-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="00666-124">La tecla Mayús está presionada.</span><span class="sxs-lookup"><span data-stu-id="00666-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="00666-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="00666-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="00666-126">El primer botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="00666-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="00666-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="00666-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="00666-128">El segundo botón X está inactivo.</span><span class="sxs-lookup"><span data-stu-id="00666-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="00666-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00666-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00666-130">La palabra de orden inferior especifica la coordenada x del cursor.</span><span class="sxs-lookup"><span data-stu-id="00666-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="00666-131">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="00666-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="00666-132">La palabra de orden superior especifica la coordenada y del cursor.</span><span class="sxs-lookup"><span data-stu-id="00666-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="00666-133">La coordenada es relativa a la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="00666-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="00666-134">Tenga en cuenta que cuando un menú contextual está presente (se muestra), las coordenadas son relativas a la pantalla, no al área cliente.</span><span class="sxs-lookup"><span data-stu-id="00666-134">Note that when a shortcut menu is present (displayed), coordinates are relative to the screen, not the client area.</span></span> <span data-ttu-id="00666-135">Dado que [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) es una llamada asincrónica y la notificación de **\_ MBUTTONUP de WM** no tiene una marca especial que indica la derivación de coordenadas, una aplicación no puede saber si las coordenadas x, y contenidas en *lParam* son relativas a la pantalla o al área cliente.</span><span class="sxs-lookup"><span data-stu-id="00666-135">Because [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) is an asynchronous call and the **WM\_MBUTTONUP** notification does not have a special flag indicating coordinate derivation, an application cannot tell if the x,y coordinates contained in *lParam* are relative to the screen or the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00666-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00666-136">Return value</span></span>

<span data-ttu-id="00666-137">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="00666-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="00666-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00666-138">Remarks</span></span>

<span data-ttu-id="00666-139">Use el código siguiente para obtener la posición horizontal y vertical:</span><span class="sxs-lookup"><span data-stu-id="00666-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="00666-140">Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores).</span><span class="sxs-lookup"><span data-stu-id="00666-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="00666-141">Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="00666-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="00666-142">También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.</span><span class="sxs-lookup"><span data-stu-id="00666-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00666-143">No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="00666-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="00666-144">Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.</span><span class="sxs-lookup"><span data-stu-id="00666-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00666-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00666-145">Requirements</span></span>



| <span data-ttu-id="00666-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="00666-146">Requirement</span></span> | <span data-ttu-id="00666-147">Value</span><span class="sxs-lookup"><span data-stu-id="00666-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00666-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00666-148">Minimum supported client</span></span><br/> | <span data-ttu-id="00666-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="00666-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="00666-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00666-150">Minimum supported server</span></span><br/> | <span data-ttu-id="00666-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00666-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="00666-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00666-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="00666-153"><dt>Winuser. h (incluir windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00666-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00666-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="00666-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="00666-155">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="00666-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="00666-156">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="00666-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="00666-157">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="00666-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="00666-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="00666-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="00666-159">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="00666-159">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="00666-160">**MBUTTONDBLCLK de WM \_**</span><span class="sxs-lookup"><span data-stu-id="00666-160">**WM\_MBUTTONDBLCLK**</span></span>](wm-mbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="00666-161">**MBUTTONDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="00666-161">**WM\_MBUTTONDOWN**</span></span>](wm-mbuttondown.md)
</dt> <dt>

<span data-ttu-id="00666-162">**Vista**</span><span class="sxs-lookup"><span data-stu-id="00666-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="00666-163">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="00666-163">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="00666-164">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="00666-164">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="00666-165">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="00666-165">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="00666-166">[**CIMA**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="00666-166">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

