---
description: Explore las tecnologías relacionadas con el esquema de impresión. Este tema no está actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: Tecnologías de Schema-Related impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c39d002b956fdd012a2b74a94ae0a4c58f568d8
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548793"
---
# <a name="print-schema-related-technologies"></a>Tecnologías de Schema-Related impresión

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Para las versiones .NET Framework 3.0, Windows Vista y versiones posteriores, las tecnologías PrintCapabilities e PrintTicket amplían las funcionalidades del esquema de impresión para permitir una experiencia de impresión más completa.

## <a name="printcapabilities"></a>PrintCapabilities

La tecnología PrintCapabilities es un método para publicar la descripción de la configuración controlable por el usuario de los atributos y la configuración por trabajo. PrintCapabilities se publica en un documento del lenguaje de marcado eXtensible (XML) denominado documento PrintCapabilities, que consta de términos definidos en las palabras clave de esquema de impresión y las extensiones privadas. El documento PrintCapabilities se puede pensar como una "instantánea" de la configuración actual del dispositivo de estado configurable por el usuario, así como una descripción de las posibles configuraciones. Los dispositivos (o controladores de dispositivo) generan un documento PrintCapabilities (la instantánea) de su conjunto actual de opciones configurables cuando los clientes lo consultan, que pueden ser aplicaciones o el subsistema de impresión. En este documento se describen todas las opciones de PrintCapabilities configurables disponibles actualmente en el dispositivo, como las opciones de finalización y las opciones de diseño de página. El documento PrintCapabilities describe explícitamente todos los atributos del dispositivo y la configuración permitido para cada atributo. Mediante el uso de Print Schema Framework, los atributos del dispositivo se pueden describir con precisión y comparar de forma eficaz. Mediante el uso de las palabras clave contenidas en el documento Imprimir palabras clave de esquema y la estructura definida en el marco de esquema de impresión, los dispositivos pueden permitir que los clientes usen PrintCapabilities de forma más eficaz. Para obtener más información, [vea PrintCapabilities Schema y Document Construction](printcapabilities-schema-and-document-construction.md).

En relación con el subsistema de impresión de Microsoft Windows Server 2003 y versiones anteriores, la tecnología PrintCapabilities permite a los componentes del subsistema de impresión y cliente ver de forma transparente la información contenida en el archivo binario del sistema Win32 actual PrintCapabilities. Esto permite al cliente consultar PrintCapabilities, recibir una instantánea XML coherente y bien comprendida y usarla para construir un PrintTicket para un dispositivo sin invocar la interfaz de usuario (UI) del controlador.

## <a name="printticket"></a>PrintTicket

La tecnología PrintTicket es la sucesora de la estructura DEVMODE actual. Es un documento basado en el lenguaje de marcado eXtensible que especifica y conserva información sobre el formato del trabajo y la configuración del trabajo de impresión. Una instancia de PrintTicket asigna una configuración de dispositivo determinada y transmite la intención del usuario. Hay dos tipos de PrintTickets: printtickets genéricos, que no se generan para un dispositivo determinado; y PrintTickets específicos del dispositivo, que se construyen para un dispositivo determinado. Los PrintTickets genéricos, que están diseñados para ser portátiles entre dispositivos, derivan su contenido seleccionando la configuración de cada uno de los atributos de dispositivo descritos exclusivamente en Las palabras clave de esquema de impresión. PrintTickets específicos del dispositivo derivan su contenido de un documento PrintCapabilities, seleccionando la configuración de cada atributo de dispositivo anunciado por este documento. Estos PrintTickets también pueden incluir extensiones privadas, específicas de un modelo de dispositivo o una familia de modelos de dispositivo. Para obtener más información, [vea Esquema PrintTicket y Construcción de documentos.](printticket-schema-and-document-construction.md)

En relación con el subsistema de impresión actual, la tecnología PrintTicket permite que todos los componentes y clientes del subsistema de impresión tengan acceso transparente a la información almacenada actualmente en las partes públicas y privadas de la estructura DEVMODE, utilizando un formato XML bien definido. Este diseño resuelve los problemas actuales que se encuentran en los escenarios de actualización o degradación de controladores y de discrepancia de controladores en controladores diseñados para la tecnología PrintTicket. Actualmente, estos escenarios pueden provocar una pérdida de configuración y, por tanto, una experiencia negativa del cliente. PrintTicket también permite nuevos escenarios, como permitir que un controlador de impresora exponga su configuración de DEVMODE privada a las aplicaciones y complementos personalizados de una manera coherente e inequívoca. Esto permite que los componentes de impresión sean más transparentes y controle las migraciones de configuración de forma más limpia. Las interfaces PrintTicket se exponen a las aplicaciones a través de métodos en objetos de código administrado que también estarán disponibles para los scripts. En el nuevo marco de trabajo de la aplicación basado en objetos de código administrado en .NET Framework 3.0, PrintTicket es la manera estándar de describir la configuración del documento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



