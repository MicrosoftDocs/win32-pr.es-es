---
description: Detiene el servicio representado por el objeto derivado de \_ CLUSTERINGSERVICE CIM.
ms.assetid: b8dbaeeb-819b-469b-9f5e-d658e88d1a6e
ms.tgt_platform: multiple
title: Método StopService de la clase CIM_ClusteringService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3a55f7b0a9527092e51156d55c7513ee59c4861
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907260"
---
# <a name="stopservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="bd487-103">Método StopService de la \_ clase ClusteringService de CIM</span><span class="sxs-lookup"><span data-stu-id="bd487-103">StopService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="bd487-104">El método **StopService** detiene el servicio representado por el objeto derivado de [**\_ ClusteringService CIM**](cim-clusteringservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd487-104">The **StopService** method stops the service represented by the object derived from [**CIM\_ClusteringService**](cim-clusteringservice.md).</span></span> <span data-ttu-id="bd487-105">Este método se hereda del [**\_ servicio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd487-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd487-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="bd487-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bd487-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bd487-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bd487-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="bd487-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bd487-109">Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bd487-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd487-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd487-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="bd487-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd487-111">Parameters</span></span>

<span data-ttu-id="bd487-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bd487-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd487-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd487-113">Return value</span></span>

<span data-ttu-id="bd487-114">Devuelve un valor de 0 (cero) si el servicio se detuvo correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="bd487-114">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd487-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd487-115">Remarks</span></span>

<span data-ttu-id="bd487-116">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="bd487-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="bd487-117">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="bd487-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="bd487-118">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="bd487-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bd487-119">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="bd487-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd487-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd487-120">Requirements</span></span>



| <span data-ttu-id="bd487-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd487-121">Requirement</span></span> | <span data-ttu-id="bd487-122">Value</span><span class="sxs-lookup"><span data-stu-id="bd487-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd487-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd487-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bd487-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd487-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd487-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd487-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bd487-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd487-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd487-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bd487-127">Namespace</span></span><br/>                | <span data-ttu-id="bd487-128">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bd487-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd487-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd487-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd487-130"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd487-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="bd487-131">MOF</span><span class="sxs-lookup"><span data-stu-id="bd487-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd487-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd487-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd487-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd487-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd487-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd487-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd487-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd487-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd487-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="bd487-136">**CIM\_ClusteringService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="bd487-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="bd487-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

