---
title: IAgentCharacter detener
description: IAgentCharacter detener
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418956"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter:: Stop

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Detiene la animación especificada (solicitud) y la quita de la cola de animaciones del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

IDENTIFICADOR de la solicitud que se va a detener.

</dd> </dl>

**Detener** también puede usarse para detener cualquier llamada de [**preparación**](iagentcharacter--prepare.md) en cola.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::P reparer**](iagentcharacter--prepare.md), [ **IAgentCharacter:: stopAll**](iagentcharacter--stopall.md)


 

 




