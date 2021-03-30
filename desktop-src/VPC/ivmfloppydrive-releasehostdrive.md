---
title: Método IVMFloppyDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libera una unidad física del host de la unidad de disquete.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- Método ReleaseHostDrive Virtual PC
- Método ReleaseHostDrive Virtual PC, interfaz IVMFloppyDrive
- Interfaz IVMFloppyDrive Virtual PC, método ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ab726ba87dd978a21c4f27b20437926e07c19b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800979"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a><span data-ttu-id="b3b3b-106">IVMFloppyDrive:: ReleaseHostDrive (método)</span><span class="sxs-lookup"><span data-stu-id="b3b3b-106">IVMFloppyDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="b3b3b-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b3b3b-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b3b3b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b3b3b-109">Libera una unidad física del host de la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-109">Releases a physical drive on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b3b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3b3b-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="b3b3b-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3b3b-111">Parameters</span></span>

<span data-ttu-id="b3b3b-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3b3b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3b3b-113">Return value</span></span>

<span data-ttu-id="b3b3b-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b3b3b-115">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3b3b-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="b3b3b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3b3b-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3b3b-117"><dt>**S \_ Aceptar**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b3b3b-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="b3b3b-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b3b3b-119"><dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b3b3b-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="b3b3b-120">La configuración de esta máquina virtual no es válida o no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="b3b3b-121"><dt>**Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="b3b3b-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="b3b3b-122">El medio conectado a esta unidad de disquete no es una unidad de disquete física.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-122">The media attached to this floppy drive is not a physical floppy drive.</span></span><br/>     |
| <dl> <span data-ttu-id="b3b3b-123"><dt>**Máquina virtual \_ E \_ no se ha \_ \_ capturado ningún medio**</dt> <dt>0xA00400652</dt></span><span class="sxs-lookup"><span data-stu-id="b3b3b-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="b3b3b-124">No hay ningún medio conectado a esta unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="b3b3b-125"><dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b3b3b-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="b3b3b-126">Se produjo un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="b3b3b-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="b3b3b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3b3b-127">Requirements</span></span>



| <span data-ttu-id="b3b3b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b3b-128">Requirement</span></span> | <span data-ttu-id="b3b3b-129">Value</span><span class="sxs-lookup"><span data-stu-id="b3b3b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b3b-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3b3b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b3b3b-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3b3b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3b3b-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3b3b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b3b3b-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b3b3b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b3b3b-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b3b3b-134">End of client support</span></span><br/>    | <span data-ttu-id="b3b3b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3b3b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b3b3b-136">Producto</span><span class="sxs-lookup"><span data-stu-id="b3b3b-136">Product</span></span><br/>                  | <span data-ttu-id="b3b3b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b3b3b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b3b3b-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3b3b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3b3b-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3b3b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b3b3b-140">IID</span><span class="sxs-lookup"><span data-stu-id="b3b3b-140">IID</span></span><br/>                      | <span data-ttu-id="b3b3b-141">IID \_ IVMFloppyDrive se define como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="b3b3b-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b3b3b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3b3b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b3b-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="b3b3b-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

