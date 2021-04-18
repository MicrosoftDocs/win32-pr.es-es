---
title: Elemento de diciembre (monthsType)
description: Especifica que la tarea se ejecuta en diciembre.
ms.assetid: 42f3cfb2-8e82-46a0-b3ef-42e83d329124
keywords:
- Programador de tareas del elemento de diciembre
topic_type:
- apiref
api_name:
- December
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c907262fe67a0529917d085583465eb97f94c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677000"
---
# <a name="december-monthstype-element"></a><span data-ttu-id="ad867-104">Elemento de diciembre (monthsType)</span><span class="sxs-lookup"><span data-stu-id="ad867-104">December (monthsType) Element</span></span>

<span data-ttu-id="ad867-105">Especifica que la tarea se ejecuta en diciembre.</span><span class="sxs-lookup"><span data-stu-id="ad867-105">Specifies that the task runs in December.</span></span>

``` syntax
<xs:element name="December">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="ad867-106">El elemento de **diciembre** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ad867-106">The **December** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ad867-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ad867-107">Parent element</span></span>



| <span data-ttu-id="ad867-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ad867-108">Element</span></span>                                                                                                          | <span data-ttu-id="ad867-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="ad867-109">Derived from</span></span>                                                     | <span data-ttu-id="ad867-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad867-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad867-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="ad867-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="ad867-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="ad867-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="ad867-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ad867-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="ad867-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="ad867-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="ad867-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="ad867-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="ad867-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="ad867-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="ad867-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ad867-117">Examples</span></span>

<span data-ttu-id="ad867-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en diciembre.</span><span class="sxs-lookup"><span data-stu-id="ad867-118">The following XML defines a months calendar that runs the task in December.</span></span>


```XML
<Months>
    <December/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="ad867-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad867-119">Requirements</span></span>



| <span data-ttu-id="ad867-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad867-120">Requirement</span></span> | <span data-ttu-id="ad867-121">Value</span><span class="sxs-lookup"><span data-stu-id="ad867-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad867-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad867-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ad867-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ad867-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ad867-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad867-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ad867-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad867-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad867-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad867-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad867-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="ad867-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ad867-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ad867-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





