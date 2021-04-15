---
title: MDM_Update_FailedUpdates01_01 (clase)
description: La \_ clase de actualización \_ FailedUpdates01 01 de MDM \_ se utiliza para administrar las actualizaciones con errores.
ms.assetid: 3bb7993b-b44b-44d1-84ee-dbdda0093ca0
keywords:
- MDM_Update_FailedUpdates01_01 (clase)
- MDM_Update_FailedUpdates01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01.InstanceID
- MDM_Update_FailedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ba8d42d97b15cd195e87f536abad9610492e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489166"
---
# <a name="mdm_update_failedupdates01_01-class"></a><span data-ttu-id="b06a4-105">\_ \_ Clase FailedUpdates01 01 de actualización \_ de MDM</span><span class="sxs-lookup"><span data-stu-id="b06a4-105">MDM\_Update\_FailedUpdates01\_01 class</span></span>

<span data-ttu-id="b06a4-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b06a4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b06a4-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b06a4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b06a4-108">La clase de **\_ actualización \_ FailedUpdates01 \_ 01 de MDM** se utiliza para administrar las actualizaciones con errores.</span><span class="sxs-lookup"><span data-stu-id="b06a4-108">The **MDM\_Update\_FailedUpdates01\_01** class is used to manage failed updates.</span></span>

<span data-ttu-id="b06a4-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b06a4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b06a4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b06a4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_FailedUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 HResult;
  sint32 State;
};
```

## <a name="members"></a><span data-ttu-id="b06a4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b06a4-111">Members</span></span>

<span data-ttu-id="b06a4-112">La clase de **\_ actualización \_ FailedUpdates01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b06a4-112">The **MDM\_Update\_FailedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="b06a4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b06a4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b06a4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b06a4-114">Properties</span></span>

<span data-ttu-id="b06a4-115">La clase de **\_ actualización \_ FailedUpdates01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b06a4-115">The **MDM\_Update\_FailedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b06a4-116">HResult</span><span class="sxs-lookup"><span data-stu-id="b06a4-116">HResult</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-hresult)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06a4-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b06a4-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b06a4-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b06a4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b06a4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b06a4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06a4-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b06a4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06a4-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b06a4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06a4-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b06a4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b06a4-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b06a4-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="b06a4-124">Para esta clase, la cadena es el GUID de la actualización con errores.</span><span class="sxs-lookup"><span data-stu-id="b06a4-124">For this class, the string is the GUID of the failed update.</span></span>

</dd> <dt>

<span data-ttu-id="b06a4-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b06a4-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06a4-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b06a4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06a4-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b06a4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06a4-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b06a4-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b06a4-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b06a4-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="b06a4-130">Para esta clase, la cadena es "./Vendor/MSFT/Update/FailedUpdates".</span><span class="sxs-lookup"><span data-stu-id="b06a4-130">For this class, the string is "./Vendor/MSFT/Update/FailedUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="b06a4-131">**State**</span><span class="sxs-lookup"><span data-stu-id="b06a4-131">**State**</span></span>](/windows/client-management/mdm/update-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06a4-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b06a4-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b06a4-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b06a4-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b06a4-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b06a4-134">Requirements</span></span>



| <span data-ttu-id="b06a4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b06a4-135">Requirement</span></span> | <span data-ttu-id="b06a4-136">Value</span><span class="sxs-lookup"><span data-stu-id="b06a4-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b06a4-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b06a4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b06a4-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b06a4-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b06a4-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b06a4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b06a4-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b06a4-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="b06a4-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b06a4-141">Namespace</span></span><br/>                | <span data-ttu-id="b06a4-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b06a4-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="b06a4-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b06a4-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b06a4-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b06a4-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="b06a4-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b06a4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b06a4-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="b06a4-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

