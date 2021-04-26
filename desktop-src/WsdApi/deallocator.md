---
description: Especifica el tipo de desasignador que va a usar una función de código auxiliar.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: deallocator, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692ed2e57b3e649c0ee7af171f205c949496f9b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994942"
---
# <a name="deallocator-element"></a><span data-ttu-id="cf2a8-103">elemento deallocator</span><span class="sxs-lookup"><span data-stu-id="cf2a8-103">deallocator element</span></span>

<span data-ttu-id="cf2a8-104">Especifica el tipo de desasignador que va a usar una función de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="cf2a8-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="cf2a8-105">Uso</span><span class="sxs-lookup"><span data-stu-id="cf2a8-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="cf2a8-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="cf2a8-106">Attributes</span></span>

<span data-ttu-id="cf2a8-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="cf2a8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cf2a8-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf2a8-108">Child elements</span></span>

<span data-ttu-id="cf2a8-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="cf2a8-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="cf2a8-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="cf2a8-110">Parent elements</span></span>



| <span data-ttu-id="cf2a8-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf2a8-111">Element</span></span>                                               | <span data-ttu-id="cf2a8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf2a8-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf2a8-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="cf2a8-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="cf2a8-114">Genera implementaciones para funciones de código auxiliar para operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="cf2a8-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="cf2a8-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf2a8-115">Remarks</span></span>

<span data-ttu-id="cf2a8-116">El tipo de desasignador debe incluirse en un par de <deallocator></deallocator> etiquetas.</span><span class="sxs-lookup"><span data-stu-id="cf2a8-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="cf2a8-117">Las cadenas siguientes son valores de desasignador válidos:</span><span class="sxs-lookup"><span data-stu-id="cf2a8-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="cf2a8-118">ninguno</span><span class="sxs-lookup"><span data-stu-id="cf2a8-118">none</span></span>
-   <span data-ttu-id="cf2a8-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="cf2a8-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="cf2a8-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="cf2a8-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="cf2a8-121">libre</span><span class="sxs-lookup"><span data-stu-id="cf2a8-121">free</span></span>
-   <span data-ttu-id="cf2a8-122">delete</span><span class="sxs-lookup"><span data-stu-id="cf2a8-122">delete</span></span>
-   <span data-ttu-id="cf2a8-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="cf2a8-123">deleteArray</span></span>
-   <span data-ttu-id="cf2a8-124">Release</span><span class="sxs-lookup"><span data-stu-id="cf2a8-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="cf2a8-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="cf2a8-125">Element information</span></span>



| <span data-ttu-id="cf2a8-126">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="cf2a8-126">Label</span></span> | <span data-ttu-id="cf2a8-127">Value</span><span class="sxs-lookup"><span data-stu-id="cf2a8-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="cf2a8-128">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf2a8-128">Minimum supported system</span></span><br/> | <span data-ttu-id="cf2a8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf2a8-129">Windows Vista</span></span> |
| <span data-ttu-id="cf2a8-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cf2a8-130">Can be empty</span></span>                        | <span data-ttu-id="cf2a8-131">Sí</span><span class="sxs-lookup"><span data-stu-id="cf2a8-131">Yes</span></span>           |



 

 




