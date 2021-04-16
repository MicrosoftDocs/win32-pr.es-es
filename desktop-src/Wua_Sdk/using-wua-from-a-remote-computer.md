---
description: El usuario puede usar la API del agente de Windows Update (WUA) en un equipo remoto o en una aplicación que se ejecuta en un equipo remoto. Sin embargo, el usuario o la aplicación remotos deben tener privilegios de administrador.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Usar WUA desde un equipo remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696238"
---
# <a name="using-wua-from-a-remote-computer"></a>Usar WUA desde un equipo remoto

El usuario puede usar la API del agente de Windows Update (WUA) en un equipo remoto o en una aplicación que se ejecuta en un equipo remoto. Sin embargo, el usuario o la aplicación remotos deben tener privilegios de administrador.

La lista siguiente contiene las interfaces que están disponibles para usuarios y aplicaciones remotos:

-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**ISearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [**IUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [**IUpdateIdentity**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [**IImageInformation**](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [**IStringCollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [**ICategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [**ICategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [**IUpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [**IUpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [**IUpdateDownloadContentCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [**IUpdateDownloadContent**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [**IUpdateServiceCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

La lista siguiente contiene las interfaces y las propiedades que no están disponibles para los usuarios y las aplicaciones remotos:

-   [**IUpdateSession::CreateUpdateDownloader**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [**IUpdateSession::CreateUpdateInstaller**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [**Propiedad WebProxy de IUpdateSession**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [**IUpdateSearcher::EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   La [**propiedad IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** es de solo lectura cuando se llama de forma remota).
-   [**IUpdate:: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [**IUpdate::CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IUpdate2::CopyToCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [**IWindowsDriverUpdate2::CopyToCache**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [**IUpdateServiceManager:: AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [**IUpdateServiceManager::RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [**IUpdateServiceManager::UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [**IAutomaticUpdate::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates:: resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::ShowSettingsDialog**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [**Propiedad de configuración de IAutomaticUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [**Propiedad ServiceEnabled de IAutomaticUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

Se deben agregar los siguientes puertos y excepciones a la configuración de Firewall de Windows para Windows Vista y Windows Server 2008 para que se llame a la API de WUA de forma remota.

<dl> <dt>

<span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Excepción 1
</dt> <dd> <dl> <dd>Puerto local: 135</dd> <dd>Puerto remoto: todos</dd> <dd>Número de protocolo: 6</dd> <dd>Ejecutable:% WINDIR% \\ system32 \\svchost.exe</dd> <dd>Servicio: RPCSS</dd> <dd>Privilegio remoto: administrador</dd> </dl> </dd> <dt>

<span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Excepción 2
</dt> <dd> <dl> <dd>Puerto local: RPC dinámico</dd> <dd>Puerto remoto: todos</dd> <dd>Número de protocolo: 6</dd> <dd>Ejecutable:% WINDIR% \\ system32 \\dllhost.exe</dd> <dd>Privilegio remoto: administrador</dd> </dl> </dd> </dl>

La lista siguiente contiene herramientas que se pueden usar para configurar el Firewall de Windows:

-   Firewall de Windows con complemento de seguridad avanzada
-   Directiva de grupo
-   Herramienta de línea de comandos Netsh advfirewall

Para obtener más información sobre cómo usar las herramientas para configurar las opciones del firewall de Windows, consulte [Introducción con firewall de Windows con seguridad avanzada](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).

 

 
