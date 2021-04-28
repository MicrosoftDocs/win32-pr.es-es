---
description: 'Método reset de la CIM_Sensor : el método Reset solicita un restablecimiento del dispositivo lógico. Este método se hereda de CIM \_ LogicalDevice.'
ms.assetid: d764986b-b512-4f38-8284-d16b1f670871
ms.tgt_platform: multiple
title: Método Reset de la CIM_Sensor clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Sensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a17599216226f2420504ee07fccd2174d7eff4e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096863"
---
# <a name="reset-method-of-the-cim_sensor-class"></a><span data-ttu-id="85479-104">Método de restablecimiento de la clase sensor CIM \_</span><span class="sxs-lookup"><span data-stu-id="85479-104">Reset method of the CIM\_Sensor class</span></span>

<span data-ttu-id="85479-105">El **método Reset** solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="85479-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="85479-106">Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="85479-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85479-107">Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="85479-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="85479-108">WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="85479-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85479-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85479-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="85479-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85479-110">Parameters</span></span>

<span data-ttu-id="85479-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="85479-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85479-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85479-112">Return value</span></span>

<span data-ttu-id="85479-113">Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y algún otro valor si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="85479-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="85479-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85479-114">Remarks</span></span>

<span data-ttu-id="85479-115">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="85479-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="85479-116">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="85479-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="85479-117">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="85479-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="85479-118">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="85479-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="85479-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85479-119">Requirements</span></span>



| <span data-ttu-id="85479-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85479-120">Requirement</span></span> | <span data-ttu-id="85479-121">Valor</span><span class="sxs-lookup"><span data-stu-id="85479-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85479-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85479-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85479-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85479-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85479-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85479-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85479-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85479-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85479-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85479-126">Namespace</span></span><br/>                | <span data-ttu-id="85479-127">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="85479-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="85479-128">MOF</span><span class="sxs-lookup"><span data-stu-id="85479-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85479-129"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="85479-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="85479-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85479-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85479-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85479-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85479-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="85479-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85479-133">CIM \_ Sensor</span><span class="sxs-lookup"><span data-stu-id="85479-133">CIM\_Sensor</span></span>](reset-method-in-class-cim-sensor.md)
</dt> <dt>

[<span data-ttu-id="85479-134">**CIM \_ Sensor**</span><span class="sxs-lookup"><span data-stu-id="85479-134">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

 




