---
title: Elemento ServiceTask2
description: Nota En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El elemento ServiceTask2 representa el segundo panel de tareas del almacén en línea.
ms.assetid: f920ef25-efca-47c8-bcbc-2cb34593e879
keywords:
- Elemento ServiceTask2 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ServiceTask2 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b1d56001effab8ae4f7375023aeac48936f7e2faeb9806b43ca90d3292b82e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569754"
---
# <a name="servicetask2-element"></a>Elemento ServiceTask2

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El **elemento ServiceTask2** representa el segundo panel de tareas del almacén en línea.

``` syntax
<ServiceTask2
    URL = "URL"
/>
```

## <a name="attributes"></a>Atributos



| Término                                                                                                                             | Descripción                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**DIRECCIÓN URL** (obligatorio)<br/> | Dirección URL de la página web que Reproductor de Windows Media muestra.<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento                       |
|-----------------|-------------------------------|
| Elementos primarios | **ServiceInfo**               |
| Elementos secundarios  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Comentarios

**ServiceTask1 se** considera el panel de tareas principal para participar en la actividad comercial. Es el panel de tareas que se muestra cuando el usuario decide comprar música. Use **ServiceTask2 para** otra actividad de la tienda en línea.

> [!Note]  
> Reproductor de Windows Media 10 tiene tres paneles de tareas donde una tienda en línea puede mostrar sus páginas web. La tienda en línea puede optar por usar uno, dos o los tres paneles de tareas. Reproductor de Windows Media 11 solo tiene un panel de tareas, que el usuario puede ver haciendo clic en la pestaña **Tiendas** en línea. Reproductor de Windows Media 11 omite los elementos **ServiceTask2** y **ServiceTask3.**

 

Los paneles de tareas de las tiendas en línea comparten una única instancia del explorador. Esto significa que no debe escribir código de script en la página web que espera que siga funcionando cuando el usuario se aleje de la tarea de servicio actual.

Cuando el usuario cambia los paneles de tareas, Reproductor de Windows Media almacena la dirección URL y las cookies de sesión. Cuando el usuario vuelve al panel de tareas, el reproductor restaura la dirección URL y las cookies. Si el usuario decide usar una tienda en línea diferente, se borran la dirección URL y los datos de sesión.

En la tabla siguiente se detallan los parámetros enviados con la solicitud de dirección URL. Otros pueden estar presentes con fines de compatibilidad heredados.



| Nombre         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows de ubicación geográfica. El usuario especifica el identificador de  ubicación en el área Ubicación de la configuración Regional e Idioma de Panel de control. |
| *locale*     | Reproductor de Windows Media de configuración regional.                                                                                                                                     |
| *userlocale* | Windows de configuración regional. El usuario especifica la configuración regional  en el área Estándares y formatos de la configuración Regional e Idioma de Panel de control.        |
| *version*    | Reproductor de Windows Media número de versión con el siguiente formato: 10.0.x.xxxx o 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





