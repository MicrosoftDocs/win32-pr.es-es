---
title: Código de notificación de TDN_DESTROYED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea cuando se destruye y su identificador de ventana ya no es válido. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- TDN_DESTROYED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905625"
---
# <a name="tdn_destroyed-notification-code"></a><span data-ttu-id="26599-105">TDN \_ código de notificación destruido</span><span class="sxs-lookup"><span data-stu-id="26599-105">TDN\_DESTROYED notification code</span></span>

<span data-ttu-id="26599-106">Enviado por un cuadro de diálogo de tarea cuando se destruye y su identificador de ventana ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="26599-106">Sent by a task dialog when it is destroyed and its window handle is no longer valid.</span></span> <span data-ttu-id="26599-107">Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="26599-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="26599-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26599-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26599-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26599-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26599-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="26599-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="26599-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26599-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26599-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="26599-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26599-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26599-113">Return value</span></span>

<span data-ttu-id="26599-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="26599-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="26599-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26599-115">Requirements</span></span>



| <span data-ttu-id="26599-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="26599-116">Requirement</span></span> | <span data-ttu-id="26599-117">Value</span><span class="sxs-lookup"><span data-stu-id="26599-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26599-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26599-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26599-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="26599-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26599-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26599-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26599-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="26599-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26599-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26599-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="26599-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26599-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





