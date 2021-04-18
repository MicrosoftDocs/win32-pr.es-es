---
title: Consideraciones de seguridad del Sistema de colores de Windows
description: Consideraciones de seguridad del Sistema de colores de Windows
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Sistema de color de Windows (WCS), seguridad
- WCS (sistema de colores de Windows), seguridad
- Administración del color de imagen, seguridad
- Administración del color, seguridad
- seguridad para el sistema de colores de Windows (WCS)
- Módulo de administración del color (CMM)
- CMM (módulo de administración del color)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef47ada0c233900f6e56a1e438d411a2ae84abd3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721368"
---
# <a name="security-considerations-windows-color-system"></a>Consideraciones de seguridad: sistema de color de Windows

En este documento se proporciona información sobre las consideraciones de seguridad relacionadas con la administración del color de imagen. En este documento no se proporciona todo lo que necesita saber acerca de los problemas de seguridad, sino que debe usarlo como punto de partida y referencia para esta área tecnológica.

## <a name="non-microsoft-cmms-can-run-in-system-context"></a>Los CMMs que no son de Microsoft pueden ejecutarse en el contexto del sistema

Los módulos de administración de color (CMMs) que no son de Microsoft deben tratarse como controladores de impresora que no son de Microsoft, ya que tienen la posibilidad de ejecutarse en un contexto del sistema para las operaciones de impresión.
