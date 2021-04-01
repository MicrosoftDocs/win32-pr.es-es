---
title: Mensaje de LVM_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetUnicodeFormat de ListView.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- LVM_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720a65baab8ec9c1ec3b311e49fe3672c97a0fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905502"
---
# <a name="lvm_getunicodeformat-message"></a><span data-ttu-id="fe968-105">\_Mensaje GETUNICODEFORMAT LVM</span><span class="sxs-lookup"><span data-stu-id="fe968-105">LVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="fe968-106">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="fe968-106">Retrieves the UNICODE character format flag for the control.</span></span> <span data-ttu-id="fe968-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetUnicodeFormat de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="fe968-107">You can send this message explicitly or use the [**ListView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe968-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe968-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe968-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe968-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe968-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fe968-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fe968-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe968-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fe968-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fe968-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe968-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe968-113">Return value</span></span>

<span data-ttu-id="fe968-114">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="fe968-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="fe968-115">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="fe968-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="fe968-116">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="fe968-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe968-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe968-117">Remarks</span></span>

<span data-ttu-id="fe968-118">Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="fe968-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe968-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe968-119">Requirements</span></span>



| <span data-ttu-id="fe968-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe968-120">Requirement</span></span> | <span data-ttu-id="fe968-121">Value</span><span class="sxs-lookup"><span data-stu-id="fe968-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe968-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe968-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fe968-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fe968-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe968-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe968-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fe968-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe968-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe968-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe968-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe968-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe968-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe968-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe968-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe968-129">**\_SETUNICODEFORMAT LVM**</span><span class="sxs-lookup"><span data-stu-id="fe968-129">**LVM\_SETUNICODEFORMAT**</span></span>](lvm-setunicodeformat.md)
</dt> </dl>

 

 





