---
description: '\_sección de \_ tipo de contenido de WPD \_'
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fbb63821f75115c5855653dc811067891652615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083196"
---
# <a name="wpd_content_type_section"></a>\_sección de \_ tipo de contenido de WPD \_

Un objeto que describe su tipo como la \_ \_ sección de tipo de contenido WPD \_ representa una sección de datos que se encuentra en otro objeto. Por ejemplo, un archivo de audio de gran tamaño puede describirse como una colección de varios capítulos y cada capítulo puede ser un objeto de sección de tipo de contenido de WPD \_ \_ \_ .

La \_ propiedad referencias del objeto WPD \_ identifica el objeto primario de una sección determinada.

Este tipo de objeto admite las siguientes propiedades.



|                                                                                                                                  |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Nombre de la propiedad**                                                                                                                | **Obligatorio u opcional**                                              |
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                           | Obligatorio.                                                             |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                            | Obligatorio.                                                             |
| [\_nombre del objeto WPD \_](object-properties.md)                                                                       | Es obligatorio si el objeto representa un archivo.                             |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                                     | Obligatorio.                                                             |
| [\_formato de objeto WPD \_](object-properties.md)                                                                   | Obligatorio.                                                             |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                                      | Obligatorio.                                                             |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                               | Es obligatorio si el objeto está oculto.                                     |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                               | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                                       | Obligatorio si el objeto tiene al menos un recurso.                     |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                                         | Es obligatorio si el objeto representa un archivo.                             |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                                  | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo. |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                           | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                               | Opcional.                                                             |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                             |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                             | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                                      | Opcional.                                                             |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                                    | Se recomienda su uso.                                                          |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                                    | Opcional.                                                             |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                                | Se recomienda si el objeto tiene referencias a otros objetos.            |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)                | Opcional.                                                             |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md)            | Opcional.                                                             |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                                          | Es obligatorio si no se puede eliminar el objeto.                             |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                           | Opcional.                                                             |
| [\_desplazamiento de \_ datos de sección de WPD \_](section-attribute-properties.md)                                           | Obligatorio.                                                             |
| [longitud de los datos de la \_ sección WPD \_ \_](section-attribute-properties.md)                                           | Obligatorio.                                                             |
| [unidades de datos de la \_ sección WPD \_ \_](section-attribute-properties.md)                                             | Se recomienda su uso.                                                          |
| [\_recursos de \_ objeto de referencia de datos de sección de \_ \_ WPD \_](section-attribute-properties.md) | Se recomienda su uso.                                                          |



 

## <a name="typical-resources"></a>Recursos típicos

Normalmente, estos objetos no hospedan recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



