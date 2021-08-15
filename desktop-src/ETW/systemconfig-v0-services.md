---
description: 'SystemConfig_V0_Services clase : esta clase es la clase de tipo de evento para los eventos de configuración del servicio.'
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: SystemConfig_V0_Services clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5cfe3bfd4509a02eeafcb014f9265f810e4cb942e87b67390dbd1cbf841f7295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393794"
---
# <a name="systemconfig_v0_services-class"></a>SystemConfig \_ V0 \_ Services (clase)

Esta clase es la clase de tipo de evento para los eventos de configuración del servicio.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a>Miembros

La **clase SystemConfig \_ V0 \_ Services** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SystemConfig \_ V0 \_ Services** tiene estas propiedades.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2), **Max** (256)
</dt> </dl>

Nombre para mostrar del servicio. El nombre se conserva en el Administrador de control de servicios. Sin embargo, las comparaciones de nombres para mostrar siempre se realizan sin distinción entre mayúsculas y minúsculas.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Identificador del proceso en el que se ejecuta el servicio.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3), **Max** (34)
</dt> </dl>

Nombre del proceso en el que se ejecuta el servicio.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1), **Max** (34)
</dt> </dl>

Identificador único del servicio. El identificador proporciona una indicación de la funcionalidad que proporciona el servicio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




