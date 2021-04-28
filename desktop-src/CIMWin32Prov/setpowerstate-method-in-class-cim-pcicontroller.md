---
description: 'Método SetPowerState de la clase CIM_PCIController: el método SetPowerState establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo en ese estado.'
ms.assetid: 846177b6-eb78-4dbd-8463-8295a5ad3cdf
ms.tgt_platform: multiple
title: Método SetPowerState de la CIM_PCIController clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCIController.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bbeffb3e6e2f3003eb6dab4e41a2d8d6cc3b6a63
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089383"
---
# <a name="setpowerstate-method-of-the-cim_pcicontroller-class"></a><span data-ttu-id="ee7c2-103">Método SetPowerState de la clase \_ PCIController de CIM</span><span class="sxs-lookup"><span data-stu-id="ee7c2-103">SetPowerState method of the CIM\_PCIController class</span></span>

<span data-ttu-id="ee7c2-104">El **método SetPowerState** establece el estado de energía deseado para un dispositivo lógico y cuándo se debe colocar un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ee7c2-105">En una subclase, el conjunto de códigos de retorno posibles debe especificarse mediante un **calificador ValueMap** en el método .</span><span class="sxs-lookup"><span data-stu-id="ee7c2-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ee7c2-106">Las cadenas a las que se traduce el contenido de **ValueMap** también se deben especificar en la subclase como calificador de **matriz Values.**</span><span class="sxs-lookup"><span data-stu-id="ee7c2-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="ee7c2-107">Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="ee7c2-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee7c2-108">Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ee7c2-109">WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ee7c2-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ee7c2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee7c2-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ee7c2-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee7c2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee7c2-112">*PowerState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ee7c2-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7c2-113">Valor **valueMap** que especifica el estado de energía deseado para este dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="ee7c2-114">1</span><span class="sxs-lookup"><span data-stu-id="ee7c2-114">1</span></span>
</dt> <dd>

<span data-ttu-id="ee7c2-115">Energía completa.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="ee7c2-116">2</span><span class="sxs-lookup"><span data-stu-id="ee7c2-116">2</span></span>
</dt> <dd>

<span data-ttu-id="ee7c2-117">Ahorro de energía en modo de bajo consumo.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="ee7c2-118">3</span><span class="sxs-lookup"><span data-stu-id="ee7c2-118">3</span></span>
</dt> <dd>

<span data-ttu-id="ee7c2-119">Espera de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="ee7c2-120">4</span><span class="sxs-lookup"><span data-stu-id="ee7c2-120">4</span></span>
</dt> <dd>

<span data-ttu-id="ee7c2-121">Otro ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="ee7c2-122">5</span><span class="sxs-lookup"><span data-stu-id="ee7c2-122">5</span></span>
</dt> <dd>

<span data-ttu-id="ee7c2-123">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="ee7c2-124">6</span><span class="sxs-lookup"><span data-stu-id="ee7c2-124">6</span></span>
</dt> <dd>

<span data-ttu-id="ee7c2-125">Apagar.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ee7c2-126">*Hora* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ee7c2-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee7c2-127">Especifica cuándo se debe establecer el estado de energía, ya sea como un valor de fecha y hora normal o como un valor de intervalo (donde el intervalo comienza cuando se recibe la invocación del método).</span><span class="sxs-lookup"><span data-stu-id="ee7c2-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="ee7c2-128">Cuando el *parámetro PowerState* es igual a 5 ("Ciclo de energía"), el parámetro *Time* indica cuándo se debe volver a encender el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="ee7c2-129">El apagado es inmediato.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee7c2-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee7c2-130">Return value</span></span>

<span data-ttu-id="ee7c2-131">Devuelve 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud *PowerState* y *Time* especificadas y otro valor si se produjo cualquier otro error.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee7c2-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee7c2-132">Remarks</span></span>

<span data-ttu-id="ee7c2-133">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ee7c2-134">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ee7c2-135">Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ee7c2-136">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="ee7c2-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7c2-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee7c2-137">Requirements</span></span>



| <span data-ttu-id="ee7c2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee7c2-138">Requirement</span></span> | <span data-ttu-id="ee7c2-139">Valor</span><span class="sxs-lookup"><span data-stu-id="ee7c2-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7c2-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee7c2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ee7c2-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee7c2-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee7c2-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee7c2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ee7c2-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee7c2-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee7c2-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ee7c2-144">Namespace</span></span><br/>                | <span data-ttu-id="ee7c2-145">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="ee7c2-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee7c2-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ee7c2-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee7c2-147"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee7c2-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee7c2-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee7c2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee7c2-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee7c2-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee7c2-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee7c2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7c2-151">CIM \_ PCIController</span><span class="sxs-lookup"><span data-stu-id="ee7c2-151">CIM\_PCIController</span></span>](setpowerstate-method-in-class-cim-pcicontroller.md)
</dt> <dt>

[<span data-ttu-id="ee7c2-152">**CIM \_ PCIController**</span><span class="sxs-lookup"><span data-stu-id="ee7c2-152">**CIM\_PCIController**</span></span>](cim-pcicontroller.md)
</dt> </dl>

 

 




