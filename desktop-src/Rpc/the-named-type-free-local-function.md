---
title: La función named_type_free_local
description: El código auxiliar llama a \_ la \_ función local de tipo Free para liberar la memoria asignada por una llamada al tipo con nombre \_ en la \_ \_ rutina local.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774623"
---
# <a name="the-named_type_free_local-function"></a>La \_ \_ función local de tipo con nombre Free \_

El código auxiliar llama a la función **\_ \_ local de tipo Free** para liberar la memoria asignada por una llamada al [tipo con nombre en la rutina \_ \_ \_ local](the-named-type-to-local-function.md) . No libera la memoria asignada por el código auxiliar. El prototipo de función se define como:

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

El parámetro es un puntero a la memoria asignada por el **tipo con nombre \_ \_ a \_ local**.

 

 




