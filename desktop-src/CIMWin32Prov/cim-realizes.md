---
description: La \_ clase CIM Observations representa la asociación que define la asignación entre un dispositivo lógico y el componente físico que implementa el dispositivo.
ms.assetid: 3bddb0c8-dca5-4877-9e30-322516a8d388
ms.tgt_platform: multiple
title: CIM_Realizes (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Realizes
- CIM_Realizes.Dependent
- CIM_Realizes.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b37b2f5f3fe9cfce78e16530df8b94e4333e9a33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659521"
---
# <a name="cim_realizes-class"></a><span data-ttu-id="194b1-103">CIM ( \_ clase)</span><span class="sxs-lookup"><span data-stu-id="194b1-103">CIM\_Realizes class</span></span>

<span data-ttu-id="194b1-104">La clase **CIM \_ Observations** representa la asociación que define la asignación entre un dispositivo lógico y el componente físico que implementa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="194b1-104">The **CIM\_Realizes** class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="194b1-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="194b1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="194b1-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="194b1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="194b1-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="194b1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="194b1-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="194b1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="194b1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="194b1-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B62-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Realizes : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_PhysicalElement REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="194b1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="194b1-110">Members</span></span>

<span data-ttu-id="194b1-111">La **clase \_ CIM** impones tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="194b1-111">The **CIM\_Realizes** class has these types of members:</span></span>

-   [<span data-ttu-id="194b1-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="194b1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="194b1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="194b1-113">Properties</span></span>

<span data-ttu-id="194b1-114">La clase **CIM \_ Observations** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="194b1-114">The **CIM\_Realizes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="194b1-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="194b1-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194b1-116">Tipo de datos: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="194b1-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="194b1-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="194b1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="194b1-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="194b1-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="194b1-119">Un [**\_ PhysicalElement de CIM**](cim-physicalelement.md) que describe el componente físico que implementa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="194b1-119">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical component that implements the device.</span></span>

</dd> <dt>

<span data-ttu-id="194b1-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="194b1-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194b1-121">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="194b1-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="194b1-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="194b1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="194b1-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="194b1-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="194b1-124">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="194b1-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="194b1-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="194b1-125">Remarks</span></span>

<span data-ttu-id="194b1-126">La **clase \_ CIM** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="194b1-126">The **CIM\_Realizes** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="194b1-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="194b1-127">WMI does not implement this class.</span></span>

<span data-ttu-id="194b1-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="194b1-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="194b1-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="194b1-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="194b1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="194b1-130">Requirements</span></span>



| <span data-ttu-id="194b1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="194b1-131">Requirement</span></span> | <span data-ttu-id="194b1-132">Value</span><span class="sxs-lookup"><span data-stu-id="194b1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="194b1-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="194b1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="194b1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="194b1-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="194b1-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="194b1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="194b1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="194b1-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="194b1-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="194b1-137">Namespace</span></span><br/>                | <span data-ttu-id="194b1-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="194b1-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="194b1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="194b1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="194b1-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="194b1-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="194b1-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="194b1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="194b1-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="194b1-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="194b1-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="194b1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194b1-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="194b1-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

