---
title: Código de notificación de NM_RELEASEDCAPTURE (pestaña) (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- Controles de Windows de código de notificación de NM_RELEASEDCAPTURE (pestaña)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9c9049b63afb18413aea9fa77b7947e97e93b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491446"
---
# <a name="nm_releasedcapture-tab-notification-code"></a><span data-ttu-id="0fd7a-105">\_RELEASEDCAPTURE código de notificación de nm (pestaña)</span><span class="sxs-lookup"><span data-stu-id="0fd7a-105">NM\_RELEASEDCAPTURE (tab) notification code</span></span>

<span data-ttu-id="0fd7a-106">Notifica a la ventana primaria de un control de pestaña que el control está liberando la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="0fd7a-106">Notifies a tab control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="0fd7a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd7a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0fd7a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fd7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fd7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fd7a-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="0fd7a-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd7a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fd7a-111">Return value</span></span>

<span data-ttu-id="0fd7a-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0fd7a-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd7a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fd7a-113">Requirements</span></span>



| <span data-ttu-id="0fd7a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd7a-114">Requirement</span></span> | <span data-ttu-id="0fd7a-115">Value</span><span class="sxs-lookup"><span data-stu-id="0fd7a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd7a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fd7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd7a-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0fd7a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fd7a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fd7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd7a-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0fd7a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fd7a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fd7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd7a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd7a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





