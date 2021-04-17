---
description: Escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor de la clase Win32_Service (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82c08f9c560a1d8e419d9a8f6474f8ea9db4e541
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659752"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="0818a-103">Método SetSecurityDescriptor de la clase Win32_Service (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0818a-103">SetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0818a-104">El método **SetSecurityDescriptor** escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="0818a-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0818a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0818a-105">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="0818a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0818a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0818a-107">*Descriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0818a-107">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0818a-108">Descriptor de seguridad asociado al servicio.</span><span class="sxs-lookup"><span data-stu-id="0818a-108">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0818a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0818a-109">Return value</span></span>

<span data-ttu-id="0818a-110">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="0818a-110">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="0818a-111">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0818a-111">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0818a-112">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0818a-112">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0818a-113">**Success**</span><span class="sxs-lookup"><span data-stu-id="0818a-113">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-114">0</span><span class="sxs-lookup"><span data-stu-id="0818a-114">0</span></span>

<span data-ttu-id="0818a-115">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0818a-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-116">**1**</span><span class="sxs-lookup"><span data-stu-id="0818a-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-117">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0818a-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-118">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="0818a-118">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-119">2</span><span class="sxs-lookup"><span data-stu-id="0818a-119">2</span></span>

<span data-ttu-id="0818a-120">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="0818a-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-121">**3**</span><span class="sxs-lookup"><span data-stu-id="0818a-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-122">No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.</span><span class="sxs-lookup"><span data-stu-id="0818a-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-123">**4**</span><span class="sxs-lookup"><span data-stu-id="0818a-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-124">El código de control solicitado no es válido o no es aceptable para el servicio.</span><span class="sxs-lookup"><span data-stu-id="0818a-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-125">**5**</span><span class="sxs-lookup"><span data-stu-id="0818a-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-126">El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="0818a-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-127">**6**</span><span class="sxs-lookup"><span data-stu-id="0818a-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-128">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="0818a-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-129">**7**</span><span class="sxs-lookup"><span data-stu-id="0818a-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-130">El servicio no respondió a tiempo a la solicitud de inicio.</span><span class="sxs-lookup"><span data-stu-id="0818a-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-131">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="0818a-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-132">8</span><span class="sxs-lookup"><span data-stu-id="0818a-132">8</span></span>

<span data-ttu-id="0818a-133">Error desconocido al iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="0818a-133">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-134">**Falta el privilegio**</span><span class="sxs-lookup"><span data-stu-id="0818a-134">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-135">9</span><span class="sxs-lookup"><span data-stu-id="0818a-135">9</span></span>

<span data-ttu-id="0818a-136">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="0818a-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-137">**10**</span><span class="sxs-lookup"><span data-stu-id="0818a-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-138">El servicio ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="0818a-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-139">**11**</span><span class="sxs-lookup"><span data-stu-id="0818a-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-140">La base de datos para agregar un nuevo servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="0818a-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-141">**12**</span><span class="sxs-lookup"><span data-stu-id="0818a-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-142">Una dependencia de la que depende este servicio se ha quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="0818a-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-143">**13**</span><span class="sxs-lookup"><span data-stu-id="0818a-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-144">El servicio no pudo encontrar el servicio necesario de un servicio dependiente.</span><span class="sxs-lookup"><span data-stu-id="0818a-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-145">**14**</span><span class="sxs-lookup"><span data-stu-id="0818a-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-146">El servicio se ha deshabilitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="0818a-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-147">**15**</span><span class="sxs-lookup"><span data-stu-id="0818a-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-148">El servicio no tiene la autenticación correcta para ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0818a-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-149">**16**</span><span class="sxs-lookup"><span data-stu-id="0818a-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-150">Este servicio se está quitando del sistema.</span><span class="sxs-lookup"><span data-stu-id="0818a-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-151">**17**</span><span class="sxs-lookup"><span data-stu-id="0818a-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-152">El servicio no tiene ningún subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="0818a-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-153">**18**</span><span class="sxs-lookup"><span data-stu-id="0818a-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-154">El servicio tiene dependencias circulares al iniciarse.</span><span class="sxs-lookup"><span data-stu-id="0818a-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-155">**19**</span><span class="sxs-lookup"><span data-stu-id="0818a-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-156">Se está ejecutando un servicio con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="0818a-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-157">**20**</span><span class="sxs-lookup"><span data-stu-id="0818a-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-158">El nombre del servicio tiene caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="0818a-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-159">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="0818a-159">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-160">21</span><span class="sxs-lookup"><span data-stu-id="0818a-160">21</span></span>

<span data-ttu-id="0818a-161">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="0818a-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-162">**22**</span><span class="sxs-lookup"><span data-stu-id="0818a-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-163">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="0818a-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-164">**23**</span><span class="sxs-lookup"><span data-stu-id="0818a-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-165">El servicio existe en la base de datos de servicios disponibles del sistema.</span><span class="sxs-lookup"><span data-stu-id="0818a-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-166">**24**</span><span class="sxs-lookup"><span data-stu-id="0818a-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-167">El servicio se encuentra en pausa actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0818a-167">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="0818a-168">**Otros**</span><span class="sxs-lookup"><span data-stu-id="0818a-168">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="0818a-169">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="0818a-169">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0818a-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0818a-170">Remarks</span></span>

<span data-ttu-id="0818a-171">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="0818a-171">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="0818a-172">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="0818a-172">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="0818a-173">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="0818a-173">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="0818a-174">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="0818a-174">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="0818a-175">Puede actualizar la DACL y la SACL en la instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o la SACL.</span><span class="sxs-lookup"><span data-stu-id="0818a-175">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="0818a-176">Los valores siguientes en [**el \_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualiza la DACL, la SACL o ambas.</span><span class="sxs-lookup"><span data-stu-id="0818a-176">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="0818a-177">**DACL de SE \_ \_ presente**</span><span class="sxs-lookup"><span data-stu-id="0818a-177">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="0818a-178">Indica que se debe actualizar la DACL.</span><span class="sxs-lookup"><span data-stu-id="0818a-178">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="0818a-179">Si no se establece, WMI conserva el valor original de la DACL.</span><span class="sxs-lookup"><span data-stu-id="0818a-179">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="0818a-180">**la \_ SACL de se \_ presente**</span><span class="sxs-lookup"><span data-stu-id="0818a-180">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="0818a-181">Indica que se debe actualizar la SACL.</span><span class="sxs-lookup"><span data-stu-id="0818a-181">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="0818a-182">Si no se establece, WMI conserva el valor original de la SACL.</span><span class="sxs-lookup"><span data-stu-id="0818a-182">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="0818a-183">Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="0818a-183">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="0818a-184">En el caso de scripting, el nombre del privilegio es **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="0818a-184">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="0818a-185">Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="0818a-185">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="0818a-186">Si el administrador de confianza del grupo y las propiedades del administrador del propietario no son **nulos**, se actualizan.</span><span class="sxs-lookup"><span data-stu-id="0818a-186">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="0818a-187">De lo contrario, WMI conserva los valores originales.</span><span class="sxs-lookup"><span data-stu-id="0818a-187">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="0818a-188">Para obtener más información, vea [objetos de descriptor de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="0818a-188">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="0818a-189">Cuando una nueva SACL es **null** en una llamada a este método, la SACL del descriptor de seguridad del objeto protegible de destino permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="0818a-189">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="0818a-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0818a-190">Requirements</span></span>



| <span data-ttu-id="0818a-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="0818a-191">Requirement</span></span> | <span data-ttu-id="0818a-192">Value</span><span class="sxs-lookup"><span data-stu-id="0818a-192">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0818a-193">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0818a-193">Minimum supported client</span></span><br/> | <span data-ttu-id="0818a-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0818a-194">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0818a-195">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0818a-195">Minimum supported server</span></span><br/> | <span data-ttu-id="0818a-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0818a-196">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0818a-197">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0818a-197">Namespace</span></span><br/>                | <span data-ttu-id="0818a-198">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0818a-198">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0818a-199">MOF</span><span class="sxs-lookup"><span data-stu-id="0818a-199">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0818a-200"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0818a-200"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0818a-201">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0818a-201">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0818a-202"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0818a-202"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0818a-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="0818a-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0818a-204">**\_Servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="0818a-204">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="0818a-205">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="0818a-205">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="0818a-206">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="0818a-206">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="0818a-207">Cambiar la seguridad de acceso en objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="0818a-207">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="0818a-208">Control de cuentas de usuario y WMI</span><span class="sxs-lookup"><span data-stu-id="0818a-208">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

