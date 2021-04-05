---
title: Propiedad del elemento IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Recupera el objeto de máquina virtual que corresponde al índice especificado.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Propiedad del elemento Virtual PC
- Propiedad del elemento Virtual PC, interfaz IVMVirtualMachineCollection
- Interfaz IVMVirtualMachineCollection Virtual PC, propiedad Item
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d70a6e30ff53f234f40803cd02fa16539f09e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078806"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a><span data-ttu-id="9ef8e-106">IVMVirtualMachineCollection:: Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9ef8e-106">IVMVirtualMachineCollection::Item property</span></span>

<span data-ttu-id="9ef8e-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9ef8e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9ef8e-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9ef8e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9ef8e-109">Recupera el objeto de máquina virtual que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="9ef8e-109">Retrieves the virtual machine object that corresponds to the specified index.</span></span>

<span data-ttu-id="9ef8e-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9ef8e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef8e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ef8e-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="9ef8e-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9ef8e-112">Property value</span></span>

<span data-ttu-id="9ef8e-113">El objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef8e-113">The [**IVMVirtualMachine**](ivmvirtualmachine.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9ef8e-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9ef8e-114">Error codes</span></span>



| <span data-ttu-id="9ef8e-115">Nombre o valor</span><span class="sxs-lookup"><span data-stu-id="9ef8e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="9ef8e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9ef8e-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ef8e-117"><dt>S \_ Aceptar</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9ef8e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9ef8e-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9ef8e-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="9ef8e-119"><dt>E \_ PUNTERO</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9ef8e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="9ef8e-120">El parámetro *virtualMachine* es **null**.</span><span class="sxs-lookup"><span data-stu-id="9ef8e-120">The *virtualMachine* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="9ef8e-121"><dt>DISP \_ . E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="9ef8e-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="9ef8e-122">El índice del elemento solicitado no corresponde a un elemento de esta colección.</span><span class="sxs-lookup"><span data-stu-id="9ef8e-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="9ef8e-123"><dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9ef8e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="9ef8e-124">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="9ef8e-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="9ef8e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ef8e-125">Requirements</span></span>



| <span data-ttu-id="9ef8e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ef8e-126">Requirement</span></span> | <span data-ttu-id="9ef8e-127">Value</span><span class="sxs-lookup"><span data-stu-id="9ef8e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef8e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ef8e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef8e-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ef8e-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ef8e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ef8e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef8e-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9ef8e-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9ef8e-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9ef8e-132">End of client support</span></span><br/>    | <span data-ttu-id="9ef8e-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ef8e-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="9ef8e-134">Producto</span><span class="sxs-lookup"><span data-stu-id="9ef8e-134">Product</span></span><br/>                  | <span data-ttu-id="9ef8e-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9ef8e-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="9ef8e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ef8e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef8e-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ef8e-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="9ef8e-138">IID</span><span class="sxs-lookup"><span data-stu-id="9ef8e-138">IID</span></span><br/>                      | <span data-ttu-id="9ef8e-139">IID \_ IVMVirtualMachineCollection se define como 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="9ef8e-139">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ef8e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ef8e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef8e-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="9ef8e-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="9ef8e-142">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="9ef8e-142">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

