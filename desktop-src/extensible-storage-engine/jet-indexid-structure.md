---
description: 'Más información sobre: JET_INDEXID estructura'
title: JET_INDEXID estructura
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89af1b81b5221ab1cdebc0c91d5340acc62dd330
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983978"
---
# <a name="jet_indexid-structure"></a>JET_INDEXID estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_indexid-structure"></a>JET_INDEXID estructura

La **JET_INDEXID** contiene un identificador de índice. Un identificador de índice es una sugerencia que se usa para acelerar la selección del índice actual [mediante JetSetCurrentIndex](./jetsetcurrentindex-function.md). Es muy útil cuando hay un número muy grande de índices en una tabla. El identificador de índice se puede recuperar [mediante JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño, en bytes, del identificador de índice.

Este es el tamaño real del identificador de índice que se devuelve en el búfer de salida de [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo.](./jetgettableindexinfo-function.md)

**rgbIndexId**

Blob opaco de información que usa el motor para identificar rápidamente un índice en su caché de esquemas.

No intente interpretar el BLOB de información. No es un tamaño establecido.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
