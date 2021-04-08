---
title: Animaciones del agente de Microsoft para el carácter Peedy
description: Animaciones del agente de Microsoft para el carácter Peedy
ms.assetid: 335d915c-9cae-4850-a6bf-66ad78d533ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e064063b322bc6549d91b5fce35bdbc491a5a3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791427"
---
# <a name="microsoft-agent-animations-for-peedy-character"></a>Animaciones del agente de Microsoft para el carácter Peedy

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El [carácter Peedy del agente de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=bd3c4655-79e4-4791-ab9d-abc7bbd133ef) es un trabajo con copyright de Microsoft Corporation.

Peedy admite las animaciones que se muestran en la tabla siguiente. Consulte [Programming the Microsoft Agent Server Interface](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) and [Programming the Microsoft Agent control](programming-the-microsoft-agent-control.md) para obtener información sobre cómo llamar a las animaciones del carácter.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método de [**preparación**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor [**Get**](get-method.md) o del servidor, tenga en cuenta cómo se descargarán. En lugar de descargar todas las animaciones a la vez, puede que desee recuperar primero las animaciones de estado de **visualización** y de **habla** . Esto le permitirá mostrar el carácter rápidamente y hacer que hable mientras se desconectan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de animación y de caracteres se cargan correctamente, use el evento [**RequestComplete**](requestcomplete-event.md) . Si se produce un error en una solicitud de carga, puede volver a intentar cargar los datos o mostrar un mensaje adecuado.

Si la animación **devuelta** de una animación se define mediante ramas de salida, no es necesario llamarlo explícitamente. El agente reproduce automáticamente la animación **devuelta** antes de la siguiente animación. Sin embargo, si se muestra una animación de **devolución** , debe llamar a la animación con el método [**Play**](play-method.md) antes de otra animación para proporcionar una transición suave. Si no aparece ninguna animación **devuelta** , la animación finaliza normalmente sin necesidad de una animación transitoria.

Si tiene acceso a estas animaciones de caracteres mediante el protocolo HTTP y el método de [**preparación**](/windows/desktop/lwef/iagentcharacter--prepare) del servidor [**Get**](get-method.md) o del servidor, tenga en cuenta cómo se descargarán. En lugar de descargar todas las animaciones a la vez, puede que desee recuperar primero las animaciones de estado de **visualización** y de **habla** . Esto le permitirá mostrar el carácter rápidamente y hacer que hable mientras se desconectan otras animaciones de forma asincrónica. Además, para asegurarse de que los datos de animación y de caracteres se cargan correctamente, use el evento [**RequestComplete**](requestcomplete-event.md) . Si se produce un error en una solicitud de carga, puede volver a intentar cargar los datos o mostrar un mensaje adecuado.

El archivo de caracteres incluye efectos sonoros para algunas animaciones, como se indica en la tabla siguiente. Los efectos de sonido solo se reproducen si esta opción está habilitada en la hoja de propiedades del agente de Microsoft. También puede deshabilitar los efectos sonoros en la aplicación.



| Animación                  | Devolver animación         | Admite hablar | Efectos sonoros | Asignado a estado                            | Descripción                                            |
|----------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------------|
| **Confirmación**            | None                     | No                | **No**        | None                                         | Encabezado nodos                                              |
| **Alerta**                  | Sí, usar ramas de salida | Sí               | **No**        | **Escucha**                                | Activa y produce eyebrows                        |
| **Anuncie**               | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | El avión del papel vuela y dobla                    |
| **Blink**                  | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Parpadeos                                            |
| **Confusión**               | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Ojos, girar                                       |
| **Felicitar**           | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Muestra la cinta azul                                   |
| **Rechazar**                | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Sacudida                                            |
| **DoMagic1**               | None                     | Sí               | **Sí**       | None                                         | Eleva la varita mágica                                      |
| **DoMagic2**               | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Se reduce la varita, aparecen nubes                             |
| **DontRecognize**          | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Agita el cabezal y mantiene la lengüeta                      |
| **Explicación**                | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Extiende los brazos al lado                                   |
| **GestureDown**            | Sí, usar ramas de salida | Sí               | **No**        | **GesturingDown**                            | Gestos hacia abajo                                          |
| **GestureLeft**            | Sí, usar ramas de salida | Sí               | **No**        | **GesturingLeft**                            | Gestos a la izquierda                                          |
| **GestureRight**           | Sí, usar ramas de salida | Sí               | **No**        | **GesturingRight**                           | Gestos a la derecha                                         |
| **GestureUp**              | Sí, usar ramas de salida | Sí               | **No**        | **GesturingUp**                              | Gestos hacia arriba                                            |
| **GetAttention**           | **GetAttentionReturn**   | Sí               | **Sí**       | None                                         | Se salta con alas sobreajustadas                       |
| **GetAttentionContinued**  | **GetAttentionReturn**   | Sí               | **Sí**       | None                                         | Se salta de nuevo con las alas deselásticas                 |
| **GetAttentionReturn**     | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **Acogida**                  | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Bow                                                   |
| **Audición \_ 1**             | None                     | No                | **No**        | **Oído**                                  | Inclinación derecha (animación en \* bucle)                 |
| **Audición \_ 2**             | None                     | No                | **No**        | **Oído**                                  | Inclina la izquierda ( \* animación en bucle)                  |
| **Audición \_ 3**             | None                     | No                | **No**        | **Oído**                                  | Convierte a la derecha a la izquierda ( \* animación en bucle)       |
| **Ocultar**                   | None                     | No                | **Sí**       | **Conde**                                   | Desaparecedo                                             |
| **Idle1 \_ 1**               | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Toma respiración                                           |
| **Idle1 \_ 2**               | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Mirada a la derecha y a los parpadeos                               |
| **Idle1 \_ 3**               | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Mirar a la izquierda y a los parpadeos                                |
| **Idle1 \_ 4**               | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | El vistazo y los parpadeos                                  |
| **Idle1 \_ 5**               | None                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Vista rápida y parpadeo                                |
| **Idle2 \_ 1**               | Sí, usar ramas de salida | No                | **No**        | **IdlingLevel2**                             | Coloca en vidrios                                     |
| **Idle2 \_ 2**               | None                     | No                | **Sí**       | **IdlingLevel2**                             | Consume un atacante                                         |
| **Idle3 \_ 1**               | None                     | No                | **Sí**       | **IdlingLevel3**                             | Yawns                                                  |
| **Idle3 \_ 2**               | Sí, usar ramas de salida | No                | **Sí**       | **IdlingLevel3**                             | Está en suspensión ( \* animación en bucle)                     |
| **Idle3 \_ 3**               | Sí, usar ramas de salida | No                | **No**        | **IdlingLevel3**                             | Escuchas en música ( \* animación en bucle)                 |
| **LookDownLookDownReturn** |                          | No                | **No**        | None                                         | Buscar                                             |
| **LookDownBlink**          | **LookDownReturn**       | No                | **Sí**       | None                                         | Parpadea al mirar                                    |
| **LookDownReturn**         | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **LookDownLeft**           | **LookDownLeftReturn**   | No                | **No**        | None                                         | Aparece a la izquierda                                        |
| **LookDownLeftBlink**      | **LookDownLeftReturn**   | No                | **Sí**       | None                                         | Parpadea al mirar a la izquierda                               |
| **LookDownLeftReturn**     | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **LookDownRight**          | **LookDownRightReturn**  | No                | **No**        | None                                         | Busca hacia abajo                                       |
| **LookDownRightBlink**     | **LookDownRightReturn**  | No                | **Sí**       | None                                         | Parpadea al mirar a la derecha                              |
| **LookDownRightReturn**    | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **LookLeft**               | **LookLeftReturn**       | Sí               | **No**        | None                                         | Aparece a la izquierda                                             |
| **LookLeftBlink**          | **LookLeftReturn**       | Sí               | **Sí**       | None                                         | Parpadea al mirar a la izquierda                                    |
| **LookLeftReturn**         | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **LookRight**              | **LookRightReturn**      | Sí               | **No**        | None                                         | Parece correcto                                            |
| **LookRightBlink**         | **LookRightReturn**      | Sí               | **Sí**       | None                                         | Parpadea al mirar a la derecha                                   |
| **LookRightReturn**        | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **Buscar**                 | **LookUpReturn**         | No                | **No**        | None                                         | Busca                                               |
| **LookUpBlink**            | **LookUpReturn**         | No                | **Sí**       | None                                         | Parpadeo de búsqueda                                      |
| **LookUpReturn**           | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **LookUpLeft**             | **LookUpLeftReturn**     | No                | **No**        | None                                         | Busca hacia la izquierda                                          |
| **LookUpLeftBlink**        | **LookUpLeftReturn**     | No                | **Sí**       | None                                         | Parpadea al buscar a la izquierda                                 |
| **LookUpLeftReturn**       | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **LookUpRight**            | **LookUpRightReturn**    | No                | **No**        | None                                         | Buscar a la derecha                                         |
| **LookUpRightBlink**       | **LookUpRightReturn**    | No                | **Sí**       | None                                         | Parpadea al buscar a la derecha                                |
| **LookUpRightReturn**      | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **Bajar**               | Sí, usar ramas de salida | No                | **Sí**       | **MovingDown**                               | Volar                                             |
| **MoveLeft**               | Sí, usar ramas de salida | No                | **Sí**       | **MovingLeft**                               | Volar a la izquierda                                             |
| **Anula**              | Sí, usar ramas de salida | No                | **Sí**       | **MovingRight**                              | Volar a la derecha                                            |
| **MoveUp**                 | Sí, usar ramas de salida | No                | **Sí**       | **MovingUp**                                 | Volar                                               |
| **Satisfechos**                | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Positivos                                                 |
| **Proceso**                | None                     | No                | **Sí**       | None                                         | Usa la calculadora                                        |
| **Processing**             | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Usa Calculator ( \* animación de bucle)                  |
| **Lectura**                   | **ReadReturn**           | Sí               | **Sí**       | None                                         | Abre la revista, Lee y busca                     |
| **ReadContinued**          | **ReadReturn**           | Sí               | **Sí**       | None                                         | Lee y busca                                     |
| **ReadReturn**             | None                     | No                | **Sí**       | None                                         | Vuelve a la posición neutra                            |
| **Leía**                | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Lecturas ( \* animación en bucle)                            |
| **RestPose**               | None                     | Sí               | **No**        | **Habla**                                 | Posición neutra                                       |
| **San**                    | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Sad (expresión)                                         |
| **Búsqueda**                 | None                     | No                | **Sí**       | None                                         | Revela telescopio y gira                          |
| **Buscándol**              | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Revela telescopio y gira ( \* animación en bucle)    |
| **Mostrar**                   | None                     | No                | **Sí**       | **Mostrando**                                  | Volar                                               |
| **StartListening**         | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Coloca la mano en el oído                                       |
| **StopListening**          | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Pone manos a los oídos                                     |
| **Sugerir**                | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Muestra bombilla                                    |
| **Sorprendido**              | Sí, usar ramas de salida | Sí               | **Sí**       | None                                         | Aspecto sorprendido                                        |
| **Opina**                  | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Busca en la superficie                             |
| **Pensando**               | None                     | No                | **No**        | None                                         | Busca en la superficie (animación en \* bucle)       |
| **Seguro**              | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Se inclina a la derecha y Shrugs                              |
| **Ondas**                   | Sí, usar ramas de salida | Sí               | **No**        | None                                         | Ondas                                                  |
| **Escritura**                  | **WriteReturn**          | Sí               | **Sí**       | None                                         | Saca el lápiz y el panel, escribe y busca          |
| **WriteContinued**         | **WriteReturn**          | Sí               | **Sí**       | None                                         | Escribe y busca                                    |
| **WriteReturn**            | None                     | No                | **No**        | None                                         | Vuelve a la posición neutra                            |
| **Escribir**                | Sí, usar ramas de salida | No                | **Sí**       | None                                         | Saca el lápiz y el panel, escribe ( \* animación en bucle) |



 

\* Si reproduce una animación de bucle, debe utilizar [**detener**](stop-method.md) para borrarla antes de que se reproduzcan otras animaciones en la cola del carácter.

 

