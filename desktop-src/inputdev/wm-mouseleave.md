---
title: Mensaje de WM_MOUSELEAVE (Winuser. h)
description: Se envía a una ventana cuando el cursor abandona el área cliente de la ventana especificada en una llamada anterior a TrackMouseEvent.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- Entrada de mouse y teclado de mensaje de WM_MOUSELEAVE
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490036"
---
# <a name="wm_mouseleave-message"></a><span data-ttu-id="bc049-104">Mensaje de WM \_ MOUSELEAVE</span><span class="sxs-lookup"><span data-stu-id="bc049-104">WM\_MOUSELEAVE message</span></span>

<span data-ttu-id="bc049-105">Se envía a una ventana cuando el cursor abandona el área cliente de la ventana especificada en una llamada anterior a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="bc049-105">Posted to a window when the cursor leaves the client area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="bc049-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bc049-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a><span data-ttu-id="bc049-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc049-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc049-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc049-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc049-109">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bc049-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bc049-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc049-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc049-111">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bc049-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc049-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc049-112">Return value</span></span>

<span data-ttu-id="bc049-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="bc049-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc049-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc049-114">Remarks</span></span>

<span data-ttu-id="bc049-115">Todo el seguimiento solicitado por [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) se cancela cuando se genera este mensaje.</span><span class="sxs-lookup"><span data-stu-id="bc049-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="bc049-116">La aplicación debe llamar a **TrackMouseEvent** cuando el mouse vuelva a entrar en su ventana si requiere un seguimiento adicional del comportamiento de desplazamiento del mouse.</span><span class="sxs-lookup"><span data-stu-id="bc049-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc049-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc049-117">Requirements</span></span>



| <span data-ttu-id="bc049-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc049-118">Requirement</span></span> | <span data-ttu-id="bc049-119">Value</span><span class="sxs-lookup"><span data-stu-id="bc049-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc049-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc049-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bc049-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc049-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bc049-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc049-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bc049-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc049-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc049-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc049-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc049-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc049-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc049-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc049-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc049-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="bc049-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc049-128">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="bc049-128">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="bc049-129">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="bc049-129">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="bc049-130">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="bc049-130">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="bc049-131">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="bc049-131">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="bc049-132">**NCMOUSELEAVE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="bc049-132">**WM\_NCMOUSELEAVE**</span></span>](wm-ncmouseleave.md)
</dt> <dt>

<span data-ttu-id="bc049-133">**Vista**</span><span class="sxs-lookup"><span data-stu-id="bc049-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc049-134">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="bc049-134">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

