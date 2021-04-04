---
title: Elemento de julio (monthsType)
description: Especifica que la tarea se ejecuta en julio.
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- Programador de tareas de julio
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6901ca83792ffd98269e26dc9cf24dd575025c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803326"
---
# <a name="july-monthstype-element"></a><span data-ttu-id="e3b46-104">Elemento de julio (monthsType)</span><span class="sxs-lookup"><span data-stu-id="e3b46-104">July (monthsType) Element</span></span>

<span data-ttu-id="e3b46-105">Especifica que la tarea se ejecuta en julio.</span><span class="sxs-lookup"><span data-stu-id="e3b46-105">Specifies that the task runs in July.</span></span>

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="e3b46-106">El elemento de **Julio** se define mediante el tipo complejo de [**monthsType**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e3b46-106">The **July** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e3b46-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="e3b46-107">Parent element</span></span>



| <span data-ttu-id="e3b46-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e3b46-108">Element</span></span>                                                                                                          | <span data-ttu-id="e3b46-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e3b46-109">Derived from</span></span>                                                     | <span data-ttu-id="e3b46-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3b46-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3b46-111">**Meses (monthlyDayOfWeekScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="e3b46-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="e3b46-112">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="e3b46-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="e3b46-113">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual de día de la semana.</span><span class="sxs-lookup"><span data-stu-id="e3b46-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="e3b46-114">**Meses (monthlyScheduleType)**</span><span class="sxs-lookup"><span data-stu-id="e3b46-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="e3b46-115">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="e3b46-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="e3b46-116">Especifica los meses del año en los que se ejecuta la tarea para una programación mensual.</span><span class="sxs-lookup"><span data-stu-id="e3b46-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="e3b46-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e3b46-117">Examples</span></span>

<span data-ttu-id="e3b46-118">El siguiente código XML define un calendario de meses que ejecuta la tarea en julio.</span><span class="sxs-lookup"><span data-stu-id="e3b46-118">The following XML defines a months calendar that runs the task in July.</span></span>


```XML
<Months>
    <July/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="e3b46-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3b46-119">Requirements</span></span>



| <span data-ttu-id="e3b46-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b46-120">Requirement</span></span> | <span data-ttu-id="e3b46-121">Value</span><span class="sxs-lookup"><span data-stu-id="e3b46-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e3b46-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3b46-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b46-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e3b46-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e3b46-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3b46-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b46-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3b46-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3b46-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3b46-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b46-127">Programador de tareas elementos de esquema</span><span class="sxs-lookup"><span data-stu-id="e3b46-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e3b46-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e3b46-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





