---
description: 'Más información sobre: método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)'
title: Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100811
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd320c42e1d24c0919010706ae3f7e61a65b78a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707402"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string"></a>Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)

Establece las opciones de configuración de base de datos.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As Integer, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    int paramValue,
    string paramString
)
```

#### <a name="parameters"></a>Parámetros

  - instance  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instancia en la que se va a establecer la opción o [Nil](./jet-instance.nil-property.md) para establecer la opción en todas las instancias.

<!-- end list -->

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - paramid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)  
    
    Parámetro que se va a establecer.

<!-- end list -->

  - Parámetro ParamValue  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Valor del parámetro que se va a establecer, si el parámetro es un tipo entero.

<!-- end list -->

  - paramString  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Valor del parámetro que se va a establecer, si el parámetro es un tipo de cadena.

#### <a name="return-value"></a>Valor devuelto

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Código de advertencia de ESENT.  

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga JetSetSystemParameter](./api.jetsetsystemparameter-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
