---
title: Directrices de creación para archivos MIDI
description: Directrices de creación para archivos MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Interfaz digital de instrumentación musical (MIDI),instrucciones de creación de archivos
- MIDI (Interfaz digital de instrumentación de música), instrucciones de creación de archivos
- crear archivos MIDI, directrices de creación de archivos
- asignaciones de revisiones estándar de MIDI
- asignaciones de claves ESTÁNDAR DE MIDI
- Interfaz digital de instrumentar música (MIDI), asignaciones de revisiones estándar
- MIDI (Interfaz digital de instrumentar música), asignaciones de revisiones estándar
- Interfaz digital de instrumentar música (MIDI), asignaciones de claves estándar
- MIDI (Interfaz digital de instrumentar música), asignaciones de claves estándar
- crear archivos MIDI, asignaciones de revisiones estándar
- crear archivos MIDI, asignaciones de claves estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe148c2fe1bb562aad994608a8c87c35e84bccb7d63ba1bc3ee3e5dd3bbc56a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065645"
---
# <a name="authoring-guidelines-for-midi-files"></a>Directrices de creación para archivos MIDI

Siga estas instrucciones para crear archivos MIDI independientes del dispositivo para Windows:

-   Use las [asignaciones de revisiones estándar de MIDI](standard-midi-patch-assignments.md) y las [asignaciones de claves ESTÁNDAR DE MIDI](standard-midi-key-assignments.md).
-   Envíe siempre un mensaje de cambio de programa a un canal para seleccionar una revisión antes de enviar otros mensajes a ese canal. Para los dos canales de televisión (10 y 16), seleccione el número de programa 0.
-   Siga siempre un mensaje de cambio del programa MIDI con un mensaje de controlador de volumen principal de MIDI (número de controlador 7) para establecer el volumen relativo de la revisión.
-   Use un valor de 80 (0x50) para el controlador de volumen principal para niveles de escucha normales. Para niveles más silenciosos o más altos, puede usar valores inferiores o superiores.
-   Use solo los siguientes mensajes MIDI: nota-on con velocidad, nota off, cambio de programa, pitch, volumen principal (controlador 7) y el controlador 64. Los síntesis internos son necesarios para responder a estos mensajes y la mayoría de los instrumentos musicales DE MES también responden a ellos.

 

 




