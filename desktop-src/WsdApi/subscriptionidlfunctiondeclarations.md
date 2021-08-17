---
description: Genera declaraciones IDL para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: elemento subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3998103d04250206ef382f822e329210b83471c69dcc51b401fcfbc241460729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130617"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a>elemento subscriptionIdlFunctionDeclarations

Genera declaraciones IDL para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.

## <a name="usage"></a>Uso

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a>Atributos



| Atributo                 | Tipo               | Requerido      | Descripción                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **extensible**<br/> | boolean<br/> | No<br/> | La capacidad de agregar puntos de extensibilidad a funciones e interfaces. Este valor siempre se establece en true.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                           | Descripción                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | Especifica el nombre de la interfaz de notificación que se usa con las suscripciones de eventos.<br/> <br/> |
| [**operation**](operation.md)<br/>                         | Especifica una operación para la que se va a generar código.<br/> <br/>                       |
| [**portType**](porttype.md)<br/>                           | Especifica el tipo de puerto para el que se va a generar el código.<br/> <br/>                      |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo desde el generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




