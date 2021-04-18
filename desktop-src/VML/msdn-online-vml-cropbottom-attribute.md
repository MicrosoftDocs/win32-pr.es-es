---
title: Atributo CropBottom de VML
description: Atributo CropBottom de VML
ms.assetid: 9548d0fa-1708-4206-90d8-1d90cb42de87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b847fcd061e13418efe04b6ea27795a19002abf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359037"
---
# <a name="vml-cropbottom-attribute"></a><span data-ttu-id="3518a-103">Atributo CropBottom de VML</span><span class="sxs-lookup"><span data-stu-id="3518a-103">VML CropBottom Attribute</span></span>

<span data-ttu-id="3518a-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3518a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3518a-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3518a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3518a-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3518a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3518a-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3518a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3518a-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3518a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3518a-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3518a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3518a-110">Define el porcentaje de eliminación de imágenes del lado inferior.</span><span class="sxs-lookup"><span data-stu-id="3518a-110">Defines the percentage of picture removal from the bottom side.</span></span> <span data-ttu-id="3518a-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3518a-111">Read/write.</span></span> <span data-ttu-id="3518a-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="3518a-112">**VgNumber**.</span></span>

<span data-ttu-id="3518a-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3518a-113">**Applies To**</span></span>

[<span data-ttu-id="3518a-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="3518a-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="3518a-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3518a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3518a-116"><v: *elemento* CropBottom = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="3518a-116"><v: *element* cropbottom=" *expression* "></span></span>

<span data-ttu-id="3518a-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="3518a-117">**Script Syntax**</span></span>

<span data-ttu-id="3518a-118">*Element* . CropBottom = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="3518a-118">*element* .cropbottom="*expression*"</span></span>

<span data-ttu-id="3518a-119">*expresión* = de *elemento*. CropBottom</span><span class="sxs-lookup"><span data-stu-id="3518a-119">*expression*=*element*.cropbottom</span></span>

<span data-ttu-id="3518a-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3518a-120">**Remarks**</span></span>

<span data-ttu-id="3518a-121">La cantidad de recorte puede oscilar entre-1,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="3518a-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="3518a-122">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="3518a-122">The default value is 0.</span></span> <span data-ttu-id="3518a-123">Tenga en cuenta que el valor 1 no mostrará ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="3518a-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="3518a-124">Los valores negativos provocarán que la imagen se apriete hacia adentro desde el borde que se va a recortar (el color de relleno de la forma se rellenará con el espacio vacío entre la imagen y el borde recortado).</span><span class="sxs-lookup"><span data-stu-id="3518a-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="3518a-125">Los valores positivos inferiores a 1 darán lugar a que la imagen restante se estire para ajustarse a la forma.</span><span class="sxs-lookup"><span data-stu-id="3518a-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="3518a-126">Atributo estándar de VML</span><span class="sxs-lookup"><span data-stu-id="3518a-126">VML Standard Attribute</span></span>

<span data-ttu-id="3518a-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3518a-127">**Example**</span></span>

<span data-ttu-id="3518a-128">No se mostrará ninguna imagen porque la imagen es 100% recortada de la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="3518a-128">No image will be displayed because the image is 100% cropped from the bottom.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropbottom="1" src="kids.jpg"/>
   </v:shape>
```



 

 