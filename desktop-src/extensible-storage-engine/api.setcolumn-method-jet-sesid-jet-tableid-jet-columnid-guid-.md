---
description: 'Más información sobre: Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)'
title: Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Guid)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100874
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b99bd107528646ed31f37d65a0c4f23531e1c00f162c27a6a92d938944b69e0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117717596"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-guid"></a>Método Api.SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)

Modifica un valor de columna única en un registro modificado que se va a insertar o para actualizar el registro actual.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Guid _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As GuidApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Guid data
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sesión que se usará.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se actualizará. Se debe preparar una actualización.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid que se establece.

<!-- end list -->

  - datos  
    Tipo: [System.Guid](/dotnet/api/system.guid)  
    
    Datos que se van a establecer.

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de api](./api-members.md)

[Sobrecarga de SetColumn](./api.setcolumn-method.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
