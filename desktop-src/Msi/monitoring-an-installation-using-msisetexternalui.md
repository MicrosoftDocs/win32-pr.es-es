---
description: Los autores de paquetes pueden supervisar los mensajes de Windows Installer internos a través de la creación de una aplicación ejecutable que contenga un controlador de devolución de llamada para recibir los mensajes y la funcionalidad para iniciar una instalación.
ms.assetid: 0aa8a2d6-f519-4d87-a28f-a11cb546bff5
title: Supervisión de una instalación mediante MsiSetExternalUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cc461845a6db1fab4ede22581093c46c0e76e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669678"
---
# <a name="monitoring-an-installation-using-msisetexternalui"></a>Supervisión de una instalación mediante MsiSetExternalUI

Los autores de paquetes pueden supervisar los mensajes de Windows Installer internos a través de la creación de una aplicación ejecutable que contenga un controlador de devolución de llamada para recibir los mensajes y la funcionalidad para iniciar una instalación.

El controlador de devolución de llamada se ajusta al \_ prototipo del controlador INSTALLUI y se pasa un puntero a este controlador de devolución de llamada a [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia). Una vez que la instalación se ha iniciado mediante una llamada a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta), el controlador de devolución de llamada captura los mensajes de instalación y el autor del paquete puede mostrar u omitir de forma selectiva alguno o todos los mensajes.

Para obtener más información, vea [controlar los mensajes de progreso mediante MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md), [devolver valores de un controlador de interfaz de usuario externo](returning-values-from-an-external-user-interface-handler.md)y [analizar mensajes de Windows Installer](parsing-windows-installer-messages.md).

Para obtener más información sobre el uso de un controlador externo basado en registros, vea [supervisar una instalación mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

 

 



