---
title: Tipos de medios para el SDK de Windows Media Format
description: Obtenga información acerca de los tipos de medios que puede usar el SDK de Windows Media Format. Los tipos de medios son valores GUID asignados a constantes en el SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, tipos de medios
- Advanced Systems Format (ASF), tipos de medios
- ASF (formato de sistemas avanzados), tipos de medios
- tipos de medios, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187814"
---
# <a name="media-types-for-windows-media-format-sdk"></a>Tipos de medios para el SDK de Windows Media Format

Los tipos de medios identifican los distintos tipos de medios que puede usar el SDK de Windows Media Format. Todos los tipos de medios son valores GUID que se han asignado a constantes en el SDK. Los valores de GUID representados por las constantes que se enumeran en esta sección se enumeran en la sección [identificadores de tipo de medio](media-type-identifiers.md) de esta referencia.

En la tabla siguiente se enumeran los tipos de medios principales. Estas constantes definen la clasificación de alto nivel de los medios digitales compatibles con el SDK de Windows Media Format.



| Tipo principal                | Descripción                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| Vídeo de WMMEDIATYPE \_        | Un flujo de vídeo.                                                                                         |
| \_Audio WMMEDIATYPE        | Secuencia de audio.                                                                                        |
| \_Script WMMEDIATYPE       | Secuencia de script.                                                                                        |
| WMMEDIATYPE \_ FileTransfer | Flujo que contiene archivos de datos. Las secuencias Web, que constan de archivos HTML, también tienen este tipo principal. |
| Imagen de WMMEDIATYPE \_        | Secuencia de imágenes JPEG para un archivo de audio ilustrado (como en una presentación).                                 |
| \_Texto WMMEDIATYPE         | Secuencia de texto.                                                                                          |



 

Además de los tipos de medios principales admitidos explícitamente, puede crear sus propios tipos de datos arbitrarios. En el caso de los tipos de datos arbitrarios personalizados, debe asegurarse de que el GUID que usa no coincide con un tipo principal existente.

A menudo, un flujo multimedia tendrá un subtipo además de su tipo principal. En las secciones siguientes se enumeran los subtipos admitidos.



| Sección                                                        | Descripción                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Subtipos de medios sin comprimir](uncompressed-media-subtypes.md) | Describe los subtipos disponibles para los medios sin comprimir. Estos son los tipos que normalmente se asocian a los medios de entrada o salida.              |
| [Subtipos de medios comprimidos](compressed-media-subtypes.md)     | Describe los subtipos disponibles para los medios comprimidos. Estos son los tipos asociados normalmente a los elementos multimedia en una secuencia dentro de un archivo ASF. |
| [Formatos de entrada de vídeo](video-input-formats.md)                 | Enumera los formatos de vídeo que se aceptan como entradas para el códec Windows Media Video 9.                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de tipo de medio**](media-type-identifiers.md)
</dt> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 




