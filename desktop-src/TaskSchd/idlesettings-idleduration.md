---
title: Propiedad IdleSettings. IdleDuration
description: En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Programador de tareas de la propiedad IdleDuration
- Programador de tareas de la propiedad IdleDuration, objeto IdleSettings
- Programador de tareas de objeto IdleSettings, propiedad IdleDuration
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802990"
---
# <a name="idlesettingsidleduration-property"></a><span data-ttu-id="8039d-106">Propiedad IdleSettings. IdleDuration</span><span class="sxs-lookup"><span data-stu-id="8039d-106">IdleSettings.IdleDuration property</span></span>

<span data-ttu-id="8039d-107">En el caso de scripting, obtiene o establece un valor que indica la cantidad de tiempo que el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.</span><span class="sxs-lookup"><span data-stu-id="8039d-107">For scripting, gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span>

## <a name="syntax"></a><span data-ttu-id="8039d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8039d-108">Syntax</span></span>


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a><span data-ttu-id="8039d-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8039d-109">Property value</span></span>

<span data-ttu-id="8039d-110">Valor que indica la cantidad de tiempo que el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.</span><span class="sxs-lookup"><span data-stu-id="8039d-110">A value that indicates the amount of time that the computer must be in an idle state before the task is run).</span></span> <span data-ttu-id="8039d-111">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="8039d-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="8039d-112">El valor mínimo es un minuto.</span><span class="sxs-lookup"><span data-stu-id="8039d-112">The minimum value is one minute.</span></span> <span data-ttu-id="8039d-113">Si este valor es **null**, el retraso se establecerá en el valor predeterminado de 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="8039d-113">If this value is **NULL**, then the delay will be set to the default of 10 minutes.</span></span>

## <a name="remarks"></a><span data-ttu-id="8039d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8039d-114">Remarks</span></span>

<span data-ttu-id="8039d-115">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="8039d-115">When reading or writing XML for a task, this setting is specified in the [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8039d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8039d-116">Requirements</span></span>



| <span data-ttu-id="8039d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8039d-117">Requirement</span></span> | <span data-ttu-id="8039d-118">Value</span><span class="sxs-lookup"><span data-stu-id="8039d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8039d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8039d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8039d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8039d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8039d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8039d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8039d-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8039d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8039d-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8039d-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="8039d-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8039d-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8039d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8039d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8039d-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8039d-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8039d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8039d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8039d-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8039d-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="8039d-129">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="8039d-129">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





