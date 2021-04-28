---
title: Caché en modo kernel
description: Caché en modo kernel
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c409b00da03c0550899f5d26c4e6a0fa215118
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090893"
---
# <a name="kernel-mode-cache"></a>Caché en modo kernel

La API del servidor HTTP versión 2.0 permite a las aplicaciones almacenar en caché respuestas con contenido estático en modo kernel. Se logra un mayor rendimiento cuando las solicitudes se atendidas desde la caché del kernel sin pasar al modo de usuario.

La API del servidor HTTP aplica las configuraciones de propiedad adecuadas a todas las solicitudes atendidas desde la caché del kernel, incluidas las respuestas de registro. Sin embargo, las solicitudes que requieren autenticación no se atendidas desde la memoria caché.

La API del servidor HTTP limita la caché del modo kernel a las solicitudes que cumplen las condiciones siguientes:

-   El verbo de solicitud es GET y se recibe toda la solicitud.
-   La solicitud no debe tener un cuerpo de entidad.
-   El protocolo HTTP es la versión 1.0 o posterior.
-   El encabezado "Translate: f" no está presente.
-   Los encabezados expect distintos de "Expect: 100-Continue" no están presentes.
-   El encabezado de autorización no está presente.
-   Los encabezados Range If-Range no están presentes.

Además de las restricciones de la solicitud, la respuesta también debe cumplir las condiciones siguientes:

-   El tamaño de respuesta está limitado a 256 KB, de forma predeterminada. Para cambiar el tamaño de la respuesta almacenada en caché, establezca el valor del Registro **UriMaxUriBytes** en el número necesario de bytes.

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   Toda la respuesta debe proporcionarse en una sola llamada a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).
-   No se debe suprimir el encabezado de fecha de la respuesta.
-   Si el encabezado modificado por última vez está presente, el valor del encabezado debe tener la sintaxis correcta. El valor de hora de este encabezado se usa para la comprobación del control de caché.
-   La caché en modo kernel tiene espacio suficiente para almacenar la respuesta.

De forma predeterminada, la caché de respuestas en modo kernel está habilitada. Si no se cumple alguna de las condiciones de la solicitud o respuesta enumeradas anteriormente, se enviará la respuesta, pero no se almacenará en caché. En la API de servidor HTTP versión 2.0, [**HttpSendHttpResponse incluye**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) un parámetro *pCachePolicy* opcional para pasar la estructura [**HTTP CACHE \_ \_ POLICY.**](/windows/desktop/api/Http/ns-http-http_cache_policy) Las aplicaciones usan la estructura de directivas de caché para configurar la memoria caché.

 

 




