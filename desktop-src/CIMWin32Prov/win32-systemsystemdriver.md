---
description: La \_ clase WMI SystemSystemDriver Association de Win32 relaciona un equipo y un controlador del sistema que se ejecutan en ese equipo.
ms.assetid: 82638c29-6769-4410-90bc-b408b27adad4
ms.tgt_platform: multiple
title: Win32_SystemSystemDriver (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSystemDriver
- Win32_SystemSystemDriver.GroupComponent
- Win32_SystemSystemDriver.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b193d173fa0592a44ba437543659dec456e432ea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539327"
---
# <a name="win32_systemsystemdriver-class"></a><span data-ttu-id="b536a-103">\_Clase Win32 SystemSystemDriver</span><span class="sxs-lookup"><span data-stu-id="b536a-103">Win32\_SystemSystemDriver class</span></span>

<span data-ttu-id="b536a-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemSystemDriver** Association de Win32 relaciona un equipo y un controlador del sistema que se ejecutan en ese equipo.</span><span class="sxs-lookup"><span data-stu-id="b536a-104">The **Win32\_SystemSystemDriver** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a system driver running on that computer system.</span></span>

<span data-ttu-id="b536a-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b536a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b536a-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b536a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b536a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b536a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSystemDriver : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_SystemDriver   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b536a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b536a-108">Members</span></span>

<span data-ttu-id="b536a-109">La **clase \_ SystemSystemDriver de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b536a-109">The **Win32\_SystemSystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="b536a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b536a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b536a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b536a-111">Properties</span></span>

<span data-ttu-id="b536a-112">La **clase \_ SystemSystemDriver de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b536a-112">The **Win32\_SystemSystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b536a-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b536a-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b536a-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b536a-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b536a-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b536a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b536a-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="b536a-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="b536a-117">Referencia a la instancia de que representa las propiedades del sistema del equipo en el que se ejecuta el controlador.</span><span class="sxs-lookup"><span data-stu-id="b536a-117">Reference to the instance representing the properties of the computer system upon which the driver is running.</span></span>

</dd> <dt>

<span data-ttu-id="b536a-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b536a-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b536a-119">Tipo de datos: **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="b536a-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="b536a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b536a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b536a-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="b536a-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="b536a-122">Referencia a la instancia de que representa el controlador del sistema que se ejecuta en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="b536a-122">Reference to the instance representing the system driver running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b536a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b536a-123">Remarks</span></span>

<span data-ttu-id="b536a-124">La **clase \_ SystemSystemDriver de Win32** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="b536a-124">The **Win32\_SystemSystemDriver** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b536a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b536a-125">Requirements</span></span>



| <span data-ttu-id="b536a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b536a-126">Requirement</span></span> | <span data-ttu-id="b536a-127">Value</span><span class="sxs-lookup"><span data-stu-id="b536a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b536a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b536a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b536a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b536a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b536a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b536a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b536a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b536a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b536a-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b536a-132">Namespace</span></span><br/>                | <span data-ttu-id="b536a-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b536a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b536a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b536a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b536a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b536a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b536a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b536a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b536a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b536a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b536a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b536a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b536a-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b536a-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="b536a-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b536a-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
