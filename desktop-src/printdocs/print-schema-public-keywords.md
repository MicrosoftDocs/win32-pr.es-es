---
description: En este artículo se especifican las palabras clave públicas que se definen para el esquema de impresión y su uso para PrintCapabilities e PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Palabras clave públicas del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbcab9ce943b7f344ce12c378252bc07c69260f75c607b36f7af54c107d3f84a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886365"
---
# <a name="print-schema-public-keywords"></a>Palabras clave públicas del esquema de impresión

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En la sección siguiente se especifican las palabras clave públicas que se definen para el esquema de impresión.

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>Uso de palabras clave públicas de esquema de impresión para funcionalidades de impresión

Las palabras clave especificadas en PrintCapabilities Public Keywords (Palabras clave públicas de PrintCapabilities) PUEDEN aparecer en un documento De capacidades de impresión. Para obtener más información sobre cómo interactúan estas palabras clave con la tecnología PrintCapabilities, consulte Información general [de la sección PrintCapabilities.](overview-of-the-printcapabilities.md)

Las palabras clave públicas específicas de PrintTicket NO DEBERÍAN aparecer en un documento PrintCapabilities.

## <a name="print-schema-public-keywords-usage-for-printticket"></a>Uso de palabras clave públicas de esquema de impresión para PrintTicket

Las palabras clave especificadas en PrintTicket Public Keywords (Palabras clave públicas de PrintTicket) PUEDEN aparecer en printTicket. Las palabras clave PrintTicket se implementan como un tipo de elemento Property. Para obtener más información sobre cómo interactúan estas palabras clave con la tecnología PrintTicket, consulte la sección Información de configuración no relacionada [con PrintCapabilities.](configuration-information-not-related-to-printcapabilities.md)

Las palabras clave especificadas en PrintCapabilities Public Keywords PUEDEN aparecer en printTicket en función de la implementación de PrintTicket en una aplicación o controlador. Esto proporciona selecciones para los atributos de dispositivo definidos en el documento PrintCapabilities. Para obtener más información sobre la interacción entre las palabras clave PrintCapabilities y PrintTicket, consulte [Propósito de la sección PrintTicket.](purpose-of-the-printticket.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



