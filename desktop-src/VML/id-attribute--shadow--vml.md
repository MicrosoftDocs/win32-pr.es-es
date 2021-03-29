---
title: ID (atributo, sombra) (VML)
description: ID (atributo, sombra) (VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792406"
---
# <a name="id-attribute-shadowvml"></a><span data-ttu-id="e3e55-103">ID (atributo, sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="e3e55-103">ID Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="e3e55-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e3e55-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e3e55-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="e3e55-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e3e55-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="e3e55-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e3e55-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="e3e55-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e3e55-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e3e55-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e3e55-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e3e55-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e3e55-110">Especifica un nombre que proporciona un identificador único para una sombra.</span><span class="sxs-lookup"><span data-stu-id="e3e55-110">Specifies a name that provides a unique identifier for a shadow.</span></span> <span data-ttu-id="e3e55-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e3e55-111">Read/write.</span></span> <span data-ttu-id="e3e55-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="e3e55-112">**String**.</span></span>

<span data-ttu-id="e3e55-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="e3e55-113">**Applies To**</span></span>

[<span data-ttu-id="e3e55-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="e3e55-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="e3e55-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="e3e55-115">**Tag Syntax**</span></span>

<span data-ttu-id="e3e55-116"><v: ID. de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="e3e55-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="e3e55-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="e3e55-117">**Script Syntax**</span></span>

<span data-ttu-id="e3e55-118">*Element* . ID = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="e3e55-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="e3e55-119">*expresión* = de identificador de *elemento*</span><span class="sxs-lookup"><span data-stu-id="e3e55-119">*expression*=*element*.id</span></span>

<span data-ttu-id="e3e55-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="e3e55-120">**Remarks**</span></span>

<span data-ttu-id="e3e55-121">Use el **identificador** para hacer referencia a una sombra específica.</span><span class="sxs-lookup"><span data-stu-id="e3e55-121">Use **ID** to refer to a specific shadow.</span></span> <span data-ttu-id="e3e55-122">Una vez que haya creado una sombra y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular la sombra.</span><span class="sxs-lookup"><span data-stu-id="e3e55-122">Once you have created a shadow and given it an ID, you can use the ID name when you want to manipulate the shadow.</span></span>

<span data-ttu-id="e3e55-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="e3e55-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="e3e55-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="e3e55-124">**Example**</span></span>

<span data-ttu-id="e3e55-125">La forma tiene un ID. de sombra denominado "prevaleci".</span><span class="sxs-lookup"><span data-stu-id="e3e55-125">The shape has a shadow ID called "myshadow".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 