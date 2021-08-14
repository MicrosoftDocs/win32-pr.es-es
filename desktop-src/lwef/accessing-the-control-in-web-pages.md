---
title: Acceso al control en páginas web
description: Acceso al control en páginas web
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3766475dc798f8f61e98b818fc8e71205bbc72c34f2282098f00b5f03ed3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480741"
---
# <a name="accessing-the-control-in-web-pages"></a>Acceso al control en páginas web

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Para acceder a los servicios de Microsoft Agent desde una página web, use la etiqueta HTML <OBJECT> dentro de <HEAD> o <BODY> elemento de la página, especificando el CLSID de Microsoft (identificador de clase) para el control. Además, use un parámetro CODEBASE para especificar la ubicación del archivo de instalación de Microsoft Agent y su número de versión.

Si Microsoft Internet Explorer (versión 3.02 o posterior) está instalado en el sistema, pero Microsoft Agent aún no está instalado y el usuario accede a una página web que tiene la etiqueta con el CLSID del Agente, el explorador intentará descargar automáticamente el Agente desde el sitio web <OBJECT> de Microsoft. A continuación, se le preguntará al usuario si desea continuar con la instalación. Para otros exploradores, póngase en contacto con el proveedor para obtener información sobre su soporte técnico o soporte técnico de terceros para ActiveX controles.

En el ejemplo siguiente se muestra cómo usar el parámetro CODEBASE para descargar automáticamente la versión 2.0 en inglés de Microsoft Agent.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

El agente también se puede instalar desde su propio servidor HTTP o como parte del proceso de instalación de una aplicación. Para admitir la instalación desde su propio servidor HTTP, debe publicar el archivo de archivo de .Exe auto-instalación de Microsoft Agent y especificar su dirección URL en la etiqueta CODEBASE.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Para admitir la descarga automática de un componente de lenguaje de Microsoft Agent desde una página web, incluya la etiqueta Object del componente de idioma en la página antes de la etiqueta Object del control Agent:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

donde XXXX se reemplaza por un identificador de idioma. Para ver los idiomas admitidos actualmente, consulte el sitio web de Microsoft Agent.

-   La <OBJECT> etiqueta de un componente de lenguaje debe preceder a la etiqueta del componente principal de Microsoft <OBJECT> Agent.
-   Se pueden instalar varios idiomas en el mismo cliente.
-   Antes de establecer [**el valor de LanguageID**](https://www.bing.com/search?q=**LanguageID**) de un carácter, se recomienda que el script compruebe que la configuración regional del explorador, disponible en la propiedad [**userLanguage,**](https://www.bing.com/search?q=**userLanguage**) coincide con el idioma que se establece.

Para admitir otras versiones de idioma del Agente , use otra etiqueta Object que especifique el componente de idioma. Sin embargo, tenga en cuenta que intentar instalar varios idiomas al mismo tiempo puede requerir que el usuario reinicie. Los componentes del lenguaje del Agente se pueden obtener del sitio web del Agente mediante el mismo procedimiento que para el componente principal del agente. Las licencias de distribución para los componentes de idioma se tratan en la licencia de distribución del Agente estándar. Para empezar a usar un carácter, debe cargar el carácter mediante el [**método Load.**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) Se puede cargar un carácter desde el almacenamiento local del usuario o desde un servidor HTTP. Para obtener más información sobre la sintaxis para cargar un carácter, vea el **método Load.** Una vez cargado correctamente el carácter, puede usar los métodos, propiedades y eventos expuestos por el control Agente para programar el carácter. También puede usar los métodos, propiedades y eventos expuestos por el lenguaje de programación y el explorador para programar el carácter. por ejemplo, para programar su reacción a un clic de botón. Consulte la documentación del explorador para determinar qué características expone en su modelo de scripting. Para microsoft Internet Explorer, consulte El modelo de objetos de scripting, que está disponible en el SDK de ActiveX.

Los servicios del agente permanecen cargados solo cuando hay al menos una aplicación cliente con una conexión. Esto significa que cuando un usuario se mueve entre páginas web habilitadas para el Agente, el Agente se apagará y los caracteres cargados desaparecerán. Para que el Agente se ejecute entre páginas (y, por tanto, mantenga visible un carácter), cree otro cliente que permanezca cargado entre los cambios de página. Por ejemplo, puede crear un conjunto de marcos HTML y declarar una <OBJECT> etiqueta para el Agente en el marco primario. A continuación, puede crear un script de las páginas que cargue en los marcos secundarios para llamar al script del elemento primario. Como alternativa, también puede incluir una etiqueta <OBJECT> en cada página que cargue en el marco secundario. En este caso, recuerde que cada página será su propio cliente. Es posible que tenga que usar el [**método Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) para establecer qué cliente tiene control cuando el usuario interactúa con la página primaria o secundaria.

 

 