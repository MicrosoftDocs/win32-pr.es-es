---
description: '\_certificado de \_ tipo de contenido de WPD \_'
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706862"
---
# <a name="wpd_content_type_certificate"></a>\_certificado de \_ tipo de contenido de WPD \_

Un objeto que describe su tipo como \_ certificado de tipo de contenido de WPD \_ \_ representa un certificado utilizado para la autenticación.

Este tipo de objeto admite las siguientes propiedades.



| Nombre de la propiedad                                                                                                         | Obligatorio u opcional                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_identificador de objeto de WPD \_](object-properties.md)                                                                | Obligatorio.                                                             |
| [\_ \_ ID. primario del objeto WPD \_](object-properties.md)                                                 | Obligatorio.                                                             |
| [\_nombre del objeto WPD \_](object-properties.md)                                                            | Es obligatorio si el objeto representa un archivo.                             |
| [\_ \_ \_ identificador único persistente del objeto WPD \_](object-properties.md)                          | Obligatorio.                                                             |
| [\_formato de objeto WPD \_](object-properties.md)                                                        | Obligatorio.                                                             |
| [\_tipo de \_ contenido del objeto WPD \_](object-properties.md)                                           | Obligatorio.                                                             |
| [\_objeto WPD \_ ISHIDDEN](object-properties.md)                                                    | Es obligatorio si el objeto está oculto.                                     |
| [\_objeto WPD \_ ISSYSTEM](object-properties.md)                                                    | Obligatorio si el objeto es un objeto del sistema (representa un archivo del sistema). |
| [\_tamaño del objeto WPD \_](object-properties.md)                                                            | Obligatorio si el objeto tiene al menos un recurso.                     |
| [\_nombre de \_ \_ archivo original del objeto \_ WPD](object-properties.md)                              | Es obligatorio si el objeto representa un archivo.                             |
| [\_objeto WPD \_ no \_ consumible](object-properties.md)                                       | Se recomienda si el objeto no está diseñado para su consumo por parte del dispositivo. |
| [\_referencias a objetos de WPD \_](object-properties.md)                                                | Obligatorio si el objeto tiene referencias a otros objetos.               |
| [\_palabras clave del objeto WPD \_](object-properties.md)                                                    | Opcional.                                                             |
| [\_identificador de \_ sincronización del objeto WPD \_](object-properties.md)                                                     | Opcional.                                                             |
| [el \_ objeto \_ WPD \_ está \_ protegido con DRM](object-properties.md)                                  | Obligatorio si el objeto está protegido por la tecnología DRM.                |
| [\_fecha de objeto WPD \_ \_ creada](object-properties.md)                                           | Opcional.                                                             |
| [\_fecha del objeto WPD \_ \_ modificada](object-properties.md)                                         | Se recomienda su uso.                                                          |
| [\_fecha del objeto WPD \_ \_ creado](object-properties.md)                                         | Opcional.                                                             |
| [\_ \_ referencias inversas de objetos de WPD \_](object-properties.md)                                     | Se recomienda si otro objeto hace referencia al objeto.            |
| [\_identificador de \_ \_ objeto funcional \_ del contenedor de objetos de \_ WPD](object-properties.md)     | Opcional.                                                             |
| [el \_ objeto WPD \_ genera \_ miniaturas \_ desde el \_ recurso](object-properties.md) | Opcional.                                                             |
| [el \_ objeto WPD \_ puede \_ eliminar](object-properties.md)                                               | Obligatorio si el objeto se puede eliminar.                                |
| [\_ \_ configuración regional de idioma del objeto WPD \_](object-properties.md)                                                                | Opcional.                                                             |



 

## <a name="typical-resources"></a>Recursos típicos

Estos objetos suelen incluir los siguientes recursos.



| Nombre de recurso                                          | Obligatorio u opcional | Descripción        |
|--------------------------------------------------------|----------------------|--------------------|
| [**\_valor predeterminado del recurso WPD \_**](wpd-resource-default.md) | Obligatorio.            | Contiene los datos. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Requisitos para objetos**](requirements-for-objects.md)
</dt> </dl>

 

 



