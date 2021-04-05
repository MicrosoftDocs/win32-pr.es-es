---
description: 'Más información sobre: columnas definidas por el usuario'
title: Columnas definidas por el usuario
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082375"
---
# <a name="user-defined-columns"></a>Columnas definidas por el usuario


_**Se aplica a:** Windows | Windows Server_

## <a name="user-defined-columns"></a>Columnas definidas por el usuario

Las columnas definidas por el usuario son columnas cuyos valores predeterminados se proporcionan mediante una función de devolución de llamada. Estas columnas siempre se etiquetan y se establecen en el valor calculado por la función de devolución de llamada. Este valor debe ser estable para cada fila de la tabla. La función de devolución de llamada solo se usa cuando la aplicación o el motor de base de datos debe leer el valor de la columna de una fila determinada. La aplicación tiene la opción de invalidar el valor predeterminado y establecer un valor específico en la columna. Cuando se invalida el valor predeterminado en las columnas, utiliza el espacio de la fila; de lo contrario, las columnas predeterminadas definidas por el usuario no usan espacio en el registro.

La opción valores predeterminados definidos por el usuario se establece en el miembro **grbit** de la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) en la llamada a [JetAddColumn](./jetaddcolumn-function.md). El parámetro *pvDefault* de la función [JetAddColumn](./jetaddcolumn-function.md) apunta a una estructura [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , que contiene el nombre de la función de devolución de llamada en el miembro **szCallback** , y los datos que se pasan a la devolución de llamada en el miembro **pbUserData** .
