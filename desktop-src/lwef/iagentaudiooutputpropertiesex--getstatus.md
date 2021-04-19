---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380749"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx::GetStatus

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

Recupera el estado del canal de audio.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Estado del canal de salida de audio, que puede ser uno de los siguientes valores:



| Value                                                                         | Descripción                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **const unsigned short** **AUDIO STATUS AVAILABLE = \_ \_ 0;**<br/>         | El canal de salida de audio está disponible (no está ocupado).                                                              |
| **const unsigned short** **AUDIO STATUS \_ \_ NOAUDIO = 1;**<br/>           | No hay compatibilidad con la salida de audio; por ejemplo, porque no hay ninguna tarjeta de sonido.                             |
| **const unsigned short** **AUDIO STATUS \_ \_ DIMPENAUDIO = 2;**<br/>     | No se puede abrir el canal de salida de audio (está ocupado); por ejemplo, porque otra aplicación reproduce audio. |
| **const unsigned short** **AUDIO STATUS \_ \_ USERSPEAKING = 3;**<br/>      | El canal de salida de audio está ocupado porque el servidor está procesando la entrada de voz del usuario.                            |
| **const unsigned short** **AUDIO STATUS \_ \_ CHARACTERSPEAKING = 4;**<br/> | El canal de salida de audio está ocupado porque un carácter está hablando actualmente.                                    |
| **const unsigned short** **AUDIO STATUS \_ \_ SROVERRIDEABLE = 5;**<br/>    | El canal de salida de audio no está ocupado, pero está esperando la entrada de voz del usuario.                                 |
| **const unsigned short** **AUDIO STATUS ERROR = \_ \_ 6;**<br/>             | Hubo algún otro problema (desconocido) al intentar acceder al canal de salida de audio.                       |



 

</dd> </dl>

Esta configuración permite a la aplicación cliente consultar el estado del canal de salida de audio. Puede usarlo para determinar si el carácter habla o si intenta activar el modo de escucha (mediante **IAgentCharacterEx::Listen).**

 

 





