---
description: Especifica los registros de arquitectura de comprobación de la máquina (MCA) sin formato. Esta clase solo está disponible en sistemas Windows de 64 bits.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: MSMCAInfo_RawMCAData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541494"
---
# <a name="msmcainfo_rawmcadata-class"></a><span data-ttu-id="4398c-104">MSMCAInfo \_ RawMCAData (clase)</span><span class="sxs-lookup"><span data-stu-id="4398c-104">MSMCAInfo\_RawMCAData class</span></span>

<span data-ttu-id="4398c-105">El **MSMCAInfo \_ RawMCAData** especifica los registros de arquitectura de comprobación de la máquina (MCA) sin procesar.</span><span class="sxs-lookup"><span data-stu-id="4398c-105">The **MSMCAInfo\_RawMCAData** specifies the raw Machine Check Architecture (MCA) logs.</span></span> <span data-ttu-id="4398c-106">Esta clase solo está disponible en sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4398c-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="4398c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4398c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4398c-108">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4398c-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4398c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4398c-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="4398c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="4398c-110">Members</span></span>

<span data-ttu-id="4398c-111">La clase **MSMCAInfo \_ RawMCAData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4398c-111">The **MSMCAInfo\_RawMCAData** class has these types of members:</span></span>

-   [<span data-ttu-id="4398c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4398c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4398c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4398c-113">Properties</span></span>

<span data-ttu-id="4398c-114">La clase **MSMCAInfo \_ RawMCAData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4398c-114">The **MSMCAInfo\_RawMCAData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4398c-115">**Activo**</span><span class="sxs-lookup"><span data-stu-id="4398c-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398c-116">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4398c-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4398c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4398c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398c-118">TRUE si esta instancia de la clase está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4398c-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4398c-119">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="4398c-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398c-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4398c-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4398c-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4398c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398c-122">Número de registros de error.</span><span class="sxs-lookup"><span data-stu-id="4398c-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="4398c-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="4398c-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398c-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4398c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4398c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4398c-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4398c-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4398c-127">Identificador único de esta instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="4398c-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="4398c-128">**Registros**</span><span class="sxs-lookup"><span data-stu-id="4398c-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398c-129">Tipo de datos: matriz de **\_ entrada MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="4398c-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="4398c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4398c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398c-131">Matriz de registros de error de MCA.</span><span class="sxs-lookup"><span data-stu-id="4398c-131">Array of MCA error records.</span></span> <span data-ttu-id="4398c-132">La propiedad **Count** especifica el número de registros de error de MCA en la matriz.</span><span class="sxs-lookup"><span data-stu-id="4398c-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4398c-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4398c-133">Remarks</span></span>

<span data-ttu-id="4398c-134">La clase **MSMCAInfo \_ RawMCAData** se deriva de [**MSMCAInfo**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="4398c-134">The **MSMCAInfo\_RawMCAData** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4398c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4398c-135">Requirements</span></span>



| <span data-ttu-id="4398c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4398c-136">Requirement</span></span> | <span data-ttu-id="4398c-137">Value</span><span class="sxs-lookup"><span data-stu-id="4398c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4398c-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4398c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4398c-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4398c-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="4398c-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4398c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4398c-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4398c-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="4398c-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4398c-142">Namespace</span></span><br/>                | <span data-ttu-id="4398c-143">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="4398c-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="4398c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4398c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4398c-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4398c-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="4398c-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4398c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4398c-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4398c-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4398c-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="4398c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4398c-149">Clases MSMCA</span><span class="sxs-lookup"><span data-stu-id="4398c-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="4398c-150">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="4398c-150">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

