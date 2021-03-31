---
description: El método estático de la clase WMI SetDeadGWDetect se usa para habilitar la detección de puerta de enlace inactiva.
ms.assetid: c813aaef-7215-4759-b68f-7808fd203d9c
ms.tgt_platform: multiple
title: Método SetDeadGWDetect de la clase Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDeadGWDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f62d84af193be99850f1a82b720a2983ca77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495994"
---
# <a name="setdeadgwdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="dae7b-103">Método SetDeadGWDetect de la \_ clase NetworkAdapterConfiguration de Win32</span><span class="sxs-lookup"><span data-stu-id="dae7b-103">SetDeadGWDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="dae7b-104">El método estático de la [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDeadGWDetect** se usa para habilitar la detección de puerta de enlace inactiva.</span><span class="sxs-lookup"><span data-stu-id="dae7b-104">The **SetDeadGWDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable dead gateway detection.</span></span>

<span data-ttu-id="dae7b-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dae7b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dae7b-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dae7b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dae7b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dae7b-107">Syntax</span></span>


```mof
uint32 SetDeadGWDetect(
  [in] boolean DeadGWDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="dae7b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dae7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae7b-109">*DeadGWDetectEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dae7b-109">*DeadGWDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-110">Si **es true**, la detección de puerta de enlace inactiva debe estar habilitada.</span><span class="sxs-lookup"><span data-stu-id="dae7b-110">If **true**, dead gateway detection should be enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae7b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dae7b-111">Return value</span></span>

<span data-ttu-id="dae7b-112">Devuelve un valor de 0 (cero) para una finalización correcta cuando no se requiere reinicio, 1 (uno) para una finalización correcta cuando se requiere un reinicio, y un número diferente si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="dae7b-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="dae7b-113">Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="dae7b-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="dae7b-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="dae7b-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="dae7b-115">**Finalización correcta, no se requiere ningún reinicio**</span><span class="sxs-lookup"><span data-stu-id="dae7b-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-116">0</span><span class="sxs-lookup"><span data-stu-id="dae7b-116">0</span></span>

<span data-ttu-id="dae7b-117">Finalización correcta, no es necesario reiniciar.</span><span class="sxs-lookup"><span data-stu-id="dae7b-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-118">**Finalización correcta, se requiere un reinicio**</span><span class="sxs-lookup"><span data-stu-id="dae7b-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-119">1</span><span class="sxs-lookup"><span data-stu-id="dae7b-119">1</span></span>

<span data-ttu-id="dae7b-120">Finalización correcta, se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="dae7b-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-121">**Método no admitido en esta plataforma**</span><span class="sxs-lookup"><span data-stu-id="dae7b-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-122">64</span><span class="sxs-lookup"><span data-stu-id="dae7b-122">64</span></span>

<span data-ttu-id="dae7b-123">El método no se admite en esta plataforma.</span><span class="sxs-lookup"><span data-stu-id="dae7b-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-124">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="dae7b-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-125">65</span><span class="sxs-lookup"><span data-stu-id="dae7b-125">65</span></span>

<span data-ttu-id="dae7b-126">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="dae7b-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-127">**Máscara de subred no válida**</span><span class="sxs-lookup"><span data-stu-id="dae7b-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-128">66</span><span class="sxs-lookup"><span data-stu-id="dae7b-128">66</span></span>

<span data-ttu-id="dae7b-129">Máscara de subred no válida.</span><span class="sxs-lookup"><span data-stu-id="dae7b-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-130">**Se produjo un error al procesar una instancia devuelta**</span><span class="sxs-lookup"><span data-stu-id="dae7b-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-131">67</span><span class="sxs-lookup"><span data-stu-id="dae7b-131">67</span></span>

<span data-ttu-id="dae7b-132">Se produjo un error al procesar una instancia devuelta.</span><span class="sxs-lookup"><span data-stu-id="dae7b-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-133">**Parámetro de entrada no válido**</span><span class="sxs-lookup"><span data-stu-id="dae7b-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-134">68</span><span class="sxs-lookup"><span data-stu-id="dae7b-134">68</span></span>

<span data-ttu-id="dae7b-135">Parámetro de entrada no válido.</span><span class="sxs-lookup"><span data-stu-id="dae7b-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-136">**Se especificaron más de 5 puertas de enlace**</span><span class="sxs-lookup"><span data-stu-id="dae7b-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-137">69</span><span class="sxs-lookup"><span data-stu-id="dae7b-137">69</span></span>

<span data-ttu-id="dae7b-138">Se han especificado más de cinco puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="dae7b-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-139">**Dirección IP no válida**</span><span class="sxs-lookup"><span data-stu-id="dae7b-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-140">70</span><span class="sxs-lookup"><span data-stu-id="dae7b-140">70</span></span>

<span data-ttu-id="dae7b-141">Dirección IP no válida.</span><span class="sxs-lookup"><span data-stu-id="dae7b-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-142">**Dirección IP de puerta de enlace no válida**</span><span class="sxs-lookup"><span data-stu-id="dae7b-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-143">71</span><span class="sxs-lookup"><span data-stu-id="dae7b-143">71</span></span>

<span data-ttu-id="dae7b-144">Dirección IP de puerta de enlace no válida.</span><span class="sxs-lookup"><span data-stu-id="dae7b-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-145">**Se produjo un error al obtener acceso al registro para obtener la información solicitada.**</span><span class="sxs-lookup"><span data-stu-id="dae7b-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-146">72</span><span class="sxs-lookup"><span data-stu-id="dae7b-146">72</span></span>

<span data-ttu-id="dae7b-147">Error al obtener acceso al registro para obtener la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="dae7b-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-148">**Nombre de dominio no válido**</span><span class="sxs-lookup"><span data-stu-id="dae7b-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-149">73</span><span class="sxs-lookup"><span data-stu-id="dae7b-149">73</span></span>

<span data-ttu-id="dae7b-150">Nombre de dominio no válido.</span><span class="sxs-lookup"><span data-stu-id="dae7b-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-151">**Nombre de host no válido**</span><span class="sxs-lookup"><span data-stu-id="dae7b-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-152">74</span><span class="sxs-lookup"><span data-stu-id="dae7b-152">74</span></span>

<span data-ttu-id="dae7b-153">Nombre de host no válido.</span><span class="sxs-lookup"><span data-stu-id="dae7b-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-154">**No hay definido ningún servidor WINS principal/secundario**</span><span class="sxs-lookup"><span data-stu-id="dae7b-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-155">75</span><span class="sxs-lookup"><span data-stu-id="dae7b-155">75</span></span>

<span data-ttu-id="dae7b-156">No hay definido ningún servidor WINS principal ni secundario.</span><span class="sxs-lookup"><span data-stu-id="dae7b-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-157">**Archivo no válido**</span><span class="sxs-lookup"><span data-stu-id="dae7b-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-158">76</span><span class="sxs-lookup"><span data-stu-id="dae7b-158">76</span></span>

<span data-ttu-id="dae7b-159">Archivo no válido.</span><span class="sxs-lookup"><span data-stu-id="dae7b-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-160">**Ruta de acceso del sistema no válida**</span><span class="sxs-lookup"><span data-stu-id="dae7b-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-161">77</span><span class="sxs-lookup"><span data-stu-id="dae7b-161">77</span></span>

<span data-ttu-id="dae7b-162">Ruta de acceso del sistema no válida.</span><span class="sxs-lookup"><span data-stu-id="dae7b-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-163">**No se pudo copiar el archivo**</span><span class="sxs-lookup"><span data-stu-id="dae7b-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-164">78</span><span class="sxs-lookup"><span data-stu-id="dae7b-164">78</span></span>

<span data-ttu-id="dae7b-165">No se pudo copiar el archivo.</span><span class="sxs-lookup"><span data-stu-id="dae7b-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-166">**Parámetro de seguridad no válido**</span><span class="sxs-lookup"><span data-stu-id="dae7b-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-167">79</span><span class="sxs-lookup"><span data-stu-id="dae7b-167">79</span></span>

<span data-ttu-id="dae7b-168">Parámetro de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="dae7b-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-169">**No se puede configurar el servicio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="dae7b-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-170">80</span><span class="sxs-lookup"><span data-stu-id="dae7b-170">80</span></span>

<span data-ttu-id="dae7b-171">No se puede configurar el servicio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="dae7b-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-172">**No se puede configurar el servicio DHCP**</span><span class="sxs-lookup"><span data-stu-id="dae7b-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-173">81</span><span class="sxs-lookup"><span data-stu-id="dae7b-173">81</span></span>

<span data-ttu-id="dae7b-174">No se puede configurar el servicio DHCP.</span><span class="sxs-lookup"><span data-stu-id="dae7b-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-175">**No se puede renovar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="dae7b-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-176">82</span><span class="sxs-lookup"><span data-stu-id="dae7b-176">82</span></span>

<span data-ttu-id="dae7b-177">No se puede renovar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="dae7b-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-178">**No se puede liberar la concesión DHCP**</span><span class="sxs-lookup"><span data-stu-id="dae7b-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-179">83</span><span class="sxs-lookup"><span data-stu-id="dae7b-179">83</span></span>

<span data-ttu-id="dae7b-180">No se puede liberar la concesión DHCP.</span><span class="sxs-lookup"><span data-stu-id="dae7b-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-181">**IP no habilitada en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="dae7b-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-182">84</span><span class="sxs-lookup"><span data-stu-id="dae7b-182">84</span></span>

<span data-ttu-id="dae7b-183">IP no habilitada en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="dae7b-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-184">**IPX no habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="dae7b-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-185">85</span><span class="sxs-lookup"><span data-stu-id="dae7b-185">85</span></span>

<span data-ttu-id="dae7b-186">IPX no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="dae7b-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-187">**Error de límite de número de trama/red**</span><span class="sxs-lookup"><span data-stu-id="dae7b-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-188">86</span><span class="sxs-lookup"><span data-stu-id="dae7b-188">86</span></span>

<span data-ttu-id="dae7b-189">Error de límite de número de trama o de red.</span><span class="sxs-lookup"><span data-stu-id="dae7b-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-190">**Tipo de marco no válido**</span><span class="sxs-lookup"><span data-stu-id="dae7b-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-191">87</span><span class="sxs-lookup"><span data-stu-id="dae7b-191">87</span></span>

<span data-ttu-id="dae7b-192">Tipo de marco no válido.</span><span class="sxs-lookup"><span data-stu-id="dae7b-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-193">**Número de red no válido**</span><span class="sxs-lookup"><span data-stu-id="dae7b-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-194">88</span><span class="sxs-lookup"><span data-stu-id="dae7b-194">88</span></span>

<span data-ttu-id="dae7b-195">Número de red no válido.</span><span class="sxs-lookup"><span data-stu-id="dae7b-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-196">**Número de red duplicado**</span><span class="sxs-lookup"><span data-stu-id="dae7b-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-197">89</span><span class="sxs-lookup"><span data-stu-id="dae7b-197">89</span></span>

<span data-ttu-id="dae7b-198">Número de red duplicado.</span><span class="sxs-lookup"><span data-stu-id="dae7b-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-199">**Parámetro fuera de los límites**</span><span class="sxs-lookup"><span data-stu-id="dae7b-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-200">90</span><span class="sxs-lookup"><span data-stu-id="dae7b-200">90</span></span>

<span data-ttu-id="dae7b-201">Parámetro fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="dae7b-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-202">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="dae7b-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-203">91</span><span class="sxs-lookup"><span data-stu-id="dae7b-203">91</span></span>

<span data-ttu-id="dae7b-204">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="dae7b-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-205">**Memoria agotada**</span><span class="sxs-lookup"><span data-stu-id="dae7b-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-206">92</span><span class="sxs-lookup"><span data-stu-id="dae7b-206">92</span></span>

<span data-ttu-id="dae7b-207">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="dae7b-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-208">**Ya existe**</span><span class="sxs-lookup"><span data-stu-id="dae7b-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-209">93</span><span class="sxs-lookup"><span data-stu-id="dae7b-209">93</span></span>

<span data-ttu-id="dae7b-210">Ya existe.</span><span class="sxs-lookup"><span data-stu-id="dae7b-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-211">**Ruta de acceso, archivo u objeto no encontrado**</span><span class="sxs-lookup"><span data-stu-id="dae7b-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-212">94</span><span class="sxs-lookup"><span data-stu-id="dae7b-212">94</span></span>

<span data-ttu-id="dae7b-213">No se encuentra la ruta de acceso, el archivo o el objeto.</span><span class="sxs-lookup"><span data-stu-id="dae7b-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-214">**No se puede notificar al servicio**</span><span class="sxs-lookup"><span data-stu-id="dae7b-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-215">95</span><span class="sxs-lookup"><span data-stu-id="dae7b-215">95</span></span>

<span data-ttu-id="dae7b-216">No se puede notificar al servicio.</span><span class="sxs-lookup"><span data-stu-id="dae7b-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-217">**No se puede notificar al servicio DNS**</span><span class="sxs-lookup"><span data-stu-id="dae7b-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-218">96</span><span class="sxs-lookup"><span data-stu-id="dae7b-218">96</span></span>

<span data-ttu-id="dae7b-219">No se puede notificar al servicio DNS.</span><span class="sxs-lookup"><span data-stu-id="dae7b-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-220">**Interfaz no configurable**</span><span class="sxs-lookup"><span data-stu-id="dae7b-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-221">97</span><span class="sxs-lookup"><span data-stu-id="dae7b-221">97</span></span>

<span data-ttu-id="dae7b-222">Interfaz no configurable.</span><span class="sxs-lookup"><span data-stu-id="dae7b-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-223">**No se pudieron liberar o renovar todas las concesiones DHCP**</span><span class="sxs-lookup"><span data-stu-id="dae7b-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-224">98</span><span class="sxs-lookup"><span data-stu-id="dae7b-224">98</span></span>

<span data-ttu-id="dae7b-225">No todas las concesiones DHCP se pueden liberar o renovar.</span><span class="sxs-lookup"><span data-stu-id="dae7b-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-226">**DHCP no está habilitado en el adaptador**</span><span class="sxs-lookup"><span data-stu-id="dae7b-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-227">100</span><span class="sxs-lookup"><span data-stu-id="dae7b-227">100</span></span>

<span data-ttu-id="dae7b-228">DHCP no está habilitado en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="dae7b-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="dae7b-229">**Otros**</span><span class="sxs-lookup"><span data-stu-id="dae7b-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="dae7b-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="dae7b-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dae7b-231">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dae7b-231">Remarks</span></span>

<span data-ttu-id="dae7b-232">Con esta característica habilitada, TCP pide a IP que cambie a una puerta de enlace de copia de seguridad si retransmite un segmento varias veces sin recibir una respuesta.</span><span class="sxs-lookup"><span data-stu-id="dae7b-232">With this feature enabled, TCP asks IP to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

## <a name="examples"></a><span data-ttu-id="dae7b-233">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dae7b-233">Examples</span></span>

<span data-ttu-id="dae7b-234">En el ejemplo de VBScript [Habilitar detección de puerta de enlace inactiva para todos los adaptadores de red](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) de la galería de TechNet se usa **SetDeadGWDetect** para configurar todos los adaptadores de red de un equipo para detectar automáticamente las puertas de enlace inactivas.</span><span class="sxs-lookup"><span data-stu-id="dae7b-234">The [Enable Dead Gateway Detection for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript sample on TechNet Gallery uses **SetDeadGWDetect** to configure all network adapters on a computer to automatically detect dead gateways.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae7b-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae7b-235">Requirements</span></span>



| <span data-ttu-id="dae7b-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae7b-236">Requirement</span></span> | <span data-ttu-id="dae7b-237">Value</span><span class="sxs-lookup"><span data-stu-id="dae7b-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dae7b-238">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dae7b-238">Minimum supported client</span></span><br/> | <span data-ttu-id="dae7b-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dae7b-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dae7b-240">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dae7b-240">Minimum supported server</span></span><br/> | <span data-ttu-id="dae7b-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dae7b-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dae7b-242">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dae7b-242">Namespace</span></span><br/>                | <span data-ttu-id="dae7b-243">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dae7b-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dae7b-244">MOF</span><span class="sxs-lookup"><span data-stu-id="dae7b-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dae7b-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dae7b-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dae7b-246">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dae7b-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dae7b-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dae7b-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae7b-248">Vea también</span><span class="sxs-lookup"><span data-stu-id="dae7b-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae7b-249">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="dae7b-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="dae7b-250">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="dae7b-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="dae7b-251">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="dae7b-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="dae7b-252">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="dae7b-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="dae7b-253">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="dae7b-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

