---
description: 'Más información sobre: método API. JetUpdate (JET_SESID, JET_TABLEID)'
title: Método API. JetUpdate (JET_SESID, JET_TABLEID)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361516"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a>Método API. JetUpdate (JET_SESID, JET_TABLEID)

La función JetUpdate realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente. La eliminación de una fila de tabla se realiza mediante una llamada a [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parámetros

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    La sesión que inició la actualización.

<!-- end list -->

  - TABLEID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursor que se va a actualizar. Se debe preparar una actualización.

## <a name="remarks"></a>Observaciones

JetUpdate es el último paso para realizar una inserción o una actualización. La actualización se inicia llamando a [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) y llamando a [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o varias veces para establecer el estado del registro. Por último, se llama a [JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) para completar la operación de actualización. Los índices solo se actualizan mediante JetUpdate o y no durante JetSetColumn.

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase de API](./api-class.md)

[Miembros de API](./api-members.md)

[Sobrecarga JetUpdate](./api.jetupdate-method.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
