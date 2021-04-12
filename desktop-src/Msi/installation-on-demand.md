---
description: Con la tecnología de instalación tradicional, es necesario salir de una aplicación y volver a ejecutar el programa de instalación para realizar una tarea de instalación.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Instalación a petición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f25c83135a0497d09aa0a7800a1272105d0db1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277172"
---
# <a name="installation-on-demand"></a>Instalación a petición

Con la tecnología de instalación tradicional, es necesario salir de una aplicación y volver a ejecutar el programa de instalación para realizar una tarea de instalación. Esto suele producirse cuando un usuario deseaba una característica o producto no elegido durante la primera ejecución del programa de instalación. A menudo, esto hizo que el proceso de configuración del producto no sea eficaz, ya que requería que el usuario produjera la funcionalidad necesaria antes de usar el producto.

La instalación a petición permite ofrecer funcionalidad a los usuarios y las aplicaciones en ausencia de los propios archivos. Esta noción se conoce como anuncio. El Windows Installer tiene la capacidad de anunciar la funcionalidad y realizar la instalación a petición de características de aplicaciones o productos completos posibles. Cuando un usuario o una aplicación activa una característica o un producto anunciado, el instalador continúa con la instalación de los componentes necesarios. Esto acorta el proceso de configuración, ya que se puede tener acceso a la funcionalidad adicional sin tener que salir y volver a ejecutar otro procedimiento de instalación.

Cuando un producto usa el instalador, un usuario puede elegir en el momento de la instalación Qué características o aplicaciones desea instalar y cuáles anunciar. Después, si durante la ejecución de una aplicación el usuario solicita una característica anunciada que no se ha instalado todavía, la aplicación llama al instalador para establecer una instalación de nivel de característica Just-in-Time de los archivos necesarios. Si el usuario activa un producto anunciado que todavía no se ha instalado, el sistema operativo llama al instalador para activar una instalación del nivel de producto Just-in-Time.

El [anuncio](advertisement.md) y la instalación a petición también pueden facilitar la administración del sistema, ya que permite a los administradores designar aplicaciones según sea necesario u opcional para los distintos grupos de usuarios. Hay dos tipos de anuncios que se conocen como "asignación" y "publicación". Si un administrador asigna una aplicación a un grupo, estos usuarios pueden instalar la aplicación a petición. Sin embargo, si el administrador publica la aplicación en el grupo, no aparece ningún punto de entrada a estos usuarios y la instalación a petición solo se activa si otra aplicación activa la aplicación publicada.

 

 



