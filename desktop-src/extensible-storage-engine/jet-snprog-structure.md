---
description: 'Más información sobre: JET_SNPROG estructura'
title: JET_SNPROG estructura
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 251f7948ec4d15e455720043b847abbd855e24146dd05a432b2bf3ea6d28dfef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252772"
---
# <a name="jet_snprog-structure"></a>JET_SNPROG estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_snprog-structure"></a>JET_SNPROG estructura

La **JET_SNPROG** estructura contiene información sobre el progreso de una operación de ejecución larga. Cuando se llama a la función de devolución de llamada para notificar el estado de la operación y la operación sigue en curso, el último parámetro de la función de devolución de llamada es un puntero a una **JET_SNPROG** estructura.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura **JET_SNPROG,** en bytes. Este valor confirma la presencia de los campos siguientes.

**cunitDone**

Número de unidades de trabajo que ya se han completado durante la función de larga duración.

**cunitTotal**

Número de unidades de trabajo que deben completarse. Este valor siempre debe ser mayor o igual que **cunitDone.**

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>

