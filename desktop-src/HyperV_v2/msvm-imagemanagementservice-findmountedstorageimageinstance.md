---
description: Busca un \_ objeto MSVM MountedStorageImage para una ruta de acceso de imagen de disco determinada.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Método FindMountedStorageImageInstance de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542470"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>Método FindMountedStorageImageInstance de la \_ clase ImageManagementService de MSVM

Busca un objeto [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) para una ruta de acceso de imagen de disco determinada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SelectionCriterion* \[ de\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación de un archivo de imagen de disco.

</dd> <dt>

*CriterionType* \[ de\]
</dt> <dd>

Tipo de criterio que se va a buscar al buscar la imagen de disco.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Ruta de acceso** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Imagen* \[ de enuncia\]
</dt> <dd>

Una referencia a [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) (puede ser null si la imagen no está montada).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**No se encontró el archivo** (32779)
</dt> <dt>

**Objeto no encontrado** (32789)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




