---
title: Win32_SessionDirectoryVMMPlugin (clase)
description: Representa un complemento de Virtual Machine Manager (VMM) registrado con un agente de sesiones.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectoryVMMPlugin de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996073"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a>\_Clase Win32 SessionDirectoryVMMPlugin

Representa un complemento de Virtual Machine Manager (VMM) registrado con un agente de sesiones.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a>Miembros

La **clase \_ SessionDirectoryVMMPlugin de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ SessionDirectoryVMMPlugin** tiene estos métodos.



| Método                                                                             | Descripción                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetCurrentVMMPlugin**](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | Obtiene el complemento de prioridad máxima que está habilitado.<br/> |
| [**RegisterVMMPlugin**](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | Registra un nuevo complemento de VMM.<br/>                       |
| [**SetEnabled**](setenabled-win32-sessiondirectoryvmmplugin.md)                   | Habilita o deshabilita el complemento.<br/>                   |
| [**SetName**](setname-win32-sessiondirectoryvmmplugin.md)                         | Establece el nombre del complemento.<br/>                      |
| [**SetPriority**](setpriority-win32-sessiondirectoryvmmplugin.md)                 | Establece la prioridad del complemento.<br/>                  |
| [**SetProvider**](setprovider-win32-sessiondirectoryvmmplugin.md)                 | Establece el nombre del proveedor del complemento.<br/>             |
| [**SetServiceLocation**](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | Establece la ubicación del servicio del complemento.<br/>          |
| [**UnregisterVMMPlugin**](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | Anula el registro del complemento.<br/>                           |



 

### <a name="properties"></a>Propiedades

La **clase \_ SessionDirectoryVMMPlugin de Win32** tiene estas propiedades.

<dl> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el complemento está habilitado o deshabilitado. **True** si el complemento está habilitado o **false** en caso contrario. El complemento está deshabilitado de forma predeterminada.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Prioridad del complemento. Cuanto mayor sea el valor, mayor será la prioridad del complemento. De forma predeterminada, la prioridad es cero.

</dd> <dt>

**sClassID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de clase del complemento.

</dd> <dt>

**sName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del complemento.

</dd> <dt>

**sProvider**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del proveedor del complemento.

</dd> <dt>

**sServiceLocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La ubicación del servicio en la que debe ponerse en contacto el complemento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

