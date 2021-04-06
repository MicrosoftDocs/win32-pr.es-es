---
title: MDM_Reboot (clase)
description: La Rebootclass de MDM \_ se usa para configurar las opciones de reinicio.
ms.assetid: 876ba854-1c26-49cf-915d-194be9f9c1d4
keywords:
- MDM_Reboot (clase)
- MDM_Reboot clase, descrita
topic_type:
- apiref
api_name:
- MDM_Reboot
- MDM_Reboot.InstanceID
- MDM_Reboot.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e078dfef883db5aad67e7ee834ceca4bd0a942
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078908"
---
# <a name="mdm_reboot-class"></a><span data-ttu-id="56ce4-105">\_Clase de reinicio de MDM</span><span class="sxs-lookup"><span data-stu-id="56ce4-105">MDM\_Reboot class</span></span>

<span data-ttu-id="56ce4-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="56ce4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="56ce4-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="56ce4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="56ce4-108">La clase de **\_ reinicio de MDM** se usa para configurar las opciones de reinicio.</span><span class="sxs-lookup"><span data-stu-id="56ce4-108">The **MDM\_Reboot** class is used to configure reboot settings.</span></span>

<span data-ttu-id="56ce4-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="56ce4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ce4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56ce4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="56ce4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="56ce4-111">Members</span></span>

<span data-ttu-id="56ce4-112">La clase de **\_ reinicio de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="56ce4-112">The **MDM\_Reboot** class has these types of members:</span></span>

-   [<span data-ttu-id="56ce4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="56ce4-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="56ce4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56ce4-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="56ce4-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="56ce4-115">Methods</span></span>

<span data-ttu-id="56ce4-116">La clase de **\_ reinicio de MDM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="56ce4-116">The **MDM\_Reboot** class has these methods.</span></span>



| <span data-ttu-id="56ce4-117">Método</span><span class="sxs-lookup"><span data-stu-id="56ce4-117">Method</span></span>                                                | <span data-ttu-id="56ce4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="56ce4-118">Description</span></span>                                             |
|:------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="56ce4-119">**RebootNowMethod**</span><span class="sxs-lookup"><span data-stu-id="56ce4-119">**RebootNowMethod**</span></span>](mdm-reboot-rebootnowmethod.md) | <span data-ttu-id="56ce4-120">Este método ejecuta un reinicio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56ce4-120">This method executes a reboot of the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="56ce4-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56ce4-121">Properties</span></span>

<span data-ttu-id="56ce4-122">La clase de **\_ reinicio de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="56ce4-122">The **MDM\_Reboot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56ce4-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="56ce4-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56ce4-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56ce4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56ce4-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56ce4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56ce4-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="56ce4-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="56ce4-127">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="56ce4-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="56ce4-128">Para esta clase, la cadena es "Reboot".</span><span class="sxs-lookup"><span data-stu-id="56ce4-128">For this class, the string is "Reboot".</span></span>

</dd> <dt>

<span data-ttu-id="56ce4-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="56ce4-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56ce4-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56ce4-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56ce4-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56ce4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56ce4-132">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="56ce4-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="56ce4-133">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="56ce4-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="56ce4-134">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="56ce4-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56ce4-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56ce4-135">Requirements</span></span>



| <span data-ttu-id="56ce4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ce4-136">Requirement</span></span> | <span data-ttu-id="56ce4-137">Value</span><span class="sxs-lookup"><span data-stu-id="56ce4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ce4-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56ce4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="56ce4-139">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="56ce4-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="56ce4-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56ce4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="56ce4-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="56ce4-141">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="56ce4-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56ce4-142">Namespace</span></span><br/>                | <span data-ttu-id="56ce4-143">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="56ce4-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="56ce4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="56ce4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56ce4-145"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56ce4-145"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="56ce4-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56ce4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56ce4-147"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="56ce4-147"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

