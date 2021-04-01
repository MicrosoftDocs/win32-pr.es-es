---
title: MDM_Policy_Result01_AboveLock02 (clase)
description: La \_ clase Result01 de AboveLock02 de directivas MDM \_ \_ representa las directivas que determinan las acciones que se permiten sobre la pantalla de bloqueo del dispositivo.
ms.assetid: 0b6d4083-2484-450b-9261-5ef339db4707
keywords:
- MDM_Policy_Result01_AboveLock02 (clase)
- MDM_Policy_Result01_AboveLock02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AboveLock02
- MDM_Policy_Result01_AboveLock02.InstanceID
- MDM_Policy_Result01_AboveLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530ed3c4afd3b6e888ee77d0963881c2b4d5ef93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996454"
---
# <a name="mdm_policy_result01_abovelock02-class"></a><span data-ttu-id="422c5-105">\_ \_ Clase AboveLock02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="422c5-105">MDM\_Policy\_Result01\_AboveLock02 class</span></span>

<span data-ttu-id="422c5-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="422c5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="422c5-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="422c5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="422c5-108">La **clase \_ \_ Result01 de \_ AboveLock02 de directivas MDM** representa las directivas que determinan las acciones que se permiten sobre la pantalla de bloqueo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="422c5-108">The **MDM\_Policy\_Result01\_AboveLock02** class represents policies that determine actions that are allowed above the Device Lock screen.</span></span>

<span data-ttu-id="422c5-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="422c5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="422c5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="422c5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AboveLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowToasts;
  sint32 AllowCortanaAboveLock;
};
```

## <a name="members"></a><span data-ttu-id="422c5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="422c5-111">Members</span></span>

<span data-ttu-id="422c5-112">La clase Result01 de la **\_ Directiva MDM \_ \_ AboveLock02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="422c5-112">The **MDM\_Policy\_Result01\_AboveLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="422c5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="422c5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="422c5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="422c5-114">Properties</span></span>

<span data-ttu-id="422c5-115">La **clase \_ \_ Result01 de \_ AboveLock02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="422c5-115">The **MDM\_Policy\_Result01\_AboveLock02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="422c5-116">AllowCortanaAboveLock</span><span class="sxs-lookup"><span data-stu-id="422c5-116">AllowCortanaAboveLock</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowcortanaabovelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="422c5-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="422c5-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="422c5-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="422c5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="422c5-119">AllowToasts</span><span class="sxs-lookup"><span data-stu-id="422c5-119">AllowToasts</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="422c5-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="422c5-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="422c5-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="422c5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="422c5-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="422c5-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="422c5-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="422c5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="422c5-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="422c5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="422c5-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="422c5-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="422c5-126">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="422c5-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="422c5-127">Para esta clase, la cadena es "AboveLock".</span><span class="sxs-lookup"><span data-stu-id="422c5-127">For this class, the string is "AboveLock".</span></span>

</dd> <dt>

<span data-ttu-id="422c5-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="422c5-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="422c5-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="422c5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="422c5-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="422c5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="422c5-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="422c5-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="422c5-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="422c5-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="422c5-133">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="422c5-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="422c5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="422c5-134">Requirements</span></span>



| <span data-ttu-id="422c5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="422c5-135">Requirement</span></span> | <span data-ttu-id="422c5-136">Value</span><span class="sxs-lookup"><span data-stu-id="422c5-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="422c5-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="422c5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="422c5-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="422c5-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="422c5-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="422c5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="422c5-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="422c5-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="422c5-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="422c5-141">Namespace</span></span><br/>                | <span data-ttu-id="422c5-142">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="422c5-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="422c5-143">MOF</span><span class="sxs-lookup"><span data-stu-id="422c5-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="422c5-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="422c5-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="422c5-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="422c5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="422c5-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="422c5-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="422c5-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="422c5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422c5-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="422c5-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

