---
title: Información general de la API del servidor HTTP
description: En este tema se identifica una secuencia típica de operaciones que usan la API del servidor HTTP.
ms.assetid: 1245fd98-8370-4f1b-8c86-de9be5e678bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c99af3e4914c5496c2adea10b3ac658f75f3018
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685696"
---
# <a name="http-server-api-overview"></a>Información general de la API del servidor HTTP

La lista siguiente identifica una secuencia típica de operaciones que usan la API del servidor HTTP:

-   Inicialice la API del servidor HTTP mediante la función [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) .
-   Cree una cola de solicitudes con la función [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) .
-   Registre una o más direcciones URL mediante la función [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) .
-   Recibir solicitudes entrantes dirigidas a direcciones URL registradas mediante la función [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) y enviar respuestas http para estas solicitudes mediante la función [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) .
-   Opta Al enviar una respuesta, envíe un cuerpo de entidad adicional mediante la función [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) .
-   Realice operaciones de limpieza mediante las funciones [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl), [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) y [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) .

En operaciones que usan direcciones URL, tenga en cuenta que se trata de la dirección URL procesada incluida en el miembro **CookedUrl** de la estructura de la [**\_ solicitud HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) que se debe usar. No se trata de la dirección URL no procesada en el miembro **pRawUrl** , que es únicamente para fines estadísticos y de seguimiento.

Cada aplicación crea su propia cola de solicitudes. Una aplicación obtiene el identificador de la cola de solicitudes de [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle). Pasa este identificador a la función [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) para agregar una dirección URL a la cola de solicitudes. La aplicación recibe la notificación de una solicitud entrante y la recupera de la cola de solicitudes mediante una llamada a la función [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) con el identificador de la cola de solicitudes. Puede usar esta función para recibir los encabezados de solicitud o los encabezados y el cuerpo de la entidad. [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) también devuelve un identificador de solicitud (RequestId) para la solicitud recibida que es única para el identificador de solicitud.

> [!Note]  
> Es responsabilidad de la aplicación examinar todos los encabezados de solicitud pertinentes, incluidos los encabezados de negociación de contenido, si se usan, y las solicitudes erróneas según corresponda según el contenido del encabezado. La API de servidor HTTP solo garantiza que cada línea de encabezado termine correctamente y no contenga caracteres no válidos.

 

Utilice la función [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) con el identificador de la cola de solicitudes para recuperar las partes posteriores del cuerpo de la entidad de una solicitud, si hay alguna.

> [!Note]  
> La API del servidor HTTP descodifica mensajes fragmentados en el lado de recepción, pero no realiza una codificación fragmentada en el lado de envío. Si se requiere fragmentación en el lado de envío, la aplicación debe implementarla. Para obtener más información acerca de la codificación fragmentada, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

 

Utilice la función [**HttpReceiveClientCertificate**](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) con aplicaciones que sirven direcciones URL mediante un esquema seguro ("**https**") para recuperar la información del certificado del cliente de forma opcional.

Las respuestas se envían con la función [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) . Esta función usa el RequestId de la solicitud correspondiente para enviar la respuesta. Se puede enviar una respuesta en varias llamadas API a lo largo del tiempo mediante una llamada a la función [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) con el RequestId de la solicitud recibida originalmente.

> [!Note]  
> De forma predeterminada, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) usa "Microsoft-HTTPAPI/1.0" como el encabezado "Server:". Si una aplicación especifica un encabezado de servidor en una respuesta, ese valor se coloca como la primera parte del encabezado del servidor, seguido de un espacio y, a continuación, "Microsoft-HTTPAPI/1.0".

 

En general, la API del servidor HTTP oculta los detalles de la administración de conexiones y su establecimiento y desmontaje de las aplicaciones. Sin embargo, una aplicación puede detectar opcionalmente la finalización de una conexión mediante una llamada a [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect).

Las aplicaciones deben realizar la limpieza mediante los pasos siguientes:

-   Cuando la aplicación no escucha o responde a una dirección URL, la dirección URL se quita mediante la función [**HttpRemoveURL**](/windows/desktop/api/Http/nf-http-httpremoveurl) .
-   Cuando la aplicación termine de usar la cola de solicitudes, cierre el identificador de la cola de solicitudes mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .
-   Cuando la aplicación termine de usar la API del servidor HTTP, llame a la función [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) .

 

 