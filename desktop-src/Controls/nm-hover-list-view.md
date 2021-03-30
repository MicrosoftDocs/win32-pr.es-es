---
title: Código de notificación de NM_HOVER (vista de lista) (commctrl. h)
description: Lo envía un control de vista de lista cuando se mantiene el mouse sobre un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- NM_HOVER (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904996"
---
# <a name="nm_hover-list-view-notification-code"></a><span data-ttu-id="67424-105">Código de notificación de desplazamiento de NM \_ (vista de lista)</span><span class="sxs-lookup"><span data-stu-id="67424-105">NM\_HOVER (list view) notification code</span></span>

<span data-ttu-id="67424-106">Lo envía un control de vista de lista cuando se mantiene el mouse sobre un elemento.</span><span class="sxs-lookup"><span data-stu-id="67424-106">Sent by a list-view control when the mouse hovers over an item.</span></span> <span data-ttu-id="67424-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="67424-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="67424-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67424-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67424-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67424-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67424-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="67424-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67424-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67424-111">Return value</span></span>

<span data-ttu-id="67424-112">Devuelve cero para permitir que la vista de lista procese el desplazamiento normal, o un valor distinto de cero para evitar que se procese el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="67424-112">Return zero to allow the list view to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="67424-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67424-113">Requirements</span></span>



| <span data-ttu-id="67424-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="67424-114">Requirement</span></span> | <span data-ttu-id="67424-115">Value</span><span class="sxs-lookup"><span data-stu-id="67424-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67424-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67424-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67424-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="67424-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67424-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67424-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67424-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="67424-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67424-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67424-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67424-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="67424-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





