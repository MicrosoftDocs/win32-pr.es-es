---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.DateTime)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100875
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
ms.openlocfilehash: e43864a1b632adbc4ecf84d4963e7f87ea799283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686476"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-datetime"></a>Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)

Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As DateTime _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As DateTimeApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    DateTime data
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que se va a usar.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se va a actualizar. Se debe preparar una actualización.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid que se va a establecer.

<!-- end list -->

  - datos  
    Tipo: [System. DateTime](/dotnet/api/system.datetime)  
    
    Datos que se van a establecer.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga SetColumn](./api.setcolumn-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
