---
description: Copia el archivo o directorio de entrada del directorio lógico especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Método Copy de la clase Win32_Directory copia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 85a16d3e63ef46ad2c536103a4e462a3e830e17f56f83cdcf39bbad5a33ebb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419760"
---
# <a name="copy-method-of-the-win32_directory-class"></a>Método copy de la clase Directory de \_ Win32

El **método copy** wmi [class](/windows/desktop/WmiSdk/retrieving-a-class) copia el archivo o directorio de entrada del directorio lógico especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada. No se admite una copia si se requiere sobrescribir un archivo lógico existente.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nombre completo de la copia del archivo (o directorio). Ejemplo: c: \\ temp \\ newdirectory

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se copió correctamente y cualquier otro número para indicar un error.

<dl> <dt>

**0**
</dt> <dd>

La solicitud fue correcta.

</dd> <dt>

**2**
</dt> <dd>

Se denegó el acceso.

</dd> <dt>

**8**
</dt> <dd>

Error no especificado.

</dd> <dt>

**9**
</dt> <dd>

El nombre especificado no era válido.

</dd> <dt>

**10**
</dt> <dd>

El objeto especificado ya existe.

</dd> <dt>

**11**
</dt> <dd>

El sistema de archivos no es NTFS.

</dd> <dt>

**12**
</dt> <dd>

La plataforma no está Windows.

</dd> <dt>

**13**
</dt> <dd>

La unidad no es la misma.

</dd> <dt>

**14**
</dt> <dd>

El directorio no está vacío.

</dd> <dt>

**15**
</dt> <dd>

Se ha infringido el uso compartido.

</dd> <dt>

**16**
</dt> <dd>

El archivo de inicio especificado no era válido.

</dd> <dt>

**17**
</dt> <dd>

No se mantiene un privilegio necesario para la operación.

</dd> <dt>

**21**
</dt> <dd>

Un parámetro especificado no es válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las carpetas a menudo deben copiarse de una ubicación a otra. Por ejemplo, puede copiar una carpeta de un servidor a otro para crear una copia de seguridad de esa carpeta. O bien, puede tener una carpeta de plantillas que debe copiarse en estaciones de trabajo de usuario o una carpeta de scripts que se debe copiar en todos los servidores DNS.

El método De copia de directorio de Win32 permite copiar una carpeta de una ubicación a otra, ya sea en el mismo equipo (por ejemplo, copiando una carpeta de la unidad C a la unidad D) o en un \_ equipo remoto. Para copiar una carpeta, devuelve una instancia de la carpeta que se va a copiar y, a continuación, llama al método Copy, pasando como parámetro la ubicación de destino de la nueva copia de la carpeta. Por ejemplo, esta línea de código copia una carpeta en la carpeta Scripts de la unidad F:

`objFolder.Copy("F:\Scripts")`

WMI no sobrescribirá una carpeta existente al ejecutar el método Copy. Esto significa que se produce un error en la operación de copia si existe la carpeta de destino. Por ejemplo, suponga que tiene una carpeta denominada Scripts e intenta copiar esa carpeta en un recurso compartido remoto denominado \\ \\ atl-fs-01 \\ archive. Si ya existe una carpeta denominada Scripts en ese recurso compartido, se produce un error en la operación de copia.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente, tomado de Copiar una carpeta mediante [WMI,](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2)se usa el método Copy para copiar la carpeta C: \\ Scripts en D: \\ Archive.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Directorio \_ win32**](win32-directory.md)
</dt> </dl>

 

