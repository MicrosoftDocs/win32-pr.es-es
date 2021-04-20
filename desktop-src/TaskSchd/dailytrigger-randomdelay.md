---
title: DailyTrigger.RandomDelay, propiedad
description: Para el scripting, obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | DailyTrigger.RandomDelay, propiedad
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Propiedad RandomDelay Programador de tareas
- Propiedad RandomDelay Programador de tareas , objeto DailyTrigger
- Objeto DailyTrigger Programador de tareas , propiedad RandomDelay
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303192d578a2681e250784c1e1eb2831c98482cc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734110"
---
# <a name="dailytriggerrandomdelay-property"></a><span data-ttu-id="23700-107">DailyTrigger.RandomDelay, propiedad</span><span class="sxs-lookup"><span data-stu-id="23700-107">DailyTrigger.RandomDelay property</span></span>

<span data-ttu-id="23700-108">Para el scripting, obtiene o establece una hora de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="23700-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="23700-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23700-109">Syntax</span></span>


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="23700-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="23700-110">Property value</span></span>

<span data-ttu-id="23700-111">Tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="23700-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="23700-112">El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, P2DT5S es un retraso de 2 días y 5 segundos).</span><span class="sxs-lookup"><span data-stu-id="23700-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="23700-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23700-113">Requirements</span></span>



| <span data-ttu-id="23700-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="23700-114">Requirement</span></span> | <span data-ttu-id="23700-115">Valor</span><span class="sxs-lookup"><span data-stu-id="23700-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23700-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23700-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23700-117">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="23700-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="23700-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23700-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23700-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="23700-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23700-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="23700-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="23700-121"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23700-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23700-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23700-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23700-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23700-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23700-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="23700-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23700-125">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="23700-125">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> <dt>

[<span data-ttu-id="23700-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="23700-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





