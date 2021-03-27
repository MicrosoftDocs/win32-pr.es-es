---
title: log
description: Devuelve el logaritmo en base e del valor especificado.
ms.assetid: 443e7aa7-7219-40ad-aafc-4bce09c8f596
keywords:
- registro de HLSL
topic_type:
- apiref
api_name:
- log
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdd08fe178925406145476b3250e8d256b263c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793023"
---
# <a name="log"></a><span data-ttu-id="beb60-104">log</span><span class="sxs-lookup"><span data-stu-id="beb60-104">log</span></span>

<span data-ttu-id="beb60-105">Devuelve el logaritmo en base e del valor especificado.</span><span class="sxs-lookup"><span data-stu-id="beb60-105">Returns the base-e logarithm of the specified value.</span></span>



| <span data-ttu-id="beb60-106">Registro *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="beb60-106">*ret* log(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="beb60-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="beb60-107">Parameters</span></span>



| <span data-ttu-id="beb60-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="beb60-108">Item</span></span>                                                   | <span data-ttu-id="beb60-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="beb60-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="beb60-110"><span id="x"></span><span id="X"></span>*x1*</span><span class="sxs-lookup"><span data-stu-id="beb60-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="beb60-111">\[en \] el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="beb60-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="beb60-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beb60-112">Return Value</span></span>

<span data-ttu-id="beb60-113">Logaritmo en base e del parámetro *x* .</span><span class="sxs-lookup"><span data-stu-id="beb60-113">The base-e logarithm of the *x* parameter.</span></span> <span data-ttu-id="beb60-114">Si el parámetro *x* es negativo, esta función devuelve un valor indefinido.</span><span class="sxs-lookup"><span data-stu-id="beb60-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="beb60-115">Si el parámetro *x* es 0, esta función devuelve-INF.</span><span class="sxs-lookup"><span data-stu-id="beb60-115">If the *x* parameter is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="beb60-116">Descripción del tipo</span><span class="sxs-lookup"><span data-stu-id="beb60-116">Type Description</span></span>



| <span data-ttu-id="beb60-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="beb60-117">Name</span></span>  | [<span data-ttu-id="beb60-118">**Tipo de plantilla**</span><span class="sxs-lookup"><span data-stu-id="beb60-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="beb60-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="beb60-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="beb60-120">Tamaño</span><span class="sxs-lookup"><span data-stu-id="beb60-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="beb60-121">*x*</span><span class="sxs-lookup"><span data-stu-id="beb60-121">*x*</span></span>   | <span data-ttu-id="beb60-122">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz**</span><span class="sxs-lookup"><span data-stu-id="beb60-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="beb60-123">**flot**</span><span class="sxs-lookup"><span data-stu-id="beb60-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="beb60-124">cualquiera</span><span class="sxs-lookup"><span data-stu-id="beb60-124">any</span></span>                            |
| <span data-ttu-id="beb60-125">*direcc*</span><span class="sxs-lookup"><span data-stu-id="beb60-125">*ret*</span></span> | <span data-ttu-id="beb60-126">igual que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="beb60-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="beb60-127">**flot**</span><span class="sxs-lookup"><span data-stu-id="beb60-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="beb60-128">mismas dimensiones que la entrada *x*</span><span class="sxs-lookup"><span data-stu-id="beb60-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="beb60-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="beb60-129">Minimum Shader Model</span></span>

<span data-ttu-id="beb60-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="beb60-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="beb60-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="beb60-131">Shader Model</span></span>                                                                       | <span data-ttu-id="beb60-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="beb60-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="beb60-133">Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos</span><span class="sxs-lookup"><span data-stu-id="beb60-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="beb60-134">sí</span><span class="sxs-lookup"><span data-stu-id="beb60-134">yes</span></span>                 |
| [<span data-ttu-id="beb60-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="beb60-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="beb60-136">sí ( \_ solo vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="beb60-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="beb60-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="beb60-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb60-138">**Funciones intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="beb60-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

