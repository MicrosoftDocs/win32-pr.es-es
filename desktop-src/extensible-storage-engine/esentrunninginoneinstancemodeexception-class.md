---
description: 'Más información sobre: clase EsentRunningInOneInstanceModeException'
title: Clase EsentRunningInOneInstanceModeException
TOCTitle: EsentRunningInOneInstanceModeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrunninginoneinstancemodeexception(v=EXCHG.10)
ms:contentKeyID: 55102675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRunningInOneInstanceModeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b764bd604076ee4dae1d3ee21d52c1d3b923407e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707057"
---
# <a name="esentrunninginoneinstancemodeexception-class"></a>Clase EsentRunningInOneInstanceModeException

Clase base para JET_err. Excepciones RunningInOneInstanceMode.

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentRunningInOneInstanceModeException  

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRunningInOneInstanceModeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRunningInOneInstanceModeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRunningInOneInstanceModeException : EsentUsageException
```

## <a name="thread-safety"></a>Seguridad para subprocesos

Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos. No se garantiza que los miembros de instancia sean seguros para subprocesos.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Miembros de EsentRunningInOneInstanceModeException](./esentrunninginoneinstancemodeexception-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
