---
description: Convertir una instantánea del sistema virtual existente en un punto de referencia. La instantánea se elimina como un efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Método ConvertToReferencePoint de la clase Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666320"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="6f5e2-105">Método ConvertToReferencePoint de la \_ clase VirtualSystemSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="6f5e2-105">ConvertToReferencePoint method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="6f5e2-106">Convertir una instantánea del sistema virtual existente en un punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="6f5e2-106">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="6f5e2-107">La instantánea se elimina como un efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="6f5e2-107">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="6f5e2-108">Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.</span><span class="sxs-lookup"><span data-stu-id="6f5e2-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f5e2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f5e2-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6f5e2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f5e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f5e2-111">*AffectedSnapshot* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f5e2-111">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f5e2-112">Referencia a la instantánea del sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="6f5e2-112">Reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="6f5e2-113">*ReferencePointSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f5e2-113">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f5e2-114">Configuración de parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f5e2-114">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="6f5e2-115">*ResultingReferencePoint* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6f5e2-115">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f5e2-116">Punto de referencia del sistema virtual resultante</span><span class="sxs-lookup"><span data-stu-id="6f5e2-116">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="6f5e2-117">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6f5e2-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f5e2-118">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="6f5e2-118">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f5e2-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f5e2-119">Return value</span></span>

<span data-ttu-id="6f5e2-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="6f5e2-120">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6f5e2-121">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-122">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-123">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-124">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-125">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-126">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-127">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-127">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-128">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-129">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-130">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6f5e2-131">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="6f5e2-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6f5e2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f5e2-132">Requirements</span></span>



| <span data-ttu-id="6f5e2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f5e2-133">Requirement</span></span> | <span data-ttu-id="6f5e2-134">Value</span><span class="sxs-lookup"><span data-stu-id="6f5e2-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5e2-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f5e2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6f5e2-136">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f5e2-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6f5e2-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f5e2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6f5e2-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6f5e2-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6f5e2-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f5e2-139">Namespace</span></span><br/>                | <span data-ttu-id="6f5e2-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6f5e2-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6f5e2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6f5e2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f5e2-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f5e2-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f5e2-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f5e2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f5e2-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f5e2-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f5e2-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f5e2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f5e2-146">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="6f5e2-146">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




