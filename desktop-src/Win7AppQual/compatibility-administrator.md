---
description: .
ms.assetid: 72a77e83-ab18-438c-af11-fa6d55bf0180
title: Administrador de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abde760ca7324aec18f0576a7f04e3a4c5db2d22
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314988"
---
# <a name="compatibility-administrator"></a>Administrador de compatibilidad

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes:** Windows 2000, Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="description"></a>Descripción

La herramienta de administración de compatibilidad, proporcionada por el kit de herramientas de compatibilidad de aplicaciones (ACT) le permite resolver muchos de los posibles problemas de compatibilidad de aplicaciones, antes de implementar una nueva versión de Windows en su organización, por:

-   Proporcionar correcciones de compatibilidad individuales, modos de compatibilidad y mensajes de AppHelp que puede usar para resolver problemas de compatibilidad específicos
-   Permitir la creación de correcciones de compatibilidad personalizadas, modos de compatibilidad, mensajes de AppHelp y bases de datos de compatibilidad
-   Proporcionar una herramienta de consulta que permite buscar correcciones instaladas en los equipos locales

## <a name="usage"></a>Uso

En el diagrama de flujo siguiente se muestran los pasos necesarios para usar el administrador de compatibilidad con el fin de crear las correcciones de compatibilidad, los modos de compatibilidad y los mensajes de AppHelp.



|                                            |          |                                                                                            |          |                                                     |          |                                                                             |
|--------------------------------------------|----------|--------------------------------------------------------------------------------------------|----------|-----------------------------------------------------|----------|-----------------------------------------------------------------------------|
| Crear una nueva base de datos de compatibilidad (. sdb) | **>** | Seleccione la aplicación y, a continuación, seleccione las correcciones de compatibilidad que se aplicarán a la aplicación. | **>** | Prueba de la aplicación con la nueva corrección de compatibilidad | **>** | Guarde la base de datos de compatibilidad y, a continuación, implemente la corrección en su corporación |



 

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Descarga del kit de herramientas de compatibilidad de aplicaciones](/windows-hardware/get-started/adk-install)
-   [Usar el administrador de compatibilidad](/previous-versions/windows/it-pro/windows-7/cc749034(v=ws.10))
-   [Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [Prueba y mitigación de problemas con las herramientas de desarrollo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))

 

 
