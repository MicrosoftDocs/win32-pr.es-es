---
title: MDM_Policy_Result01_Security02 (clase)
description: La \_ clase Result01 de Security02 de directivas MDM \_ \_ representa las directivas de seguridad disponibles.
ms.assetid: e4f9bbeb-b542-454d-930b-0b4ac88fe189
keywords:
- MDM_Policy_Result01_Security02 (clase)
- MDM_Policy_Result01_Security02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Security02
- MDM_Policy_Result01_Security02.InstanceID
- MDM_Policy_Result01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 959d5cbc9382b4bef0899f5b44d8ee2d171bd704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079172"
---
# <a name="mdm_policy_result01_security02-class"></a><span data-ttu-id="ff038-105">\_ \_ Clase Security02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="ff038-105">MDM\_Policy\_Result01\_Security02 class</span></span>

<span data-ttu-id="ff038-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ff038-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ff038-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ff038-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ff038-108">La **clase \_ \_ Result01 de \_ Security02 de directivas MDM** representa las directivas de seguridad disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff038-108">The **MDM\_Policy\_Result01\_Security02** class represents the security policies available.</span></span>

<span data-ttu-id="ff038-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ff038-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff038-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff038-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Security02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddProvisioningPackage;
  sint32 AllowRemoveProvisioningPackage;
  sint32 ClearTPMIfNotReady;
  sint32 PreventAutomaticDeviceEncryptionForAzureADJoinedDevices;
  sint32 RequireDeviceEncryption;
  sint32 RequireProvisioningPackageSignature;
  sint32 RequireRetrieveHealthCertificateOnBoot;
};
```

## <a name="members"></a><span data-ttu-id="ff038-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff038-111">Members</span></span>

<span data-ttu-id="ff038-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Security02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ff038-112">The **MDM\_Policy\_Result01\_Security02** class has these types of members:</span></span>

-   [<span data-ttu-id="ff038-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff038-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff038-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff038-114">Properties</span></span>

<span data-ttu-id="ff038-115">La **clase \_ \_ Result01 de \_ Security02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ff038-115">The **MDM\_Policy\_Result01\_Security02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ff038-116">AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="ff038-116">AllowAddProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ff038-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ff038-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ff038-119">AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="ff038-119">AllowRemoveProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ff038-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ff038-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ff038-122">ClearTPMIfNotReady</span><span class="sxs-lookup"><span data-stu-id="ff038-122">ClearTPMIfNotReady</span></span>](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ff038-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ff038-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ff038-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ff038-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff038-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff038-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff038-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ff038-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ff038-129">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ff038-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="ff038-130">Para esta clase, la cadena es "Security".</span><span class="sxs-lookup"><span data-stu-id="ff038-130">For this class, the string is "Security".</span></span>

</dd> <dt>

<span data-ttu-id="ff038-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ff038-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff038-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff038-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff038-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ff038-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ff038-135">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ff038-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="ff038-136">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="ff038-136">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="ff038-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span><span class="sxs-lookup"><span data-stu-id="ff038-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span></span>](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ff038-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ff038-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ff038-140">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="ff038-140">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ff038-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ff038-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ff038-143">RequireProvisioningPackageSignature</span><span class="sxs-lookup"><span data-stu-id="ff038-143">RequireProvisioningPackageSignature</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ff038-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ff038-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ff038-146">RequireRetrieveHealthCertificateOnBoot</span><span class="sxs-lookup"><span data-stu-id="ff038-146">RequireRetrieveHealthCertificateOnBoot</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff038-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ff038-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff038-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ff038-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff038-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff038-149">Requirements</span></span>



| <span data-ttu-id="ff038-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff038-150">Requirement</span></span> | <span data-ttu-id="ff038-151">Value</span><span class="sxs-lookup"><span data-stu-id="ff038-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff038-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff038-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ff038-153">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff038-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff038-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff038-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ff038-155">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ff038-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ff038-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ff038-156">Namespace</span></span><br/>                | <span data-ttu-id="ff038-157">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="ff038-157">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ff038-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ff038-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff038-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff038-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff038-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff038-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff038-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff038-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff038-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff038-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff038-163">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="ff038-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

