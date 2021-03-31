---
description: El método Invoke de la \_ clase CIM OSVersionCheck evalúa una comprobación determinada. Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en las subclases de comprobación CIM no abstractas \_ . Este método se hereda de la \_ comprobación CIM.
ms.assetid: ff06772c-e40c-49c8-b334-5ee480926245
ms.tgt_platform: multiple
title: Método Invoke de la clase CIM_OSVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49d6944c4a28c956356fef430e47bc8636082930
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152984"
---
# <a name="invoke-method-of-the-cim_osversioncheck-class"></a>Método Invoke de la \_ clase CIM OSVersionCheck

El método **Invoke** de la clase [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) evalúa una comprobación determinada. Los detalles de cómo evalúa el método una comprobación determinada en un contexto CIM se describen en las subclases de [**\_ comprobación CIM**](cim-check.md) no abstractas. Este método se hereda de **la \_ comprobación CIM**.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.

## <a name="remarks"></a>Observaciones

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

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

[\_OSVERSIONCHECK CIM](invoke-method-in-class-cim-osversioncheck.md)
</dt> <dt>

[**\_OSVERSIONCHECK CIM**](cim-osversioncheck.md)
</dt> </dl>

 

