---
title: Atributo StartArrowLength de VML
description: Atributo StartArrowLength de VML
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420983"
---
# <a name="vml-startarrowlength-attribute"></a>Atributo StartArrowLength de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la longitud de la punta de flecha para el inicio de una línea. Lectura/escritura **VgArrowheadLength**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* startarrowlength = " *expresión* " >

**Sintaxis de script**

*Element* . startarrowlength = "*expresión*"

*expresión* = de *elemento*. startarrowlength

**Comentarios:**

Estos valores incluyen:

-   Short
-   Media (valor predeterminado)
-   long

Atributo estándar de VML

**Ejemplo**

Una línea se dibuja con una punta de flecha clásica corta en el inicio del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 