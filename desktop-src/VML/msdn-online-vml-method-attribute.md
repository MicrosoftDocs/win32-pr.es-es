---
title: Atributo de método VML
description: Atributo de método VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695698"
---
# <a name="vml-method-attribute"></a>Atributo de método VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el método utilizado para generar un relleno de degradado. Lectura/escritura **VgSigmaType**.

**Se aplica a**

[Fill](msdn-online-vml-fill-element.md)

**Sintaxis de etiquetas**

<v: *Element* Method = " *expresión* " >

**Sintaxis de script**

*Element* . Method = "*expresión*"

*expresión* = de *Element*. Method

**Comentarios:**

Estos valores incluyen:



| Value  | Descripción          |
|--------|----------------------|
| None   | Sin relleno de Sigma.       |
| Lineal | Relleno de Sigma lineal.   |
| Sigma  | Relleno de Sigma. Predeterminada. |
| Any    | Cualquier relleno de Sigma.      |



 

*Atributo estándar de VML*

**Ejemplo**

La forma tendrá un relleno de degradado lineal rojo.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 