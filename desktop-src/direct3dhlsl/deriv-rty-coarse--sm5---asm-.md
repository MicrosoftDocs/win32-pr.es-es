---
title: deriv_rty_coarse (SM5-ASM)
description: Calcula la tasa de cambio de los componentes. | deriv_rty_coarse (SM5-ASM)
ms.assetid: 1EBCC0B9-BD3E-46DD-AC17-F7167F892195
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7fd539adf8587118a6bdfdcb5959925e6a97f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998169"
---
# <a name="deriv_rty_coarse-sm5---asm"></a><span data-ttu-id="5a3a2-104">derivar \_ propiedad \_ grueso (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5a3a2-104">deriv\_rty\_coarse (sm5 - asm)</span></span>

<span data-ttu-id="5a3a2-105">Calcula la tasa de cambio de los componentes.</span><span class="sxs-lookup"><span data-stu-id="5a3a2-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="5a3a2-106">derive \_ propiedad \_ General \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="5a3a2-106">deriv\_rty\_coarse\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|----------------------------------------------------------------------------|



 



| <span data-ttu-id="5a3a2-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5a3a2-107">Item</span></span>                                                            | <span data-ttu-id="5a3a2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a3a2-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="5a3a2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5a3a2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5a3a2-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="5a3a2-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="5a3a2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5a3a2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5a3a2-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="5a3a2-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="5a3a2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a3a2-113">Remarks</span></span>

<span data-ttu-id="5a3a2-114">Para obtener más información, vea [derive \_ RTX \_ grueso.](deriv-rtx-coarse--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="5a3a2-114">For more information, see [deriv\_rtx\_coarse.](deriv-rtx-coarse--sm5---asm-.md)</span></span>

<span data-ttu-id="5a3a2-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="5a3a2-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5a3a2-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="5a3a2-116">Vertex</span></span> | <span data-ttu-id="5a3a2-117">Casco</span><span class="sxs-lookup"><span data-stu-id="5a3a2-117">Hull</span></span> | <span data-ttu-id="5a3a2-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="5a3a2-118">Domain</span></span> | <span data-ttu-id="5a3a2-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="5a3a2-119">Geometry</span></span> | <span data-ttu-id="5a3a2-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="5a3a2-120">Pixel</span></span> | <span data-ttu-id="5a3a2-121">Compute</span><span class="sxs-lookup"><span data-stu-id="5a3a2-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5a3a2-122">X</span><span class="sxs-lookup"><span data-stu-id="5a3a2-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5a3a2-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="5a3a2-123">Minimum Shader Model</span></span>

<span data-ttu-id="5a3a2-124">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="5a3a2-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5a3a2-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5a3a2-125">Shader Model</span></span>                                              | <span data-ttu-id="5a3a2-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="5a3a2-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5a3a2-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5a3a2-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5a3a2-128">sí</span><span class="sxs-lookup"><span data-stu-id="5a3a2-128">yes</span></span>       |
| [<span data-ttu-id="5a3a2-129">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5a3a2-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5a3a2-130">no</span><span class="sxs-lookup"><span data-stu-id="5a3a2-130">no</span></span>        |
| [<span data-ttu-id="5a3a2-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5a3a2-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5a3a2-132">no</span><span class="sxs-lookup"><span data-stu-id="5a3a2-132">no</span></span>        |
| [<span data-ttu-id="5a3a2-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a3a2-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5a3a2-134">no</span><span class="sxs-lookup"><span data-stu-id="5a3a2-134">no</span></span>        |
| [<span data-ttu-id="5a3a2-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a3a2-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5a3a2-136">no</span><span class="sxs-lookup"><span data-stu-id="5a3a2-136">no</span></span>        |
| [<span data-ttu-id="5a3a2-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a3a2-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5a3a2-138">no</span><span class="sxs-lookup"><span data-stu-id="5a3a2-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5a3a2-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a3a2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a3a2-140">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a3a2-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





