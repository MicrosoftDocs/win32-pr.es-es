---
description: 'Método GetErrorEx de la Msvm_ConcreteJob clase : recupera los objetos de error del trabajo, si existe alguno.'
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: Método GetErrorEx de la Msvm_ConcreteJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f0e6af7883ec5aa1b7c0a714b822c8a0d8fd4a33dcda32ab4772e0573d60d046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149807"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a>Método GetErrorEx de la clase ConcreteJob de Msvm \_

Recupera los objetos de error para el trabajo, si existe alguno. Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna [**instancia de \_ error de Msvm.**](msvm-error.md) Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, se devuelven una o varias instancias de error de **Msvm. \_**

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Errores* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una o varias instancias incrustadas de la clase Error de [**Msvm, \_**](msvm-error.md) en formato CIM-XML, que representan los errores encontrados en el trabajo. Si el estado operativo del trabajo es 2 (correcto), se **devuelve Null.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**Sistema en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El acceso a [**la clase \_ ConcreteJob de Msvm**](msvm-concretejob.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

