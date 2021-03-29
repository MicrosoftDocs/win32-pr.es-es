---
title: Schtasks.exe
description: Permite a un administrador crear, eliminar, consultar, cambiar, ejecutar y finalizar tareas programadas en un equipo local o remoto.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Programador de tareas
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 2a57ee4edae1cd1604f10a88f3fc8cf2ea0971fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679313"
---
# <a name="schtasksexe"></a><span data-ttu-id="8b441-104">Schtasks.exe</span><span class="sxs-lookup"><span data-stu-id="8b441-104">Schtasks.exe</span></span>

<span data-ttu-id="8b441-105">Permite a un administrador crear, eliminar, consultar, cambiar, ejecutar y finalizar tareas programadas en un equipo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="8b441-105">Enables an administrator to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> <span data-ttu-id="8b441-106">Al ejecutar Schtasks.exe sin argumentos, se muestra el estado y el siguiente tiempo de ejecución de cada tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="8b441-106">Running Schtasks.exe without arguments displays the status and next run time for each registered task.</span></span> 

<span data-ttu-id="8b441-107">Para obtener más información sobre Programador de tareas, vea esta introducción: [programador de tareas para desarrolladores](task-scheduler-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="8b441-107">For more information on Task Scheduler, see this introduction: [Task Scheduler for developers](task-scheduler-start-page.md).</span></span>

## <a name="creating-a-task"></a><span data-ttu-id="8b441-108">Crear una tarea</span><span class="sxs-lookup"><span data-stu-id="8b441-108">Creating a Task</span></span>

<span data-ttu-id="8b441-109">La siguiente sintaxis se usa para crear una tarea en el equipo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="8b441-109">The following syntax is used to create a task on the local or remote computer.</span></span>

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

## <a name="parameters"></a><span data-ttu-id="8b441-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b441-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b441-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="8b441-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-112">Valor que especifica el equipo remoto al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="8b441-112">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="8b441-113">Si se omite, el valor predeterminado del parámetro System es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8b441-113">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**</span><span class="sxs-lookup"><span data-stu-id="8b441-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-115">Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-115">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**</span><span class="sxs-lookup"><span data-stu-id="8b441-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-117">Valor que especifica la contraseña para un contexto de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="8b441-117">A value that specifies the password for a given user context.</span></span> <span data-ttu-id="8b441-118">Si se omite, Schtasks.exe solicita la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="8b441-118">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span> **Nombre de usuario** /RU</span><span class="sxs-lookup"><span data-stu-id="8b441-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-120">Valor que especifica el contexto de usuario en el que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-120">A value that specifies the user context under which the task runs.</span></span> <span data-ttu-id="8b441-121">En la cuenta del sistema, los valores válidos son "", "NT AUTHORITY \\ System" o "System".</span><span class="sxs-lookup"><span data-stu-id="8b441-121">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="8b441-122">Por Programador de tareas 2,0 tareas, "NT AUTHORITY \\ LOCALSERVICE" y "NT Authority \\ NETWORKSERVICE" también son valores válidos.</span><span class="sxs-lookup"><span data-stu-id="8b441-122">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE", and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[ contraseña \]**</span><span class="sxs-lookup"><span data-stu-id="8b441-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-124">Valor que especifica la contraseña para el usuario especificado con el parámetro/RU.</span><span class="sxs-lookup"><span data-stu-id="8b441-124">A value that specifies the password for the user specified with the /RU parameter.</span></span> <span data-ttu-id="8b441-125">Para solicitar la contraseña, el valor debe ser " \* " o ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8b441-125">To prompt for the password, the value must be either "\*" or no value.</span></span> <span data-ttu-id="8b441-126">Esta contraseña se omite para la cuenta del sistema.</span><span class="sxs-lookup"><span data-stu-id="8b441-126">This password is ignored for the system account.</span></span> <span data-ttu-id="8b441-127">Este parámetro debe combinarse con el modificador/RU o/XML.</span><span class="sxs-lookup"><span data-stu-id="8b441-127">This parameter must be combined with either /RU or the /XML switch.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** ( **programación** )</span><span class="sxs-lookup"><span data-stu-id="8b441-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **schedule**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-129">Valor que especifica la frecuencia de programación.</span><span class="sxs-lookup"><span data-stu-id="8b441-129">A value that specifies the schedule frequency.</span></span> <span data-ttu-id="8b441-130">Los valores válidos son: MINUTE, HOURly, DAILY, WEEKly, MONTHly, ONCE, ONLOGON, OnIdle e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-130">Valid values are: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Mo** ( **modificador** )</span><span class="sxs-lookup"><span data-stu-id="8b441-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/MO** **modifier**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-132">Un valor que refina el tipo de programación para permitir un mayor control sobre la periodicidad de la programación.</span><span class="sxs-lookup"><span data-stu-id="8b441-132">A value that refines the schedule type to allow for finer control over the schedule recurrence.</span></span> <span data-ttu-id="8b441-133">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="8b441-133">Valid values are:</span></span>

-   <span data-ttu-id="8b441-134">MINUTO: 1-1439 minutos.</span><span class="sxs-lookup"><span data-stu-id="8b441-134">MINUTE: 1 - 1439 minutes.</span></span>
-   <span data-ttu-id="8b441-135">CADA hora: 1-23 horas.</span><span class="sxs-lookup"><span data-stu-id="8b441-135">HOURLY: 1 - 23 hours.</span></span>
-   <span data-ttu-id="8b441-136">DIARIAMENTE: 1-365 días.</span><span class="sxs-lookup"><span data-stu-id="8b441-136">DAILY: 1 - 365 days.</span></span>
-   <span data-ttu-id="8b441-137">SEMANAL: semanas 1-52.</span><span class="sxs-lookup"><span data-stu-id="8b441-137">WEEKLY: weeks 1 - 52.</span></span>
-   <span data-ttu-id="8b441-138">UNA vez: sin modificadores.</span><span class="sxs-lookup"><span data-stu-id="8b441-138">ONCE: No modifiers.</span></span>
-   <span data-ttu-id="8b441-139">OnStart: sin modificadores.</span><span class="sxs-lookup"><span data-stu-id="8b441-139">ONSTART: No modifiers.</span></span>
-   <span data-ttu-id="8b441-140">ONLOGON: sin modificadores.</span><span class="sxs-lookup"><span data-stu-id="8b441-140">ONLOGON: No modifiers.</span></span>
-   <span data-ttu-id="8b441-141">OnIdle: sin modificadores.</span><span class="sxs-lookup"><span data-stu-id="8b441-141">ONIDLE: No modifiers.</span></span>
-   <span data-ttu-id="8b441-142">MONTHly: 1-12, or FIRST, SECOND, THIRD, cuarto, LAST y LASTDAY.</span><span class="sxs-lookup"><span data-stu-id="8b441-142">MONTHLY: 1 - 12, or FIRST, SECOND, THIRD, FOURTH, LAST, and LASTDAY.</span></span>
-   <span data-ttu-id="8b441-143">ONEVENT: cadena de consulta de evento XPath.</span><span class="sxs-lookup"><span data-stu-id="8b441-143">ONEVENT: XPath event query string.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **días**</span><span class="sxs-lookup"><span data-stu-id="8b441-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **days**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-145">Valor que especifica el día de la semana en el que se va a ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-145">A value that specifies the day of the week to run the task.</span></span> <span data-ttu-id="8b441-146">Los valores válidos son: MON, mar, Mié, THU, Vie, SAT, SUN y para las programaciones mensuales 1-31 (días del mes).</span><span class="sxs-lookup"><span data-stu-id="8b441-146">Valid values are: MON, TUE, WED, THU, FRI, SAT, SUN and for MONTHLY schedules 1 - 31 (days of the month).</span></span> <span data-ttu-id="8b441-147">El carácter comodín ( \* ) especifica todos los días.</span><span class="sxs-lookup"><span data-stu-id="8b441-147">The wildcard character (\*) specifies all days.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **meses**</span><span class="sxs-lookup"><span data-stu-id="8b441-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **months**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-149">Valor que especifica los meses del año.</span><span class="sxs-lookup"><span data-stu-id="8b441-149">A value that specifies months of the year.</span></span> <span data-ttu-id="8b441-150">El valor predeterminado es el primer día del mes.</span><span class="sxs-lookup"><span data-stu-id="8b441-150">Defaults to the first day of the month.</span></span> <span data-ttu-id="8b441-151">Los valores válidos son: JAN, FEB, MAR, APR, mayo, JUN, JUL, ago, SEP, OCT, NOV y DEC.</span><span class="sxs-lookup"><span data-stu-id="8b441-151">Valid values are: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV, and DEC.</span></span> <span data-ttu-id="8b441-152">El carácter comodín ( \* ) especifica todos los meses.</span><span class="sxs-lookup"><span data-stu-id="8b441-152">The wildcard character (\*) specifies all months.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **tiempodeinactividad**</span><span class="sxs-lookup"><span data-stu-id="8b441-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-154">Valor que especifica la cantidad de tiempo de inactividad que se va a esperar antes de ejecutar una tarea de OnIdle programada.</span><span class="sxs-lookup"><span data-stu-id="8b441-154">A value that specifies the amount of idle time to wait before running a scheduled ONIDLE task.</span></span> <span data-ttu-id="8b441-155">El intervalo válido es de 1-999 minutos.</span><span class="sxs-lookup"><span data-stu-id="8b441-155">The valid range is 1 - 999 minutes.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**</span><span class="sxs-lookup"><span data-stu-id="8b441-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-157">Valor que especifica un nombre que identifica de forma única la tarea programada.</span><span class="sxs-lookup"><span data-stu-id="8b441-157">A value that specifies a name which uniquely identifies the scheduled task.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** </span><span class="sxs-lookup"><span data-stu-id="8b441-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-159">Valor que especifica la ruta de acceso y el nombre de archivo de la tarea que se va a ejecutar en el momento programado.</span><span class="sxs-lookup"><span data-stu-id="8b441-159">A value that specifies the path and file name of the task to be run at the scheduled time.</span></span> <span data-ttu-id="8b441-160">Por ejemplo: C: \\ Windows \\ system32 \\calc.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-160">For example: C:\\Windows\\System32\\calc.exe.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **startTime**</span><span class="sxs-lookup"><span data-stu-id="8b441-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-162">Valor que especifica la hora de inicio para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-162">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="8b441-163">El formato de hora es HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="8b441-163">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="8b441-164">Por ejemplo, 14:30 especifica 2: las 16:30.</span><span class="sxs-lookup"><span data-stu-id="8b441-164">For example, 14:30 specifies 2:30PM.</span></span> <span data-ttu-id="8b441-165">El valor predeterminado es la hora actual en que no se especifica/ST.</span><span class="sxs-lookup"><span data-stu-id="8b441-165">The default is the current time is /ST is not specified.</span></span> <span data-ttu-id="8b441-166">Esta opción es necesaria para el argumento/SC una vez.</span><span class="sxs-lookup"><span data-stu-id="8b441-166">This option is required wit the /SC ONCE argument.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **intervalo**</span><span class="sxs-lookup"><span data-stu-id="8b441-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-168">Valor que especifica el intervalo de repetición en minutos.</span><span class="sxs-lookup"><span data-stu-id="8b441-168">A value that specifies the repetition interval in minutes.</span></span> <span data-ttu-id="8b441-169">Esto no es aplicable a los siguientes tipos de programación: MINUTE, HOURly, OnStart, ONLOGON, OnIdle e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-169">This is not applicable for the following schedule types: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="8b441-170">El intervalo válido es de 1-599940 minutos.</span><span class="sxs-lookup"><span data-stu-id="8b441-170">The valid range is 1 - 599940 minutes.</span></span> <span data-ttu-id="8b441-171">Si se especifican los parámetros/ET o/DU, el valor predeterminado es 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="8b441-171">If either the /ET or /DU parameters are specified, the default is 10 minutes.</span></span>

<span data-ttu-id="8b441-172">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-172">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**</span><span class="sxs-lookup"><span data-stu-id="8b441-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-174">Valor que especifica la hora de finalización para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-174">A value that specifies the end time to run the task.</span></span> <span data-ttu-id="8b441-175">El formato de hora es HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="8b441-175">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="8b441-176">Por ejemplo, 14:50 especifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="8b441-176">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="8b441-177">Esto no es aplicable a los siguientes tipos de programación: OnStart, ONLOGON, OnIdle e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-177">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

<span data-ttu-id="8b441-178">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-178">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **duración**</span><span class="sxs-lookup"><span data-stu-id="8b441-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-180">Valor que especifica la duración para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-180">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="8b441-181">El formato de hora es HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="8b441-181">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="8b441-182">Por ejemplo, 14:50 especifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="8b441-182">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="8b441-183">Esto no es aplicable con/ET y para los siguientes tipos de programación: OnStart, ONLOGON, OnIdle e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-183">This is not applicable with /ET and for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="8b441-184">En el caso de las tareas de/V1 (Programador de tareas 1,0), si se especifica/RI, el valor predeterminado de Duration es una hora.</span><span class="sxs-lookup"><span data-stu-id="8b441-184">For /V1 tasks (Task Scheduler 1.0 tasks), if /RI is specified, then the duration default is one hour.</span></span>

<span data-ttu-id="8b441-185">**Windows XP:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-185">**Windows XP:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="8b441-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-187">Valor que finaliza la tarea en la hora de finalización o en el tiempo de duración.</span><span class="sxs-lookup"><span data-stu-id="8b441-187">A value that terminates the task at the end time or duration time.</span></span> <span data-ttu-id="8b441-188">Esto no es aplicable a los siguientes tipos de programación: OnStart, ONLOGON, OnIdle e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-188">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="8b441-189">Se debe especificar/ET o/DU.</span><span class="sxs-lookup"><span data-stu-id="8b441-189">Either /ET or /DU must be specified.</span></span>

<span data-ttu-id="8b441-190">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-190">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startDate**</span><span class="sxs-lookup"><span data-stu-id="8b441-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-192">Valor que especifica la primera fecha en la que se va a ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-192">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="8b441-193">El formato es mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="8b441-193">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="8b441-194">El valor predeterminado es la fecha actual.</span><span class="sxs-lookup"><span data-stu-id="8b441-194">This value defaults to the current date.</span></span> <span data-ttu-id="8b441-195">Esto no es aplicable a los siguientes tipos de programación: una vez, OnStart, ONLOGON, OnIdle e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-195">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="8b441-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-197">Valor que especifica la última fecha en la que se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-197">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="8b441-198">El formato es mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="8b441-198">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="8b441-199">Esto no es aplicable a los siguientes tipos de programación: una vez, OnStart, ONLOGON, OnIdle e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-199">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span><span class="sxs-lookup"><span data-stu-id="8b441-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-201">Valor que especifica el canal de eventos para los desencadenadores ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-201">A value that specifies the event channel for ONEVENT triggers.</span></span>

<span data-ttu-id="8b441-202">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-202">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="8b441-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-204">Un valor que permite que la tarea se ejecute de forma interactiva solo si el usuario/RU está conectado actualmente en el momento en que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-204">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="8b441-205">La tarea solo se ejecuta si el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="8b441-205">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="8b441-206">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-206">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span><span class="sxs-lookup"><span data-stu-id="8b441-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-208">Valor que indica que no hay ninguna contraseña almacenada.</span><span class="sxs-lookup"><span data-stu-id="8b441-208">A value that indicates that no password is stored.</span></span> <span data-ttu-id="8b441-209">La tarea no se ejecuta de forma interactiva como el usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="8b441-209">The task does not run interactively as the given user.</span></span> <span data-ttu-id="8b441-210">Solo están disponibles los recursos locales.</span><span class="sxs-lookup"><span data-stu-id="8b441-210">Only local resources are available.</span></span>

<span data-ttu-id="8b441-211">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-211">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="8b441-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-213">Valor que marca la tarea que se va a eliminar después de su última ejecución.</span><span class="sxs-lookup"><span data-stu-id="8b441-213">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="8b441-214">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-214">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span> **Xmlfile** de/XML</span><span class="sxs-lookup"><span data-stu-id="8b441-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-216">Valor que crea una tarea a partir de un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="8b441-216">A value that creates a task from an XML file.</span></span> <span data-ttu-id="8b441-217">Este parámetro se puede combinar con los modificadores/RU y/RP, o con el modificador/RP solo cuando el XML de la tarea ya contiene la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8b441-217">This parameter can be combined with /RU and /RP switches, or with the /RP switch alone when the task XML already contains the principal.</span></span>

<span data-ttu-id="8b441-218">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-218">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span><span class="sxs-lookup"><span data-stu-id="8b441-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-220">Valor que crea una tarea visible para las plataformas Windows 2000, Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8b441-220">A value that creates a task visible to Windows 2000, Windows Server 2003, and Windows XP platforms.</span></span>

<span data-ttu-id="8b441-221">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-221">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="8b441-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-223">Valor que fuerza la creación de la tarea y suprime las advertencias si la tarea especificada ya existe.</span><span class="sxs-lookup"><span data-stu-id="8b441-223">A value that forcefully creates the task and suppresses warnings if the specified task already exists.</span></span>

<span data-ttu-id="8b441-224">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-224">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Nivel** de/RL</span><span class="sxs-lookup"><span data-stu-id="8b441-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-226">Valor que establece el nivel de ejecución de la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-226">A value that sets the run level for the task.</span></span> <span data-ttu-id="8b441-227">Los valores válidos son LIMITED y HIGHEST.</span><span class="sxs-lookup"><span data-stu-id="8b441-227">Valid values are LIMITED and HIGHEST.</span></span> <span data-ttu-id="8b441-228">El valor predeterminado es limitado.</span><span class="sxs-lookup"><span data-stu-id="8b441-228">The default is LIMITED.</span></span>

<span data-ttu-id="8b441-229">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-229">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **Delaytime**</span><span class="sxs-lookup"><span data-stu-id="8b441-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-231">Valor que especifica el tiempo de espera para retrasar la tarea después de que se desencadene el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="8b441-231">A value that specifies the wait time to delay the task after the trigger is fired.</span></span> <span data-ttu-id="8b441-232">El formato de hora es mmmm: SS.</span><span class="sxs-lookup"><span data-stu-id="8b441-232">The time format is mmmm:ss.</span></span> <span data-ttu-id="8b441-233">Esta opción solo es válida para los tipos de programación OnStart, ONLOGON e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-233">This option is only valid for schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="8b441-234">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-234">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-235"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="8b441-235"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-236">Valor que muestra el mensaje de ayuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-236">A value that displays the help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b441-237">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b441-237">Remarks</span></span>

<span data-ttu-id="8b441-238">Al crear una tarea en un equipo remoto que se ejecuta en el sistema operativo Windows XP, Windows Server 2003 o Windows 2000, use el modificador/v1</span><span class="sxs-lookup"><span data-stu-id="8b441-238">When creating a task on a remote computer running on the Windows XP, Windows Server 2003, or Windows 2000 operating system, use the /V1 switch.</span></span>

<span data-ttu-id="8b441-239">No se puede crear una tarea remota Programador de tareas 1,0 no interactiva (cree una tarea sin usar el modificador/IT y usando el modificador/V1) si el equipo remoto tiene habilitada la excepción de Firewall compartir archivos e impresoras y la excepción de Firewall administración remota de tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="8b441-239">You cannot create a non-interactive remote Task Scheduler 1.0 task (create a task by not using the /IT switch and using the /V1 switch) if the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled.</span></span>

## <a name="deleting-a-task"></a><span data-ttu-id="8b441-240">Eliminar una tarea</span><span class="sxs-lookup"><span data-stu-id="8b441-240">Deleting a Task</span></span>

<span data-ttu-id="8b441-241">La siguiente sintaxis se usa para eliminar una o varias tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="8b441-241">The following syntax is used to delete one or more scheduled tasks.</span></span>

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

## <a name="parameters"></a><span data-ttu-id="8b441-242">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b441-242">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b441-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="8b441-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-244">Valor que especifica el equipo remoto al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="8b441-244">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="8b441-245">Si se omite, el valor predeterminado del parámetro System es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8b441-245">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**</span><span class="sxs-lookup"><span data-stu-id="8b441-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-247">Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-247">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**</span><span class="sxs-lookup"><span data-stu-id="8b441-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-249">Valor que especifica la contraseña para el contexto de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="8b441-249">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="8b441-250">Si se omite, Schtasks.exe solicita la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="8b441-250">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**</span><span class="sxs-lookup"><span data-stu-id="8b441-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-252">Valor que especifica el nombre de la tarea programada que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8b441-252">A value that specifies the name of the scheduled task to delete.</span></span> <span data-ttu-id="8b441-253">El carácter comodín ( \* ) se puede usar para eliminar todas las tareas.</span><span class="sxs-lookup"><span data-stu-id="8b441-253">The wildcard character (\*) can be used to delete all tasks.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="8b441-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-255">Valor que fuerza la eliminación de la tarea y suprime las advertencias si se está ejecutando la tarea especificada.</span><span class="sxs-lookup"><span data-stu-id="8b441-255">A value that forcefully deletes the task and suppresses warnings if the specified task is running.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-256"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="8b441-256"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-257">Valor que muestra la ayuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-257">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="running-a-task"></a><span data-ttu-id="8b441-258">Ejecutar una tarea</span><span class="sxs-lookup"><span data-stu-id="8b441-258">Running a Task</span></span>

<span data-ttu-id="8b441-259">La siguiente sintaxis se usa para ejecutar inmediatamente una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="8b441-259">The following syntax is used to immediately run a scheduled task.</span></span>

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a><span data-ttu-id="8b441-260">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b441-260">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b441-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="8b441-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-262">Valor que especifica el equipo remoto al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="8b441-262">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="8b441-263">Si se omite, el valor predeterminado del parámetro System es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8b441-263">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**</span><span class="sxs-lookup"><span data-stu-id="8b441-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-265">Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-265">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**</span><span class="sxs-lookup"><span data-stu-id="8b441-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-267">Valor que especifica la contraseña para el contexto de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="8b441-267">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="8b441-268">Si se omite, Schtasks.exe solicita la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="8b441-268">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**</span><span class="sxs-lookup"><span data-stu-id="8b441-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-270">Valor que especifica el nombre de la tarea programada que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="8b441-270">A value that specifies the name of the scheduled task to run.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-271"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="8b441-271"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-272">Valor que muestra la ayuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-272">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="ending-a-running-task"></a><span data-ttu-id="8b441-273">Finalizar una tarea en ejecución</span><span class="sxs-lookup"><span data-stu-id="8b441-273">Ending a Running Task</span></span>

<span data-ttu-id="8b441-274">La siguiente sintaxis se usa para detener una tarea programada en ejecución.</span><span class="sxs-lookup"><span data-stu-id="8b441-274">The following syntax is used to stop a running scheduled task.</span></span>

> [!Note]  
> <span data-ttu-id="8b441-275">Para detener la ejecución de una tarea remota, asegúrese de que el equipo remoto tenga habilitadas las excepciones de Firewall administración de archivos e impresoras y tareas programadas remotas.</span><span class="sxs-lookup"><span data-stu-id="8b441-275">To stop a remote task from running, ensure that the remote computer has the File and Printer Sharing and Remote Scheduled Tasks Management firewall exceptions enabled.</span></span>

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a><span data-ttu-id="8b441-276">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b441-276">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b441-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="8b441-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-278">Valor que especifica el equipo remoto al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="8b441-278">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="8b441-279">Si se omite, el valor predeterminado del parámetro System es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8b441-279">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**</span><span class="sxs-lookup"><span data-stu-id="8b441-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-281">Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-281">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**</span><span class="sxs-lookup"><span data-stu-id="8b441-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-283">Valor que especifica la contraseña para el contexto de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="8b441-283">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="8b441-284">Si se omite, Schtasks.exe solicita la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="8b441-284">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**</span><span class="sxs-lookup"><span data-stu-id="8b441-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-286">Valor que especifica el nombre de la tarea programada que se va a detener.</span><span class="sxs-lookup"><span data-stu-id="8b441-286">A value that specifies the name of the scheduled task to stop.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-287"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="8b441-287"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-288">Valor que muestra la ayuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-288">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="querying-for-task-information"></a><span data-ttu-id="8b441-289">Consultar la información de la tarea</span><span class="sxs-lookup"><span data-stu-id="8b441-289">Querying for Task Information</span></span>

<span data-ttu-id="8b441-290">La siguiente sintaxis se usa para mostrar las tareas programadas desde el equipo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="8b441-290">The following syntax is used to display the scheduled tasks from the local or remote computer.</span></span>

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

## <a name="parameters"></a><span data-ttu-id="8b441-291">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b441-291">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b441-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="8b441-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-293">Valor que especifica el equipo remoto al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="8b441-293">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="8b441-294">Si se omite, el valor predeterminado del parámetro System es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8b441-294">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**</span><span class="sxs-lookup"><span data-stu-id="8b441-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-296">Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-296">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**</span><span class="sxs-lookup"><span data-stu-id="8b441-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-298">Valor que especifica la contraseña para el contexto de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="8b441-298">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="8b441-299">Si se omite, Schtasks.exe solicita la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="8b441-299">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **formato**</span><span class="sxs-lookup"><span data-stu-id="8b441-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-301">Valor que especifica el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="8b441-301">A value that specifies the output format.</span></span> <span data-ttu-id="8b441-302">Los valores válidos son TABLE, LIST y CSV.</span><span class="sxs-lookup"><span data-stu-id="8b441-302">The valid values are TABLE, LIST, and CSV.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span><span class="sxs-lookup"><span data-stu-id="8b441-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-304">Valor que especifica que el encabezado de columna no debe mostrarse en la salida.</span><span class="sxs-lookup"><span data-stu-id="8b441-304">A value that specifies that the column header should not be displayed in the output.</span></span> <span data-ttu-id="8b441-305">Esto solo es válido para los formatos de tabla y CSV.</span><span class="sxs-lookup"><span data-stu-id="8b441-305">This is valid only for TABLE and CSV formats.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="8b441-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-307">Valor que muestra el resultado detallado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-307">A value that displays verbose task output.</span></span>

> [!Note]  
> <span data-ttu-id="8b441-308">Si una tarea estaba programada para ejecutarse una sola vez, la información de programación mostrada es "la programación de datos no está disponible en este formato".</span><span class="sxs-lookup"><span data-stu-id="8b441-308">If a task was scheduled to run only one time, then the displayed schedule information is "Scheduling data is not available in this format."</span></span>

 

</dd> <dt>

<span data-ttu-id="8b441-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**</span><span class="sxs-lookup"><span data-stu-id="8b441-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-310">Valor que especifica el nombre de la tarea para la que se va a recuperar la información.</span><span class="sxs-lookup"><span data-stu-id="8b441-310">A value that specifies the task name for which to retrieve the information.</span></span> <span data-ttu-id="8b441-311">Si no se especifica ningún nombre de tarea, se mostrará la información de todas las tareas.</span><span class="sxs-lookup"><span data-stu-id="8b441-311">If no task name is specified, then information for all the tasks will be displayed.</span></span>

<span data-ttu-id="8b441-312">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-312">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span><span class="sxs-lookup"><span data-stu-id="8b441-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-314">Valor que se usa para mostrar las definiciones de tarea en formato XML.</span><span class="sxs-lookup"><span data-stu-id="8b441-314">A value that is used to display the task definitions in XML format.</span></span>

<span data-ttu-id="8b441-315">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-315">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-316"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="8b441-316"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-317">Valor que se usa para mostrar la ayuda de Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-317">A value that is used to display the Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="changing-a-task"></a><span data-ttu-id="8b441-318">Cambiar una tarea</span><span class="sxs-lookup"><span data-stu-id="8b441-318">Changing a Task</span></span>

<span data-ttu-id="8b441-319">La siguiente sintaxis se usa para cambiar la forma en que se ejecuta el programa, o para cambiar la cuenta de usuario y la contraseña que usa una tarea programada.</span><span class="sxs-lookup"><span data-stu-id="8b441-319">The following syntax is used to change how the program runs, or change the user account and password used by a scheduled task.</span></span>

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

## <a name="parameters"></a><span data-ttu-id="8b441-320">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b441-320">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b441-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**</span><span class="sxs-lookup"><span data-stu-id="8b441-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-322">Valor que especifica el equipo remoto al que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="8b441-322">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="8b441-323">Si se omite, el valor predeterminado del parámetro System es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="8b441-323">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**</span><span class="sxs-lookup"><span data-stu-id="8b441-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-325">Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-325">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**</span><span class="sxs-lookup"><span data-stu-id="8b441-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-327">Valor que especifica la contraseña para el contexto de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="8b441-327">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="8b441-328">Si se omite, Schtasks.exe solicita la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="8b441-328">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**</span><span class="sxs-lookup"><span data-stu-id="8b441-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-330">Valor que especifica la tarea programada que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="8b441-330">A value that specifies which scheduled task to change.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **como_usuario**</span><span class="sxs-lookup"><span data-stu-id="8b441-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-332">Valor que cambia el nombre de usuario (contexto de usuario) en el que se ejecutará la tarea programada.</span><span class="sxs-lookup"><span data-stu-id="8b441-332">A value that changes the user name (user context) under which the scheduled task will run.</span></span> <span data-ttu-id="8b441-333">En la cuenta del sistema, los valores válidos son "", "NT AUTHORITY \\ System" o "System".</span><span class="sxs-lookup"><span data-stu-id="8b441-333">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="8b441-334">Por Programador de tareas tareas 2,0, "NT AUTHORITY \\ LOCALSERVICE" y "NT Authority \\ NETWORKSERVICE" también son valores válidos.</span><span class="sxs-lookup"><span data-stu-id="8b441-334">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE" and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span><span class="sxs-lookup"><span data-stu-id="8b441-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-336">Valor que especifica una nueva contraseña para el contexto de usuario existente o la contraseña de una nueva cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="8b441-336">A value that specifies a new password for the existing user context or the password for a new user account.</span></span> <span data-ttu-id="8b441-337">Esta contraseña se omite para la cuenta del sistema.</span><span class="sxs-lookup"><span data-stu-id="8b441-337">This password is ignored for the system account.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** </span><span class="sxs-lookup"><span data-stu-id="8b441-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-339">Valor que especifica un nuevo programa que ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-339">A value that specifies a new program that the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **startTime**</span><span class="sxs-lookup"><span data-stu-id="8b441-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-341">Valor que especifica la hora de inicio para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-341">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="8b441-342">El formato de hora es HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="8b441-342">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="8b441-343">Por ejemplo, 14:30 especifica 2: las 16:30.</span><span class="sxs-lookup"><span data-stu-id="8b441-343">For example, 14:30 specifies 2:30PM.</span></span>

<span data-ttu-id="8b441-344">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-344">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **intervalo**</span><span class="sxs-lookup"><span data-stu-id="8b441-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-346">Valor que especifica el intervalo de repetición, en minutos.</span><span class="sxs-lookup"><span data-stu-id="8b441-346">A value that specifies the repetition interval, in minutes.</span></span> <span data-ttu-id="8b441-347">El intervalo válido es de 1-599940 minutos.</span><span class="sxs-lookup"><span data-stu-id="8b441-347">The valid range is 1 - 599940 minutes.</span></span>

<span data-ttu-id="8b441-348">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-348">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**</span><span class="sxs-lookup"><span data-stu-id="8b441-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-350">Valor que especifica la hora de finalización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-350">A value that specifies the end time for the task.</span></span> <span data-ttu-id="8b441-351">El formato de hora es HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="8b441-351">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="8b441-352">Por ejemplo, 14:50 especifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="8b441-352">For example, 14:50 specifies 2:50PM.</span></span>

<span data-ttu-id="8b441-353">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-353">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **duración**</span><span class="sxs-lookup"><span data-stu-id="8b441-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-355">Valor que especifica la duración para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-355">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="8b441-356">El formato de hora es HH: mm (hora de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="8b441-356">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="8b441-357">Por ejemplo, 14:50 especifica 2:50PM.</span><span class="sxs-lookup"><span data-stu-id="8b441-357">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="8b441-358">Esto no es aplicable con el parámetro/ET.</span><span class="sxs-lookup"><span data-stu-id="8b441-358">This is not applicable with the /ET parameter.</span></span>

<span data-ttu-id="8b441-359">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-359">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="8b441-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-361">Valor que finaliza la tarea en la hora de finalización o en el tiempo de duración.</span><span class="sxs-lookup"><span data-stu-id="8b441-361">A value that terminates the task at the end time or duration time.</span></span>

<span data-ttu-id="8b441-362">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-362">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startDate**</span><span class="sxs-lookup"><span data-stu-id="8b441-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-364">Valor que especifica la primera fecha en la que se va a ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-364">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="8b441-365">El formato es mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="8b441-365">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="8b441-366">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-366">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**</span><span class="sxs-lookup"><span data-stu-id="8b441-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-368">Valor que especifica la última fecha en la que se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-368">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="8b441-369">El formato es mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="8b441-369">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="8b441-370">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-370">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="8b441-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-372">Un valor que permite que la tarea se ejecute de forma interactiva solo si el usuario/RU está conectado actualmente en el momento en que se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-372">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="8b441-373">La tarea solo se ejecuta si el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="8b441-373">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="8b441-374">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-374">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Nivel** de/RL</span><span class="sxs-lookup"><span data-stu-id="8b441-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-376">Valor que establece el nivel de ejecución de la tarea.</span><span class="sxs-lookup"><span data-stu-id="8b441-376">A value that sets the run level for the task.</span></span> <span data-ttu-id="8b441-377">Los valores válidos son LIMITED y HIGHEST.</span><span class="sxs-lookup"><span data-stu-id="8b441-377">Valid values are LIMITED and HIGHEST.</span></span>

<span data-ttu-id="8b441-378">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-378">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span><span class="sxs-lookup"><span data-stu-id="8b441-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-380">Valor que habilita la tarea programada.</span><span class="sxs-lookup"><span data-stu-id="8b441-380">A value that enables the scheduled task.</span></span> <span data-ttu-id="8b441-381">Se puede ejecutar una tarea habilitada y no se puede ejecutar una tarea deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="8b441-381">An enabled task can run, and a disabled task cannot run.</span></span>

<span data-ttu-id="8b441-382">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-382">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span><span class="sxs-lookup"><span data-stu-id="8b441-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-384">Valor que deshabilita la ejecución de la tarea programada.</span><span class="sxs-lookup"><span data-stu-id="8b441-384">A value that disables the scheduled task from running.</span></span>

> [!Note]  
> <span data-ttu-id="8b441-385">Si la tarea Remote Programador de tareas 1,0 está deshabilitada Schtasks.exe y el equipo remoto tiene habilitada la excepción de Firewall compartir archivos e impresoras y la excepción de Firewall administración remota de tareas programadas, la tarea no se deshabilitará cuando se lea desde una API de Programador de tareas 2,0.</span><span class="sxs-lookup"><span data-stu-id="8b441-385">If a remote Task Scheduler 1.0 task is disabled by Schtasks.exe and the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled, then the task will not be disabled when read from a Task Scheduler 2.0 API.</span></span>

 

<span data-ttu-id="8b441-386">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-386">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="8b441-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-388">Valor que marca la tarea que se va a eliminar después de su última ejecución.</span><span class="sxs-lookup"><span data-stu-id="8b441-388">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="8b441-389">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-389">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **Delaytime**</span><span class="sxs-lookup"><span data-stu-id="8b441-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="8b441-391">Valor que especifica el tiempo de espera para retrasar la ejecución de la tarea después de que se desencadene el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="8b441-391">A value that specifies the wait time to delay the running of the task after the trigger is fired.</span></span> <span data-ttu-id="8b441-392">El formato de hora es mmmm: SS.</span><span class="sxs-lookup"><span data-stu-id="8b441-392">The time format is mmmm:ss.</span></span> <span data-ttu-id="8b441-393">Esta opción solo es válida para las tareas con los tipos de programación OnStart, ONLOGON e ONEVENT.</span><span class="sxs-lookup"><span data-stu-id="8b441-393">This option is only valid for tasks with the schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="8b441-394">**Windows XP y Windows Server 2003:** Esta opción no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8b441-394">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="8b441-395"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="8b441-395"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="8b441-396">Valor que muestra el mensaje de ayuda para Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="8b441-396">A value that displays the Help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b441-397">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b441-397">Requirements</span></span>



| <span data-ttu-id="8b441-398">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b441-398">Requirement</span></span> | <span data-ttu-id="8b441-399">Value</span><span class="sxs-lookup"><span data-stu-id="8b441-399">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8b441-400">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b441-400">Minimum supported client</span></span><br/> | <span data-ttu-id="8b441-401">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8b441-401">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8b441-402">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b441-402">Minimum supported server</span></span><br/> | <span data-ttu-id="8b441-403">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b441-403">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





