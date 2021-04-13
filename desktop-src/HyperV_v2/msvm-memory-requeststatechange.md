---
description: Solicita un cambio de estado.
ms.assetid: 836ee3a1-e28e-4f84-8e1c-09f4a2ff0a25
title: Método RequestStateChange de la clase Msvm_Memory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 761a486f21f6c1cd8c61978038cc2d37bba8c288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361410"
---
# <a name="requeststatechange-method-of-the-msvm_memory-class"></a><span data-ttu-id="c94d1-103">Método RequestStateChange de la \_ clase de memoria MSVM</span><span class="sxs-lookup"><span data-stu-id="c94d1-103">RequestStateChange method of the Msvm\_Memory class</span></span>

<span data-ttu-id="c94d1-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="c94d1-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="c94d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c94d1-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="c94d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c94d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c94d1-107">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c94d1-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c94d1-108">El nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="c94d1-108">The new state.</span></span> <span data-ttu-id="c94d1-109">La información se coloca en la propiedad **RequestedState** de la instancia de si el código de retorno del método **RequestStateChange** es 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="c94d1-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="c94d1-110">Para obtener más información, vea la descripción de las propiedades **EnabledState** y **RequestedState** del elemento.</span><span class="sxs-lookup"><span data-stu-id="c94d1-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="c94d1-111">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c94d1-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c94d1-112">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c94d1-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c94d1-113">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c94d1-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="c94d1-114">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="c94d1-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="c94d1-115">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="c94d1-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="c94d1-116">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="c94d1-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="c94d1-117">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="c94d1-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="c94d1-118">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="c94d1-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="c94d1-119">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="c94d1-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="c94d1-120">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="c94d1-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c94d1-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c94d1-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c94d1-122">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="c94d1-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c94d1-123">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c94d1-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c94d1-124">Puede contener una referencia al [**\_ ConcreteJob de CIM**](cim-concretejob.md) creado para realizar el seguimiento de la transición de estado iniciada por la invocación del método.</span><span class="sxs-lookup"><span data-stu-id="c94d1-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="c94d1-125">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c94d1-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c94d1-126">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="c94d1-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="c94d1-127">El formato de intervalo debe usarse para especificar el TimeoutPeriod.</span><span class="sxs-lookup"><span data-stu-id="c94d1-127">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="c94d1-128">Un valor de 0 o un parámetro null indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="c94d1-128">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="c94d1-129">Si esta propiedad no contiene 0 o NULL y la implementación no admite este parámetro, se devolverá el código de retorno "uso del parámetro de tiempo de espera no admitido".</span><span class="sxs-lookup"><span data-stu-id="c94d1-129">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c94d1-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c94d1-130">Return value</span></span>

<span data-ttu-id="c94d1-131">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c94d1-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c94d1-132">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c94d1-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c94d1-133">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="c94d1-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c94d1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c94d1-134">Requirements</span></span>



| <span data-ttu-id="c94d1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c94d1-135">Requirement</span></span> | <span data-ttu-id="c94d1-136">Value</span><span class="sxs-lookup"><span data-stu-id="c94d1-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c94d1-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c94d1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c94d1-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c94d1-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c94d1-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c94d1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c94d1-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c94d1-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c94d1-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c94d1-141">Namespace</span></span><br/>                | <span data-ttu-id="c94d1-142">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c94d1-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c94d1-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c94d1-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c94d1-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c94d1-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c94d1-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c94d1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c94d1-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c94d1-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c94d1-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c94d1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c94d1-148">**Memoria de MSVM \_**</span><span class="sxs-lookup"><span data-stu-id="c94d1-148">**Msvm\_Memory**</span></span>](msvm-memory.md)
</dt> </dl>

 

 




