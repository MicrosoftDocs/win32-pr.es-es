---
title: VML MSO-Wrap-Distance-Left (atributo)
description: VML MSO-Wrap-Distance-Left (atributo)
ms.assetid: 25dcb5d0-a839-4a4b-8969-8e5dcf1baa47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d1e47fff0f9dceff5fd98ad526208bf487d851
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359072"
---
# <a name="vml-mso-wrap-distance-left-attribute"></a><span data-ttu-id="92f37-103">VML MSO-Wrap-Distance-Left (atributo)</span><span class="sxs-lookup"><span data-stu-id="92f37-103">VML MSO-Wrap-Distance-Left Attribute</span></span>

<span data-ttu-id="92f37-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="92f37-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="92f37-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="92f37-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="92f37-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="92f37-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="92f37-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="92f37-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="92f37-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="92f37-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="92f37-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="92f37-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="92f37-110">Define la distancia desde el lado izquierdo de la forma hasta el texto que se ajusta alrededor de ella.</span><span class="sxs-lookup"><span data-stu-id="92f37-110">Defines the distance from the left side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="92f37-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="92f37-111">Read/write.</span></span> <span data-ttu-id="92f37-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="92f37-112">**String**.</span></span>

<span data-ttu-id="92f37-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="92f37-113">**Applies To**</span></span>

[<span data-ttu-id="92f37-114">Forma</span><span class="sxs-lookup"><span data-stu-id="92f37-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="92f37-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="92f37-115">**Tag Syntax**</span></span>

<span data-ttu-id="92f37-116"><v: *Element* style = "MSO-Wrap-Distance-Left: *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="92f37-116"><v: *element* style="mso-wrap-distance-left: *expression* "></span></span>

<span data-ttu-id="92f37-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="92f37-117">**Remarks**</span></span>

<span data-ttu-id="92f37-118">Tenga en cuenta que este atributo es diferente del atributo de **margen** de CSS.</span><span class="sxs-lookup"><span data-stu-id="92f37-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="92f37-119">**Margen** cambia el origen de la forma para incluir las áreas de margen, pero la distancia de ajuste en Microsoft Office no cambia el origen de la forma.</span><span class="sxs-lookup"><span data-stu-id="92f37-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="92f37-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="92f37-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="92f37-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="92f37-121">**Example**</span></span>

<span data-ttu-id="92f37-122">La forma tiene una distancia de ajuste izquierda de 10 puntos.</span><span class="sxs-lookup"><span data-stu-id="92f37-122">The shape has a left wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-left:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 