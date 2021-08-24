---
title: Registros de recursos
description: Obtenga información sobre los registros de recursos. Un registro de recursos es la unidad de entrada de información en los archivos de zona DNS, que se usa para resolver todas las consultas DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606d74f41e18fefa144ff21d3ed88d9683938304b0c8aa0bc7d94e2fbaa624cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825065"
---
# <a name="resource-records"></a>Registros de recursos

Un registro de recursos, conocido normalmente como RR, es la unidad de entrada de información en los archivos de zona DNS. Las RR son los bloques de creación básicos de la información ip y el nombre de host y se usan para resolver todas las consultas DNS. Los registros de recursos existen tantos tipos como para proporcionar servicios extendidos de resolución de nombres.

Los distintos tipos de RR tienen formatos diferentes, ya que contienen datos diferentes. Sin embargo, en general, muchas RR comparten un formato común, como se muestra en el ejemplo de registros de recursos de dirección siguientes. En el ejemplo ficticio siguiente se explican los campos que se encuentran en un registro de recursos A:

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   El primer campo (microsoft.com) denota el propietario.
-   El segundo campo (600) es el parámetro de período de vida (TTL), en segundos.
-   El tercer campo (IN) es el campo de clase que representa la familia de protocolos, que es casi siempre IN, para la clase de Internet.
-   El cuarto campo (A) es el tipo de recurso que el RR representa.
-   El quinto campo (150.150.150.1) son los datos de recursos o RDATA. Este campo es un tipo de variable que proporciona información adecuada para el tipo de recurso; En este caso, es una dirección IP de 32 bits.

Los siguientes tipos de registro de recursos se usan normalmente en DNS:

-   Inicio de autoridad (SOA)
-   Servidor de nombres (NS)
-   [*Registro de puntero*](p-gly.md) (PTR)
-   Dirección (A)
-   Dirección IPv6 (AAAA)
-   Intercambio de correo (MX)
-   [*Nombre canónico*](c-gly.md) (CNAME)
-   Windows Internet Naming Service (WINS)
-   Búsqueda inversa wins (WINSR)

Hay muchos otros tipos de registros de recursos en DNS. Para obtener más información, vea [Referencia del proveedor WMI de DNS.](dns-wmi-provider-reference.md)

 

 




