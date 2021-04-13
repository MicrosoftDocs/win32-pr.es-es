---
title: Creación de un cliente
description: La creación de un cliente para los servicios web se ha simplificado en gran medida en WWSAPI mediante la API del modelo de servicio y la herramienta WsUtil.exe.
ms.assetid: 09f489e8-958d-4bc5-a232-aa59bd75333a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606a68f574a9ad79d15f3ddd48247f93a5414250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419136"
---
# <a name="creating-a-client"></a>Creación de un cliente

La creación de un cliente para los servicios web se ha simplificado en gran medida en WWSAPI mediante la API del [modelo de servicio](service-model-layer-overview.md) y la herramienta [WsUtil.exe](wsutil-compiler-tool.md) . El modelo de servicio proporciona una API que permite al cliente enviar y recibir [mensajes](message.md) a través de un [canal](channel.md) como llamadas a métodos de C. La herramienta WsUtil genera encabezados y aplicaciones auxiliares para implementar el cliente. Estos encabezados incluyen los tipos y prototipos de función para las funciones de C que representan los servicios que ofrece el servicio Web de destino. Las aplicaciones auxiliares se utilizan para crear el proxy del servicio, que contiene la información de enlace y la [dirección del punto de conexión](endpoint-address.md) para el servicio.

## <a name="using-wsutil-to-generate-headers-and-helpers"></a>Uso de WsUtil para generar encabezados y aplicaciones auxiliares

Para generar encabezados y aplicaciones auxiliares, WsUtil abre y Lee los archivos de metadatos para el servicio de destino (archivos WSDL y XSD) y los convierte en encabezados. por lo tanto, es necesario recuperar de antemano los archivos de metadatos para el servicio de destino, por ejemplo, mediante SvcUtil, una parte de la Windows Communication Foundation. Por motivos de seguridad, es imperativo que las copias de estos archivos sean de confianza. (Para obtener más información, vea la sección "seguridad" del tema de la [herramienta del compilador WsUtil](wsutil-compiler-tool.md) ).

Para ejecutar WsUtil, use la siguiente sintaxis de línea de comandos si los archivos WSDL y XSD para el servicio se encuentran en su propio directorio: `WsUtil.exe *.wsdl *.xsd` . También puede especificar los archivos por nombre completo.

Normalmente, WsUtil genera dos archivos para cada archivo de metadatos: un encabezado y un archivo C. Agregue estos archivos al proyecto de codificación y use \# instrucciones include para incluirlos en el código del cliente. (Los archivos XSD representan tipos y los archivos WSDL representan operaciones).

## <a name="creating-the-service-proxy"></a>Creación del proxy de servicio

El encabezado generado por WsUtil contiene una rutina auxiliar para crear el proxy de servicio con el enlace necesario. Esta rutina se incluye en la sección "rutinas auxiliares de directivas" del archivo de encabezado generado. Por ejemplo, el encabezado generado para el servicio de calculadora mostrado en el ejemplo [httpcalculatorclientexample](httpcalculatorclientexample.md) contendrá el prototipo de función siguiente.


```
HRESULT BasicHttpBinding_ICalculator_CreateServiceProxy(
    __in_opt WS_HTTP_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(proxyPropertyCount) const WS_PROXY_PROPERTY* proxyProperties,
    __in const ULONG proxyPropertyCount,
    __deref_out_opt WS_SERVICE_PROXY** _serviceProxy,
    __in_opt WS_ERROR* error);
```



Incorpore esta aplicación auxiliar en el código y pase un identificador de [ \_ \_ proxy de servicio WS](ws-service-proxy.md) para recibir el identificador del proxy de servicio creado. En el escenario más sencillo, en el que solo un identificador de proxy de servicio y un objeto de error se pasan a la función, la llamada es similar a la siguiente.


```C++
hr = BasicHttpBinding_ICalculator_CreateServiceProxy(
            NULL,
            NULL,
            0,
            &serviceProxy,
            error);
```



Para crear la parte de la dirección del proxy de servicio, llame a [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) con un identificador al proxy de servicio y un puntero a una [**dirección de \_ extremo \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que contenga la dirección del punto de conexión de servicio a la que desea conectarse.

## <a name="implementing-the-client-with-function-prototypes"></a>Implementar el cliente con prototipos de función

Los encabezados generados a partir de los archivos WSDL de servicio también contienen prototipos de función de C que representan los servicios disponibles del servicio Web y específicos del enlace requerido. Por ejemplo, un encabezado generado para el servicio de calculadora que se muestra en HttpCalculatorServiceExample contendrá el siguiente prototipo para la operación de multiplicación de ese servicio.

``` syntax
HRESULT BasicHttpBinding_ICalculator_Multiply(
    __in WS_SERVICE_PROXY* _serviceProxy,
    __in double n1,
    __in double n2,
    __out double* MultiplyResult,
    __in WS_HEAP* _heap,
    __in_ecount_opt(_callPropertyCount) const WS_CALL_PROPERTY* _callProperties,
    __in const ULONG _callPropertyCount,
    __in_opt const WS_ASYNC_CONTEXT* _asyncContext,
    __in_opt WS_ERROR* _error);
```

Puede copiar los prototipos y usarlos como plantillas para codificar las llamadas de función en el cliente, en cada caso pasando el identificador al proxy del servicio. Cuando haya terminado con el proxy de servicio, llame a [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy).

 

 




