---
description: Modifica los datos de configuración para el servicio de migración.
ms.assetid: 5162fe88-dd39-4fe0-b8e9-e9b70c2b6a5c
title: Método ModifyServiceSettings de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1e9dc96196752ec4408939adc418e7c43bc0c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668078"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="b51c1-103">Método ModifyServiceSettings de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="b51c1-103">ModifyServiceSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="b51c1-104">Modifica los datos de configuración para el servicio de migración.</span><span class="sxs-lookup"><span data-stu-id="b51c1-104">Modifies the setting data for the migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b51c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b51c1-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b51c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b51c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b51c1-107">*ServiceSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b51c1-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b51c1-108">Una instancia incrustada de la clase [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) que contiene los nuevos valores de servicio.</span><span class="sxs-lookup"><span data-stu-id="b51c1-108">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the new service settings.</span></span>

</dd> <dt>

<span data-ttu-id="b51c1-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b51c1-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b51c1-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b51c1-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b51c1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b51c1-111">Return value</span></span>

<span data-ttu-id="b51c1-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b51c1-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b51c1-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b51c1-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b51c1-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="b51c1-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b51c1-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="b51c1-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b51c1-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="b51c1-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b51c1-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b51c1-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="b51c1-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b51c1-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="b51c1-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b51c1-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b51c1-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b51c1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b51c1-126">Requirements</span></span>



| <span data-ttu-id="b51c1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b51c1-127">Requirement</span></span> | <span data-ttu-id="b51c1-128">Value</span><span class="sxs-lookup"><span data-stu-id="b51c1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b51c1-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b51c1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b51c1-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b51c1-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b51c1-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b51c1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b51c1-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b51c1-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b51c1-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b51c1-133">Namespace</span></span><br/>                | <span data-ttu-id="b51c1-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b51c1-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b51c1-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b51c1-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b51c1-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b51c1-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b51c1-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b51c1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b51c1-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b51c1-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b51c1-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b51c1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b51c1-140">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="b51c1-140">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

