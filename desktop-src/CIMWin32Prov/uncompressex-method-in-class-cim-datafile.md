---
description: Descomprime el archivo de datos lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método UNCOMPRESS y se hereda de CIM \_ LogicalFile.
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: Método UncompressEx de la clase CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153442"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a>Método UncompressEx de la \_ clase de archivo de archivos CIM

El método **UncompressEx** descomprime el archivo de datos lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método [**UNCOMPRESS**](uncompress-method-in-class-cim-datafile.md) y se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StopFileName* \[ enuncia\]
</dt> <dd>

Nombre del archivo (o directorio) en el que se produjo un error en el método. Este parámetro es **null** si el método se ejecuta correctamente.

</dd> <dt>

*StartFileName* \[ de\]
</dt> <dd>

Archivo secundario (o directorio) que se va a usar como punto de partida para este método. Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior. Si este parámetro es **null**, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

Si se utiliza *StartFileName* , *Recursive* también debe establecerse en true.

</dd> <dt>

*Recursivo* \[ de\]
</dt> <dd>

Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**archivo de \_ archivos CIM**](cim-datafile.md) . En el caso de las instancias de archivo, este parámetro se omite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Correcto.

</dd> <dt>

**2**
</dt> <dd>

Acceso denegado.

</dd> <dt>

**8**
</dt> <dd>

Error no especificado.

</dd> <dt>

**9**
</dt> <dd>

Objeto no válido.

</dd> <dt>

**10**
</dt> <dd>

El objeto ya existe.

</dd> <dt>

**11**
</dt> <dd>

Sistema de archivos no NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plataforma no Windows.

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

Infracción de uso compartido.

</dd> <dt>

**16**
</dt> <dd>

Archivo de inicio no válido.

</dd> <dt>

**17**
</dt> <dd>

Privilegio no mantenido.

</dd> <dt>

**21**
</dt> <dd>

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI implementa el método **UncompressEx** en el [**archivo de \_ archivos de CIM**](cim-datafile.md) .

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

[**\_Archivo de archivos CIM**](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Archivo de archivos CIM**](cim-datafile.md)
</dt> <dt>

[Tareas de WMI: archivos y carpetas](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

