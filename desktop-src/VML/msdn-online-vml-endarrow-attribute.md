---
title: Atributo EndArrow de VML
description: Atributo EndArrow de VML
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542d6dbb3b30467c4bcad909f2b49d617f8bd886
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676507"
---
# <a name="vml-endarrow-attribute"></a>Atributo EndArrow de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una punta de flecha para el final de una línea. Lectura/escritura **Cadena**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* EndArrow = " *Expression* " >

**Sintaxis de script**

*Element* . EndArrow = "*Expression*"

*expresión* = de *elemento*. EndArrow

**Comentarios:**

Estos valores incluyen:

-   Ninguna (valor predeterminado)
-   Bloquear
-   Clásico
-   Diamond
-   Elipse
-   Abrir

*Atributo estándar de VML*

**Ejemplo**

Una línea se dibuja con una punta de flecha clásica en el final del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 