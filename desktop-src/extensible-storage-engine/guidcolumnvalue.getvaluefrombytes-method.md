---
description: 'Más información sobre: GuidColumnValue. GetValueFromBytes (método)'
title: GuidColumnValue. GetValueFromBytes, método
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.guidcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55107384
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06f10cef46603d6cf023ed3786b3c6bbe1b1a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715546"
---
# <a name="guidcolumnvaluegetvaluefrombytes-method"></a>GuidColumnValue. GetValueFromBytes, método

Dados los datos recuperados de ESENT, descodifique los datos y establezca el valor en el objeto ColumnValue.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Parámetros

  - value  
    Automáticamente \[\]  
    
    Matriz de bytes.

<!-- end list -->

  - startIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Posición inicial dentro de los bytes.

<!-- end list -->

  - count  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número de bytes que se van a descodificar.

<!-- end list -->

  - err  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Error devuelto desde ESENT.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase GuidColumnValue](./guidcolumnvalue-class.md)

[Miembros de GuidColumnValue](./guidcolumnvalue-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
