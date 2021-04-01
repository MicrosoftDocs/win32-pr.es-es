---
title: Método IVMVirtualMachineEvents OnHeartbeatStopped (VPCCOMInterfaces. h)
description: Recibe la notificación de que el latido de una máquina virtual se ha detenido.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- Método OnHeartbeatStopped Virtual PC
- Método OnHeartbeatStopped Virtual PC, interfaz IVMVirtualMachineEvents
- Interfaz IVMVirtualMachineEvents Virtual PC, método OnHeartbeatStopped
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ade783d2d182439d5c500dcc114c74c8278ba6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996875"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a><span data-ttu-id="ac36c-106">IVMVirtualMachineEvents:: OnHeartbeatStopped (método)</span><span class="sxs-lookup"><span data-stu-id="ac36c-106">IVMVirtualMachineEvents::OnHeartbeatStopped method</span></span>

<span data-ttu-id="ac36c-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ac36c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ac36c-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ac36c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ac36c-109">Recibe la notificación de que el latido de una máquina virtual se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="ac36c-109">Receives notification that a virtual machine's heartbeat has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac36c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac36c-110">Syntax</span></span>


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a><span data-ttu-id="ac36c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac36c-111">Parameters</span></span>

<span data-ttu-id="ac36c-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ac36c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac36c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac36c-113">Return value</span></span>

<span data-ttu-id="ac36c-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ac36c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac36c-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac36c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac36c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac36c-116">Remarks</span></span>

<span data-ttu-id="ac36c-117">Se llama a este método cuando el sistema operativo invitado de esta máquina virtual se ha detenido repentinamente.</span><span class="sxs-lookup"><span data-stu-id="ac36c-117">This method is called when the guest operating system for this virtual machine has stopped abruptly.</span></span> <span data-ttu-id="ac36c-118">El programa cliente debe implementar este método de interfaz para recibir la notificación del \_ evento vmVirtualMachineEvent HeartbeatStopped que se origina desde [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="ac36c-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_HeartbeatStopped event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac36c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac36c-119">Requirements</span></span>



| <span data-ttu-id="ac36c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac36c-120">Requirement</span></span> | <span data-ttu-id="ac36c-121">Value</span><span class="sxs-lookup"><span data-stu-id="ac36c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac36c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac36c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac36c-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac36c-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac36c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac36c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac36c-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ac36c-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ac36c-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ac36c-126">End of client support</span></span><br/>    | <span data-ttu-id="ac36c-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ac36c-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ac36c-128">Producto</span><span class="sxs-lookup"><span data-stu-id="ac36c-128">Product</span></span><br/>                  | <span data-ttu-id="ac36c-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ac36c-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ac36c-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac36c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac36c-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac36c-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ac36c-132">IID</span><span class="sxs-lookup"><span data-stu-id="ac36c-132">IID</span></span><br/>                      | <span data-ttu-id="ac36c-133">DIID \_ IVMVirtualMachineEvents se define como 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="ac36c-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="ac36c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac36c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac36c-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="ac36c-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

