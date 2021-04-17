---
description: Una vez que un controlador de dispositivo ha convertido un archivo de diario completo en comandos de dispositivo sin formato, el archivo de comandos convertidos se pasa de nuevo al administrador de trabajos de impresión.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitores de Puerto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706639"
---
# <a name="port-monitors"></a>Monitores de Puerto

Una vez que un controlador de dispositivo ha convertido un archivo de diario completo en comandos de dispositivo sin formato, el archivo de comandos convertidos se pasa de nuevo al administrador de trabajos de impresión. El administrador de trabajos de impresión envía estos comandos de bajo nivel a un monitor. Un monitor de puerto es un archivo. dll que pasa los comandos de dispositivo sin formato a través de la red, a través de un puerto paralelo o a través de un puerto serie al dispositivo de impresora. Se pueden instalar monitores de Puerto personalizados para permitir el paso de datos del dispositivo a través de otros puertos de comunicación.

Utilice las siguientes funciones para trabajar con monitores de puerto.



| Función                               | Descripción                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | Instala un monitor de puerto local y vincula los archivos de configuración, datos y supervisión. |
| [**DeleteMonitor**](deletemonitor.md) | Quita un monitor de Puerto agregado por la función [**AddMonitor**](addmonitor.md) .      |
| [**EnumMonitors**](enummonitors.md)   | Enumera los monitores de Puerto instalados en un servidor especificado.                       |



 

 

 



