---
title: Grupos en servidores miembro y Windows 2000 Professional
description: En los servidores miembro y equipos que ejecutan Windows 2000 Professional, hay una base de datos de seguridad local.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Grupos en servidores miembro y Windows 2000 Professional AD
- grupos AD, grupos en servidores miembro y Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356724"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>Grupos en servidores miembro y Windows 2000 Professional

En los servidores miembro y equipos que ejecutan Windows 2000 Professional, hay una base de datos de seguridad local. Esta base de datos de seguridad local puede contener su propio usuario local y grupos locales cuyo ámbito sea solo el equipo determinado en el que se crean. Al administrar estos tipos de usuarios y grupos en servidores miembro y equipos que ejecutan Windows NT Workstation o Windows 2000 Professional, use el proveedor de Winnt.

Cuando un servidor miembro o un equipo que se ejecuta en Windows 2000 Professional o Windows 2000 Professional es miembro de un dominio de Windows 2000, los grupos o usuarios del dominio se pueden usar en la base de datos de seguridad local para conceder derechos a ese grupo en ese equipo en particular.

Al administrar grupos en un dominio de Windows 2000 mediante ADSI, use el proveedor LDAP. Al administrar grupos en servidores miembro y equipos que ejecutan Windows NT Workstation o Windows 2000 Professional, use el proveedor de Winnt.

Debe enlazar, al menos una instancia, a cada proveedor: 1) enlazar con el proveedor LDAP para recuperar el ADsPath al grupo o usuario que desea agregar a un grupo en la base de datos local y 2) enlazar con el proveedor WinNT para agregar ese usuario o grupo a un grupo local.

 

 




