---
title: Atributo StrokeWeight de VML
description: Atributo StrokeWeight de VML
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792202"
---
# <a name="vml-strokeweight-attribute"></a><span data-ttu-id="79120-103">Atributo StrokeWeight de VML</span><span class="sxs-lookup"><span data-stu-id="79120-103">VML StrokeWeight Attribute</span></span>

<span data-ttu-id="79120-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="79120-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="79120-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="79120-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="79120-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="79120-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="79120-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="79120-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="79120-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="79120-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="79120-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="79120-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="79120-110">Define el grosor del pincel que traza el trazado de una forma.</span><span class="sxs-lookup"><span data-stu-id="79120-110">Defines the brush thickness that strokes the path of a shape.</span></span> <span data-ttu-id="79120-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="79120-111">Read/write.</span></span> <span data-ttu-id="79120-112">**VGLength**.</span><span class="sxs-lookup"><span data-stu-id="79120-112">**VGLength**.</span></span>

<span data-ttu-id="79120-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="79120-113">**Applies To**</span></span>

[<span data-ttu-id="79120-114">Forma</span><span class="sxs-lookup"><span data-stu-id="79120-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="79120-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="79120-115">**Tag Syntax**</span></span>

<span data-ttu-id="79120-116"><v: *Element* strokeweight = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="79120-116"><v: *element* strokeweight=" *expression* "></span></span>

<span data-ttu-id="79120-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="79120-117">**Script Syntax**</span></span>

<span data-ttu-id="79120-118">*Element* . strokeweight = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="79120-118">*element* .strokeweight="*expression*"</span></span>

<span data-ttu-id="79120-119">*expresión* = de *elemento*. strokeweight</span><span class="sxs-lookup"><span data-stu-id="79120-119">*expression*=*element*.strokeweight</span></span>

<span data-ttu-id="79120-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="79120-120">**Remarks**</span></span>

<span data-ttu-id="79120-121">El valor se duplica desde el atributo **Weight** del elemento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="79120-121">The value is duplicated from the **Weight** attribute of the **Stroke** element.</span></span> <span data-ttu-id="79120-122">Si se especifica un número, pero no se agregan unidades, la unidad de medida predeterminada es la UME.</span><span class="sxs-lookup"><span data-stu-id="79120-122">If a number is specified, but no units are added, the default unit of measurement is the Emu.</span></span> <span data-ttu-id="79120-123">Si no se especifica ningún valor, el valor predeterminado es 1 píxel (1px).</span><span class="sxs-lookup"><span data-stu-id="79120-123">If no value is specified, the default is 1 pixel (1px).</span></span>

<span data-ttu-id="79120-124">En el caso de las secuencias de comandos, sin embargo, la unidad de medida predeterminada está en puntos.</span><span class="sxs-lookup"><span data-stu-id="79120-124">For scripting, however, the default unit of measurement is in points.</span></span>

<span data-ttu-id="79120-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="79120-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="79120-126">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="79120-126">**See Also**</span></span>

<span data-ttu-id="79120-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span><span class="sxs-lookup"><span data-stu-id="79120-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span></span>

<span data-ttu-id="79120-128">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="79120-128">**Example**</span></span>

<span data-ttu-id="79120-129">El grosor del trazo de la forma es de 1 punto.</span><span class="sxs-lookup"><span data-stu-id="79120-129">The stroke weight of the shape is 1 point.</span></span>


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="79120-130">[Ejemplo del atributo StrokeWeight](/previous-versions/bb264095(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79120-130">[StrokeWeight Attribute Example](/previous-versions/bb264095(v=vs.85)).</span></span> <span data-ttu-id="79120-131">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="79120-131">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 