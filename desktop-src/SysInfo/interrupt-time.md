---
description: El tiempo de interrupción es la cantidad de tiempo transcurrido desde la última vez que se inició el sistema, en intervalos de 100 segundos.
ms.assetid: 56fe322e-53ea-4186-9b5e-352f69b09109
title: Tiempo de interrupción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6018d97ab0eecd1182c02b734357ca13fbe12632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666639"
---
# <a name="interrupt-time"></a><span data-ttu-id="263a2-103">Tiempo de interrupción</span><span class="sxs-lookup"><span data-stu-id="263a2-103">Interrupt Time</span></span>

<span data-ttu-id="263a2-104">El *tiempo de interrupción* es la cantidad de tiempo transcurrido desde la última vez que se inició el sistema, en intervalos de 100 segundos.</span><span class="sxs-lookup"><span data-stu-id="263a2-104">*Interrupt time* is the amount of time since the system was last started, in 100-nanosecond intervals.</span></span> <span data-ttu-id="263a2-105">El recuento de tiempo de interrupción comienza en cero cuando se inicia el sistema y se incrementa en cada interrupción del reloj por la duración de un paso del reloj.</span><span class="sxs-lookup"><span data-stu-id="263a2-105">The interrupt-time count begins at zero when the system starts and is incremented at each clock interrupt by the length of a clock tick.</span></span> <span data-ttu-id="263a2-106">La duración exacta de un paso de reloj depende del hardware subyacente y puede variar entre sistemas.</span><span class="sxs-lookup"><span data-stu-id="263a2-106">The exact length of a clock tick depends on underlying hardware and can vary between systems.</span></span>

<span data-ttu-id="263a2-107">A diferencia de la [hora del sistema](system-time.md), el recuento de tiempo de interrupción no está sujeto a ajustes por los usuarios o el servicio de hora de Windows, lo que lo convierte en una mejor opción para medir duraciones cortas.</span><span class="sxs-lookup"><span data-stu-id="263a2-107">Unlike [system time](system-time.md), the interrupt-time count is not subject to adjustments by users or the Windows time service, making it a better choice for measuring short durations.</span></span> <span data-ttu-id="263a2-108">Las aplicaciones que requieren mayor precisión que el número de tiempo de interrupción deben usar un [temporizador de alta resolución](../winmsg/about-timers.md).</span><span class="sxs-lookup"><span data-stu-id="263a2-108">Applications that require greater precision than the interrupt-time count should use a [high-resolution timer](../winmsg/about-timers.md).</span></span> <span data-ttu-id="263a2-109">Utilice la función [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) para recuperar la frecuencia del temporizador de alta resolución y la función [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) para recuperar el valor del contador.</span><span class="sxs-lookup"><span data-stu-id="263a2-109">Use the [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) function to retrieve the frequency of the high-resolution timer and the [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) function to retrieve the counter's value.</span></span>

<span data-ttu-id="263a2-110">Las funciones [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)y [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) se pueden usar para recuperar el recuento de tiempo de interrupción.</span><span class="sxs-lookup"><span data-stu-id="263a2-110">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions can be used to retrieve the interrupt-time count.</span></span> <span data-ttu-id="263a2-111">Tiempo de interrupción no sesgado significa que solo se cuenta el tiempo que el sistema está en el estado de funcionamiento; por lo tanto, el recuento de tiempo de interrupción no se "sesga" por el tiempo que el sistema invierte en suspensión o hibernación.</span><span class="sxs-lookup"><span data-stu-id="263a2-111">Unbiased interrupt-time means that only time that the system is in the working state is counted—therefore, the interrupt-time count is not "biased" by time the system spends in sleep or hibernation.</span></span>

<span data-ttu-id="263a2-112">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP/2000:** La función [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) está disponible a partir de Windows 7 y windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="263a2-112">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:** The [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="263a2-113">La resolución del temporizador establecida por las funciones [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) y [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) afecta a la resolución de las funciones [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) y [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) .</span><span class="sxs-lookup"><span data-stu-id="263a2-113">The timer resolution set by the [**timeBeginPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod) and [**timeEndPeriod**](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod) functions affects the resolution of the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) and [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) functions.</span></span> <span data-ttu-id="263a2-114">Sin embargo, no se recomienda aumentar la resolución del temporizador porque puede reducir el rendimiento general del sistema y aumentar el consumo de energía evitando que el procesador entre en Estados de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="263a2-114">However, increasing the timer resolution is not recommended because it can reduce overall system performance and increase power consumption by preventing the processor from entering power-saving states.</span></span> <span data-ttu-id="263a2-115">En su lugar, las aplicaciones deben usar un temporizador de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="263a2-115">Instead, applications should use a high-resolution timer.</span></span>

> [!Note]  
> <span data-ttu-id="263a2-116">Las funciones [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)y [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) generan resultados diferentes en las compilaciones de depuración ("comprobadas") de Windows, ya que el recuento de ciclos y tiempos de interrupción es de aproximadamente 49 días.</span><span class="sxs-lookup"><span data-stu-id="263a2-116">The [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions produces different results on debug ("checked") builds of Windows, because the interrupt-time count and tick count are advanced by approximately 49 days.</span></span> <span data-ttu-id="263a2-117">Esto ayuda a identificar los errores que podrían no producirse hasta que el sistema se ejecute durante mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="263a2-117">This helps to identify bugs that might not occur until the system has been running for a long time.</span></span> <span data-ttu-id="263a2-118">La compilación comprobada está disponible para los suscriptores de MSDN a través del sitio web de [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="263a2-118">The checked build is available to MSDN subscribers through the [Microsoft Developer Network (MSDN)](https://msdn.microsoft.com/default.aspx) Web site.</span></span>

 

<span data-ttu-id="263a2-119">En el ejemplo siguiente se muestra cómo recuperar el recuento de tiempo de interrupción llamando a las funciones [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)y [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) .</span><span class="sxs-lookup"><span data-stu-id="263a2-119">The following example shows how to retrieve the interrupt-time count by calling the [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), and [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) functions.</span></span> <span data-ttu-id="263a2-120">Vínculo a la biblioteca OneCore. lib al compilar una aplicación de consola que llama a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="263a2-120">Link to the OneCore.lib library when you build a console application that calls these functions.</span></span>


```C++
#include "stdafx.h"
#include <windows.h>
#include <realtimeapiset.h>

void InterruptTimeTest()
{
    ULONGLONG InterruptTime;
    ULONGLONG PreciseInterruptTime;
    ULONGLONG UnbiasedInterruptTime;
    ULONGLONG PreciseUnbiasedInterruptTime;

        // The interrupt time that QueryInterruptTime reports is based on the 
        // latest tick of the system clock timer. The system clock timer is 
        // the hardware timer that periodically generates interrupts for the 
        // system clock. The uniform period between system clock timer 
        // interrupts is referred to as a system clock tick, and is typically 
        // in the range of 0.5 milliseconds to 15.625 milliseconds, depending 
        // on the hardware platform. The interrupt time value retrieved by 
        // QueryInterruptTime is accurate within a system clock tick.

    QueryInterruptTime(&InterruptTime);
    printf("Interrupt time: %.7f seconds\n", 
            (double)InterruptTime/(double)10000000);

        // Precise interrupt time is more precise than the interrupt time that
        // QueryInterruptTime reports because the functions that report  
        // precise interrupt time read the timer hardware directly.

    QueryInterruptTimePrecise(&PreciseInterruptTime);
    printf("Precise interrupt time: %.7f seconds\n", 
            (double)PreciseInterruptTime/(double)10000000);

        // Unbiased interrupt time means that only time that the system is in 
        // the working state is counted. Therefore, the interrupt-time count 
        // is not biased by time the system spends in sleep or hibernation.

    QueryUnbiasedInterruptTime(&UnbiasedInterruptTime);
    printf("Unbiased interrupt time: %.7f seconds\n", 
            (double)UnbiasedInterruptTime/(double)10000000);

        // QueryUnbiasedInterruptTimePrecise gets an interrupt-time count
        // that is both unbiased and precise, as defined in the comments
        // included earlier in this example.

    QueryUnbiasedInterruptTimePrecise(&PreciseUnbiasedInterruptTime);
    printf("Precise unbiased interrupt time: %.7f seconds\n", 
            (double)PreciseUnbiasedInterruptTime/(double)10000000);

}

int main(void)
{
    void InterruptTimeTime();

    InterruptTimeTest();
    return(0);
}
```



<span data-ttu-id="263a2-121">Para recuperar el tiempo transcurrido que cuentas para la suspensión o hibernación, use la función [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) , o use el contador de rendimiento del sistema de tiempo de actividad.</span><span class="sxs-lookup"><span data-stu-id="263a2-121">To retrieve elapsed time that accounts for sleep or hibernation, use the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) or [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) function, or use the System Up Time performance counter.</span></span> <span data-ttu-id="263a2-122">Este contador de rendimiento se puede recuperar de los datos de rendimiento en la clave del registro **HKEY \_ performance \_ Data**.</span><span class="sxs-lookup"><span data-stu-id="263a2-122">This performance counter can be retrieved from the performance data in the registry key **HKEY\_PERFORMANCE\_DATA**.</span></span> <span data-ttu-id="263a2-123">El valor devuelto es un valor de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="263a2-123">The value returned is an 8-byte value.</span></span> <span data-ttu-id="263a2-124">Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="263a2-124">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

## <a name="related-topics"></a><span data-ttu-id="263a2-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="263a2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="263a2-126">**QueryInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="263a2-126">**QueryInterruptTime**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)
</dt> <dt>

[<span data-ttu-id="263a2-127">**QueryInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="263a2-127">**QueryInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="263a2-128">**QueryUnbiasedInterruptTime**</span><span class="sxs-lookup"><span data-stu-id="263a2-128">**QueryUnbiasedInterruptTime**</span></span>](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)
</dt> <dt>

[<span data-ttu-id="263a2-129">**QueryUnbiasedInterruptTimePrecise**</span><span class="sxs-lookup"><span data-stu-id="263a2-129">**QueryUnbiasedInterruptTimePrecise**</span></span>](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)
</dt> <dt>

[<span data-ttu-id="263a2-130">**timeBeginPeriod**</span><span class="sxs-lookup"><span data-stu-id="263a2-130">**timeBeginPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timebeginperiod)
</dt> <dt>

[<span data-ttu-id="263a2-131">**timeEndPeriod**</span><span class="sxs-lookup"><span data-stu-id="263a2-131">**timeEndPeriod**</span></span>](/windows/desktop/api/timeapi/nf-timeapi-timeendperiod)
</dt> </dl>

 

 
