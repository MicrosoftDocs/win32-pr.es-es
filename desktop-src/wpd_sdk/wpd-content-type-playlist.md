---
description: '\_lista de \_ reproducción de tipo de contenido de WPD \_'
ms.assetid: 4223970d-8c37-4326-a2df-bec558f8ac5e
title: WPD_CONTENT_TYPE_PLAYLIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b650527d92d2b3523654b3445aaf60496aae3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816278"
---
# <a name="wpd_content_type_playlist"></a>\_lista de \_ reproducción de tipo de contenido de WPD \_

Un objeto que describe su tipo como lista de reproducción de tipo de contenido de WPD \_ \_ \_ representa una lista de reproducción. Una lista de reproducción se puede representar mediante un archivo físico o puede constar de referencias almacenadas como metadatos.

Este tipo de objeto admite las siguientes propiedades.



|                                                                                                                       |                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre de la propiedad**                                                                                                     | **Obligatorio u opcional**                                                                                                                       |
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad incluso en el momento de la creación.                                                                  |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                                                                                                      |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                                                                                                      |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Requerido, de solo lectura. Un cliente no puede establecer esta propiedad, ni siquiera en el momento de la creación.                                                                 |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                                                                                                      |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                                                                                                      |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                                                                                              |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema).                                                                          |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                                                                                              |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                                                                                                      |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo.                                                                          |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Es obligatorio si el objeto tiene referencias a otros objetos; es decir, si las referencias se almacenan como metadatos en lugar de datos físicos en un archivo. |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                                                                                                      |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                                                                                                      |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                                                                                         |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                                                                                                      |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                                                                                                   |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                                                                                                      |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                                | Se recomienda si otro objeto hace referencia al objeto.                                                                                     |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                                                                                                      |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                                                                                                      |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                                     | Es obligatorio si no se puede eliminar el objeto.                                                                                                      |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                                                                                                      |
| [\_marcador de \_ objeto \_ multimedia WPD](object-properties.md)                                                                 | Se recomienda su uso.                                                                                                                                   |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                          | Obligatorio u opcional | Descripción                                                                                                                  |
|--------------------------------------------------------|----------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md) | Opcional.            | Si la lista de reproducción es un archivo físico, por ejemplo, un archivo XML que enumera los archivos multimedia que se van a reproducir, es el archivo bytes real. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



