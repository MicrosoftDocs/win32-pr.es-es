---
description: La \_ clase WMI SCSIControllerDevice Association de Win32 relaciona una controladora de interfaz del sistema de equipos pequeños (SCSI) y el dispositivo lógico (unidad de disco) conectado a ella.
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Win32_SCSIControllerDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a3189f9d9b75321df7c69214e68779864953f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539346"
---
# <a name="win32_scsicontrollerdevice-class"></a><span data-ttu-id="685ab-103">\_Clase Win32 SCSIControllerDevice</span><span class="sxs-lookup"><span data-stu-id="685ab-103">Win32\_SCSIControllerDevice class</span></span>

<span data-ttu-id="685ab-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SCSIControllerDevice** Association de Win32 relaciona una controladora de interfaz del sistema de equipos pequeños (SCSI) y el dispositivo lógico (unidad de disco) conectado a ella.</span><span class="sxs-lookup"><span data-stu-id="685ab-104">The **Win32\_SCSIControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a small computer system interface (SCSI) controller and the logical device (disk drive) connected to it.</span></span>

<span data-ttu-id="685ab-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="685ab-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="685ab-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="685ab-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="685ab-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="685ab-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="685ab-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="685ab-108">Members</span></span>

<span data-ttu-id="685ab-109">La **clase \_ SCSIControllerDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="685ab-109">The **Win32\_SCSIControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="685ab-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="685ab-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="685ab-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="685ab-111">Properties</span></span>

<span data-ttu-id="685ab-112">La **clase \_ SCSIControllerDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="685ab-112">The **Win32\_SCSIControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="685ab-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="685ab-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685ab-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="685ab-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="685ab-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="685ab-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="685ab-116">Indica si el controlador está activamente realizando comandos o accediendo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="685ab-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="685ab-117">Esta información es necesaria cuando se puede realizar el comando de un dispositivo lógico, o bien a través de varios controladores.</span><span class="sxs-lookup"><span data-stu-id="685ab-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="685ab-118">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="685ab-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="685ab-119">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="685ab-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="685ab-120">**Activo** (1)</span><span class="sxs-lookup"><span data-stu-id="685ab-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="685ab-121">**Inactivo** (2)</span><span class="sxs-lookup"><span data-stu-id="685ab-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="685ab-122">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="685ab-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685ab-123">Tipo de datos: **Win32 \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="685ab-123">Data type: **Win32\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="685ab-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="685ab-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="685ab-125">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| Win32 \_ SCSIController")</span><span class="sxs-lookup"><span data-stu-id="685ab-125">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|Win32\_SCSIController")</span></span>
</dt> </dl>

<span data-ttu-id="685ab-126">La referencia antecedente [**\_ SCSIController de Win32**](win32-scsicontroller.md) representa el controlador SCSI asociado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="685ab-126">The [**Win32\_SCSIController**](win32-scsicontroller.md) antecedent reference represents the SCSI controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="685ab-127">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="685ab-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685ab-128">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="685ab-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="685ab-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="685ab-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="685ab-130">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("dependiente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="685ab-130">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="685ab-131">La referencia dependiente del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) representa el dispositivo lógico conectado a la controladora SCSI.</span><span class="sxs-lookup"><span data-stu-id="685ab-131">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) dependent reference represents the logical device connected to the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="685ab-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="685ab-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685ab-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="685ab-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="685ab-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="685ab-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="685ab-135">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="685ab-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="685ab-136">Cuando se pueden usar varios buses o anchos de datos de conexión, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="685ab-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="685ab-137">El ancho de los datos se especifica en bits.</span><span class="sxs-lookup"><span data-stu-id="685ab-137">Data width is specified in bits.</span></span> <span data-ttu-id="685ab-138">Si no se negocia el ancho de los datos, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="685ab-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="685ab-139">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="685ab-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="685ab-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="685ab-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685ab-141">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="685ab-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="685ab-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="685ab-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="685ab-143">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="685ab-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="685ab-144">Cuando se pueden realizar varias velocidades de conexión o bus, esta propiedad define el que se utiliza entre los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="685ab-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="685ab-145">La velocidad se especifica en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="685ab-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="685ab-146">Si no se negocian las velocidades de conexión o de bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="685ab-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="685ab-147">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="685ab-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="685ab-148">Esta propiedad se hereda de [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="685ab-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="685ab-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="685ab-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685ab-150">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="685ab-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="685ab-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="685ab-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="685ab-152">Número de restablecimientos fuertes emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="685ab-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="685ab-153">Un restablecimiento de hardware devuelve el dispositivo a su estado de inicialización o arranque.</span><span class="sxs-lookup"><span data-stu-id="685ab-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="685ab-154">Se pierden todos los datos y la información de estado de los dispositivos internos.</span><span class="sxs-lookup"><span data-stu-id="685ab-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="685ab-155">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="685ab-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="685ab-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="685ab-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685ab-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="685ab-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="685ab-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="685ab-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="685ab-159">Número de restablecimientos flexibles emitidos por el controlador.</span><span class="sxs-lookup"><span data-stu-id="685ab-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="685ab-160">Un restablecimiento parcial no borra completamente los datos y el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="685ab-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="685ab-161">La semántica exacta depende del dispositivo y de los protocolos y mecanismos utilizados para comunicarse con él.</span><span class="sxs-lookup"><span data-stu-id="685ab-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="685ab-162">Esta propiedad se hereda de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="685ab-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="685ab-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="685ab-163">Remarks</span></span>

<span data-ttu-id="685ab-164">La **clase \_ SCSIControllerDevice de Win32** se deriva de [**\_ ControlledBy de CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="685ab-164">The **Win32\_SCSIControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="685ab-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="685ab-165">Requirements</span></span>



| <span data-ttu-id="685ab-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="685ab-166">Requirement</span></span> | <span data-ttu-id="685ab-167">Value</span><span class="sxs-lookup"><span data-stu-id="685ab-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="685ab-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="685ab-168">Minimum supported client</span></span><br/> | <span data-ttu-id="685ab-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="685ab-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="685ab-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="685ab-170">Minimum supported server</span></span><br/> | <span data-ttu-id="685ab-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="685ab-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="685ab-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="685ab-172">Namespace</span></span><br/>                | <span data-ttu-id="685ab-173">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="685ab-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="685ab-174">MOF</span><span class="sxs-lookup"><span data-stu-id="685ab-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="685ab-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="685ab-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="685ab-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="685ab-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="685ab-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="685ab-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685ab-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="685ab-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685ab-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="685ab-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="685ab-180">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="685ab-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
