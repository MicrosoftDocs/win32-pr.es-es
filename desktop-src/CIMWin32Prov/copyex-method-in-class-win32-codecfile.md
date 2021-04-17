---
description: Copia el archivo o directorio lógico del códec especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName. Este método es una versión extendida del método de copia.
ms.assetid: 0e9097ed-a599-44f7-a654-8622c0618c27
ms.tgt_platform: multiple
title: Método CopyEx de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c649c60850c23313ad308a431714276ce30895b1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659766"
---
# <a name="copyex-method-of-the-win32_codecfile-class"></a>Método CopyEx de la \_ clase CodecFile de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia el archivo de códec lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* . Este método es una versión extendida del método de [**copia**](copy-method-in-class-win32-directory.md) . No se admite una copia si se requiere sobrescribir un archivo lógico existente.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* \[ de\]
</dt> <dd>

Nombre completo de la copia del archivo (o directorio).

Ejemplo: c: \\ temp \\ newdirectory.

</dd> <dt>

*StopFileName* \[ enuncia\]
</dt> <dd>

Nombre del archivo o directorio en el que se produjo un error en el método **CopyEx** . Este parámetro será **null** si el método se ejecuta correctamente.

</dd> <dt>

*StartFileName* \[ en, opcional\]
</dt> <dd>

Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **CopyEx**. El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .

</dd> <dt>

*Recursivo* \[ en, opcional\]
</dt> <dd>

Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .

> [!Note]  
> En el caso de las instancias de archivo, se omite el parámetro de entrada *recursivo* .

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se ha copiado correctamente y cualquier otro número para indicar un error.

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

Se produjo un error no especificado.

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

La plataforma no es Windows.

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

Se ha producido una infracción de uso compartido.

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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ CodecFile**](win32-codecfile.md)
</dt> </dl>

 

