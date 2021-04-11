---
description: La \_ clase CIM SoftwareFeatureServiceImplementation representa una asociación entre un servicio y cómo se implementa en el software.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureServiceImplementation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152834"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a>\_Clase SoftwareFeatureServiceImplementation de CIM

La clase **CIM \_ SoftwareFeatureServiceImplementation** representa una asociación entre un servicio y cómo se implementa en el software. Un servicio puede ser proporcionado por más de una característica de software, que funciona conjuntamente entre sí. Además, una característica de software puede proporcionar más de un servicio. Cuando hay varias características de software asociadas a un único servicio, se supone que los elementos funcionan conjuntamente para proporcionar el servicio. Si existen implementaciones diferentes de un servicio, cada implementación produciría instancias individuales del objeto de servicio. Las instancias individuales tendrían asociaciones con las implementaciones únicas.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ SoftwareFeatureServiceImplementation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ SoftwareFeatureServiceImplementation** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ SoftwareFeature de CIM**](cim-softwarefeature.md) que describe la característica de software antecedente.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ servicio CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Un [**\_ servicio CIM**](cim-service.md) que describe el servicio dependiente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ SoftwareFeatureServiceImplementation** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 

