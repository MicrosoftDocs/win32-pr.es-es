---
title: Componentes de la arquitectura del enrutador
description: La documentación de administración del enrutador hace referencia frecuente a los siguientes componentes del enrutador.
ms.assetid: 841a5728-39d6-4bd7-a41a-6543b4ed9985
keywords:
- enrutadores RRAS, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb0cc69de5402b03550873b3b052f6329b5238
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486795"
---
# <a name="components-of-the-router-architecture"></a>Componentes de la arquitectura del enrutador

La documentación de administración del enrutador hace referencia frecuente a los siguientes componentes del enrutador.

Dynamic interface Manager (DIM)

Todas las funciones de administración del enrutador pasan a través de DIM. Dependiendo de la naturaleza de la función, DIM puede pasar la llamada a uno de los administradores de enrutadores. Las funciones que solo tratan las interfaces se controlan mediante DIM. Si la función afecta a los protocolos de enrutamiento, DIM llamará al administrador de enrutador para el transporte correspondiente a ese protocolo. Por ejemplo, si la función afecta al Protocolo de la ruta de acceso más corta (OSPF) abierta, DIM llamará al administrador de enrutadores IP, ya que OSPF es un protocolo de enrutamiento IP.

Administradores de enrutadores

Cada transporte enrutable que encaja en la arquitectura del enrutador tiene su propio administrador de enrutadores. Actualmente existen administradores de enrutadores para los transportes IP y IPX. Los administradores de enrutadores administran los protocolos de enrutador y otros tipos de clientes de enrutamiento que se ejecutan en interfaces en el equipo local.

Protocolos de enrutamiento y otros clientes

Los clientes son proveedores de servicios que funcionan dentro del marco de la arquitectura del enrutador. Los protocolos de enrutamiento son un tipo de cliente que es compatible con el enrutador.

Los clientes son específicos de un transporte enrutable determinado: IP o IPX. Los protocolos de enrutamiento para el transporte IP incluyen primero la ruta de acceso más corta (OSPF) y el protocolo de información de enrutamiento (RIP). Algunos ejemplos de protocolos de enrutamiento IPX son protocolo de anuncio de servicio (SAP) y RIP para IPX. Un ejemplo de un cliente que no es un protocolo de enrutamiento es la traducción de direcciones de red (NAT) para IP.

La interfaz entre el administrador de enrutadores y un cliente se describe en la sección [interfaz del Protocolo de enrutamiento](about-routing-protocol-interface.md). Todos los clientes se ajustan a esta interfaz. Mediante esta interfaz, los proveedores pueden implementar sus propios clientes que son compatibles con el enrutador.

[Interfaces](interfaces.md)

Una interfaz es una conexión a una red externa. Cada interfaz se identifica mediante un *Índice* de interfaz único. Las interfaces son entidades lógicas; los clientes de enrutador, como NAT o OSPF, tratan todos los tipos de interfaces de forma similar. Sin embargo, en lo que respecta a la implementación, una interfaz puede representar una conexión dedicada (como una red de área local (LAN)) o una conexión de acceso telefónico no dedicada (como una conexión PPP a una red de área extensa (WAN)).

En el caso de una interfaz LAN, la interfaz corresponde a un dispositivo físico real del equipo, un adaptador de LAN. En el caso de una interfaz WAN, la interfaz se asigna a un puerto en el momento en que se establece una conexión. El puerto puede ser un puerto COM, un puerto paralelo o un puerto virtual (para túneles como PPTP y L2TP).

Las interfaces WAN tienen la calidad adicional de que normalmente reciben una dirección de red en el momento en que se establece una conexión. Por ejemplo, una interfaz WAN que usa PPP recibe su dirección de nivel de red del elemento remoto del mismo nivel durante el proceso de conexión. La recepción de una dirección de red como parte del proceso de conexión a veces se conoce como *enlace en tiempo de ejecución*.

 

 




