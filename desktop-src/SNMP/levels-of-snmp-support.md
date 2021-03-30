---
title: Niveles de compatibilidad con SNMP
description: La implementación de Microsoft WinSNMP proporciona compatibilidad con las comunicaciones SNMP de nivel 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148770"
---
# <a name="levels-of-snmp-support"></a>Niveles de compatibilidad con SNMP

La implementación de Microsoft WinSNMP proporciona compatibilidad con las comunicaciones SNMP de nivel 2. El nivel 2 es compatible con el protocolo SNMPv2 estándar de Internet Engineering Task Force (IETF), tal y como se define en RFC 1902-1908. También admite el contenedor de mensajes basado en la comunidad, tal y como se define en RFC 1901 (SNMPv2C).

La compatibilidad con las comunicaciones de nivel 2 incluye servicios de codificación y descodificación de mensajes, anteriormente denominado compatibilidad de comunicaciones de nivel 0 en la versión 1.1 de WinSNMP. El nivel 2 también es compatible con todas las operaciones de protocolo SNMPv1, anteriormente denominadas compatibilidad de comunicaciones de nivel 1 en la versión 1.1 de WinSNMP.

La implementación de devuelve el nivel máximo de comunicaciones SNMP que admite en respuesta a una llamada de la aplicación WinSNMP a la función [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .

Si la aplicación WinSNMP usa la implementación de para la codificación y descodificación de mensajes SNMP, la aplicación debe realizar las transformaciones necesarias que la implementación habría realizado. Esto incluye la traducción de las capturas de SNMPv1 devueltas por una llamada a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) , a las capturas de SNMPv2c. También incluye la conversión de tipos de PDU definidos por SNMPv1 en el tipo de PDU correspondiente definido por SNMPv2C, de acuerdo con RFC 1908.

 

 




