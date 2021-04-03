---
title: MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03 (clase)
description: La \_ clase ApplicationLaunchRestrictions01 EXE03 de AppLocker de MDM \_ \_ le permite especificar qué aplicaciones exe se pueden iniciar.
ms.assetid: 27f10b5c-bc3b-4344-afcf-5718ea13e909
keywords:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03 (clase)
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58aeb86edc21fec974c099fd8d25bd2e3fb244ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905168"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_exe03-class"></a><span data-ttu-id="c0ee1-105">MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ clase EXE03</span><span class="sxs-lookup"><span data-stu-id="c0ee1-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03 class</span></span>

<span data-ttu-id="c0ee1-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c0ee1-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c0ee1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c0ee1-108">La **clase \_ \_ ApplicationLaunchRestrictions01 \_ EXE03 de AppLocker de MDM** le permite especificar qué aplicaciones exe se pueden iniciar.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class allows you to specify which EXE applications are allowed to launch.</span></span>

<span data-ttu-id="c0ee1-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ee1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0ee1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="c0ee1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0ee1-111">Members</span></span>

<span data-ttu-id="c0ee1-112">La **clase \_ \_ ApplicationLaunchRestrictions01 de \_ EXE03 de AppLocker de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c0ee1-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="c0ee1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0ee1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0ee1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0ee1-114">Properties</span></span>

<span data-ttu-id="c0ee1-115">La **clase \_ \_ ApplicationLaunchRestrictions01 \_ EXE03 de AppLocker de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_EXE03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c0ee1-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ee1-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ee1-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0ee1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0ee1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ee1-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ee1-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0ee1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0ee1-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0ee1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0ee1-123">Define las restricciones para iniciar aplicaciones ejecutables.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-123">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

[<span data-ttu-id="c0ee1-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ee1-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ee1-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0ee1-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0ee1-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ee1-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ee1-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0ee1-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0ee1-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0ee1-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0ee1-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c0ee1-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="c0ee1-132">Para esta clase, la cadena es "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*".</span><span class="sxs-lookup"><span data-stu-id="c0ee1-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="c0ee1-133">**Directiva**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ee1-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0ee1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0ee1-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0ee1-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0ee1-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0ee1-136">Requirements</span></span>



| <span data-ttu-id="c0ee1-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0ee1-137">Requirement</span></span> | <span data-ttu-id="c0ee1-138">Value</span><span class="sxs-lookup"><span data-stu-id="c0ee1-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ee1-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0ee1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ee1-140">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0ee1-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0ee1-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0ee1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ee1-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c0ee1-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c0ee1-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c0ee1-143">Namespace</span></span><br/>                | <span data-ttu-id="c0ee1-144">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="c0ee1-144">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c0ee1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="c0ee1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0ee1-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0ee1-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0ee1-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0ee1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0ee1-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ee1-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ee1-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0ee1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ee1-150">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="c0ee1-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

