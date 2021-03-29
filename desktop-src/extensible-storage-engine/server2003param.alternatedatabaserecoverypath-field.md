---
description: 'Más información sobre: Server2003Param. AlternateDatabaseRecoveryPath, campo'
title: Campo Server2003Param. AlternateDatabaseRecoveryPath (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 770ac27596b4385d0012cb65847754b4deb7e9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648231"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a>Server2003Param. AlternateDatabaseRecoveryPath, campo

La ruta de acceso completa a cada base de datos se conserva en los registros de transacciones en tiempo de ejecución. Normalmente, estas bases de datos deben permanecer en la ubicación original para que la reproducción de transacciones funcione correctamente. Este parámetro se puede usar para forzar la recuperación tras bloqueo o una operación de restauración para buscar las bases de datos a las que se hace referencia en el registro de transacciones en la carpeta especificada.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase Server2003Param](./server2003param-class.md)

[Miembros de Server2003Param](./server2003param-members.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
