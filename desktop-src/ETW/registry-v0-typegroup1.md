---
description: 'Registry_V0_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos del Registro. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Registry_V0_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 86f6d695afa2e05c87a076cf88ed8023e9416beb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106193"
---
# <a name="registry_v0_typegroup1-class"></a>Clase \_ \_ TypeGroup1 del Registro V0

Esta clase es la clase de tipo de evento para los eventos del Registro.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ TypeGroup1 de Registry V0** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ TypeGroup1 de Registry V0** tiene estas propiedades.

<dl> <dt>

ElapsedTime
</dt> <dd> <dl> <dt>

Tipo de datos: **sint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Tiempo transcurrido de la operación del Registro.

</dd> <dt>

KeyHandle
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Identificador de la clave del Registro.

</dd> <dt>

KeyName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nombre de la clave del Registro.

</dd> <dt>

Status
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Valor NTSTATUS de la operación del Registro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Registro \_ V0**](registry-v0.md)
</dt> </dl>

 

 




