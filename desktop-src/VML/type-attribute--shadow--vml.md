---
title: Atributo de tipo (Shadow)(VML)
description: Atributo de tipo (Shadow)(VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90a264cbaf77890e39f10d56103c8acdc84727de21d7f2de9946911b6df41dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513165"
---
# <a name="type-attribute-shadowvml"></a>Atributo de tipo (Shadow)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica el tipo de sombra. Lectura/escritura **Cadena**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *element* type=" *expression* ">

**Sintaxis de script**

*element* .type="*expression*"

*expresión* = *element*.type

**Comentarios:**

Estos valores incluyen:



| Value           | Descripción                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sola          | Sombra única. Predeterminada.                                                                                                                                                                              |
| double          | Sombra doble. [Color2](color2-attribute--shadow--vml.md) se usa para el color de la segunda sombra y [Offset2](msdn-online-vml-offset2-attribute.md) para el desplazamiento de la segunda sombra. |
| perspectiva     | Sombra de perspectiva.                                                                                                                                                                                |
| shapeRelative   | La sombra se crea en relación con la forma.                                                                                                                                                         |
| drawingRelative | La sombra se crea en relación con el dibujo.                                                                                                                                                       |
| Realza          | La sombra tiene un aspecto relieve.                                                                                                                                                                     |



 

**Atributo estándar de VML**

**Ejemplo**

Se crea una sombra doble con la segunda sombra verde y el desplazamiento 5 puntos hacia abajo y hacia la derecha.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 