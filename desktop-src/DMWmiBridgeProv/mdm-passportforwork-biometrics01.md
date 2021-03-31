---
title: MDM_PassportForWork_Biometrics01 (clase)
description: La \_ clase Biometrics01 de MDM PassportForWork \_ define la configuración de biométrica.
ms.assetid: 64012526-eac6-4f01-8665-2bd460bc1b93
keywords:
- MDM_PassportForWork_Biometrics01 (clase)
- MDM_PassportForWork_Biometrics01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01.InstanceID
- MDM_PassportForWork_Biometrics01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132351f17b6f242e39d6e6d6680aa756d5f7b5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150118"
---
# <a name="mdm_passportforwork_biometrics01-class"></a><span data-ttu-id="d6fc0-105">\_Clase Biometrics01 PassportForWork de MDM \_</span><span class="sxs-lookup"><span data-stu-id="d6fc0-105">MDM\_PassportForWork\_Biometrics01 class</span></span>

<span data-ttu-id="d6fc0-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d6fc0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d6fc0-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d6fc0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d6fc0-108">La **clase \_ \_ Biometrics01 de MDM PassportForWork** define la configuración de biométrica.</span><span class="sxs-lookup"><span data-stu-id="d6fc0-108">The **MDM\_PassportForWork\_Biometrics01** class defines biometric settings.</span></span>

<span data-ttu-id="d6fc0-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d6fc0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6fc0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6fc0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Biometrics01
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
  boolean FacialFeaturesUseEnhancedAntiSpoofing;
};
```

## <a name="members"></a><span data-ttu-id="d6fc0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6fc0-111">Members</span></span>

<span data-ttu-id="d6fc0-112">La **clase \_ \_ Biometrics01 de MDM PassportForWork** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6fc0-112">The **MDM\_PassportForWork\_Biometrics01** class has these types of members:</span></span>

-   [<span data-ttu-id="d6fc0-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6fc0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6fc0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6fc0-114">Properties</span></span>

<span data-ttu-id="d6fc0-115">La **clase \_ \_ Biometrics01 de MDM PassportForWork** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d6fc0-115">The **MDM\_PassportForWork\_Biometrics01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d6fc0-116">FacialFeaturesUseEnhancedAntiSpoofing</span><span class="sxs-lookup"><span data-stu-id="d6fc0-116">FacialFeaturesUseEnhancedAntiSpoofing</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc0-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d6fc0-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc0-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d6fc0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d6fc0-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d6fc0-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc0-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d6fc0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc0-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6fc0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6fc0-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d6fc0-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d6fc0-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="d6fc0-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="d6fc0-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d6fc0-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc0-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d6fc0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc0-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6fc0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6fc0-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d6fc0-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d6fc0-128">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="d6fc0-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="d6fc0-129">Para esta clase, la cadena es "./Vendor/MSFT/PassportForWork/".</span><span class="sxs-lookup"><span data-stu-id="d6fc0-129">For this class, the string is "./Vendor/MSFT/PassportForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="d6fc0-130">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="d6fc0-130">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6fc0-131">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d6fc0-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d6fc0-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d6fc0-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6fc0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6fc0-133">Requirements</span></span>



| <span data-ttu-id="d6fc0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6fc0-134">Requirement</span></span> | <span data-ttu-id="d6fc0-135">Value</span><span class="sxs-lookup"><span data-stu-id="d6fc0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fc0-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6fc0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d6fc0-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6fc0-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6fc0-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6fc0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d6fc0-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d6fc0-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d6fc0-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6fc0-140">Namespace</span></span><br/>                | <span data-ttu-id="d6fc0-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="d6fc0-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d6fc0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d6fc0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6fc0-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6fc0-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6fc0-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6fc0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6fc0-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6fc0-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6fc0-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6fc0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fc0-147">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="d6fc0-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

