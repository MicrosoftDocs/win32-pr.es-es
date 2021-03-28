---
title: atomic_and (SM5-ASM)
description: And bit a bit atómico en la memoria.
ms.assetid: 5FA731E0-7D18-4416-9579-FCA01FF5FC38
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef21f2f9d49a05f1eeb828ee1ce54ad1f162d7a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983894"
---
# <a name="atomic_and-sm5---asm"></a><span data-ttu-id="73111-103">Atomic \_ y (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="73111-103">atomic\_and (sm5 - asm)</span></span>

<span data-ttu-id="73111-104">And bit a bit atómico en la memoria.</span><span class="sxs-lookup"><span data-stu-id="73111-104">Atomic bitwise AND to memory.</span></span>



| <span data-ttu-id="73111-105">Atomic \_ and DST, dstAddress \[ . swizzle \] , src0 \[ . Select ( \_ componente)\]</span><span class="sxs-lookup"><span data-stu-id="73111-105">atomic\_and dst, dstAddress\[.swizzle\], src0\[.select\_component\]</span></span> |
|---------------------------------------------------------------------|



 



| <span data-ttu-id="73111-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="73111-106">Item</span></span>                                                                                                           | <span data-ttu-id="73111-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="73111-107">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73111-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="73111-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="73111-109">\[en \] los componentes de y con *src0*.</span><span class="sxs-lookup"><span data-stu-id="73111-109">\[in\] The components to AND with *src0*.</span></span> <span data-ttu-id="73111-110">Este valor debe ser una vista de acceso desordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="73111-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="73111-111">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="73111-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="73111-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="73111-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="73111-113">\[en \] la dirección de memoria.</span><span class="sxs-lookup"><span data-stu-id="73111-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                 |
| <span data-ttu-id="73111-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="73111-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="73111-115">\[en \] los componentes de y con *DST*.</span><span class="sxs-lookup"><span data-stu-id="73111-115">\[in\] The components to AND with *dst*.</span></span><br/>                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="73111-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73111-116">Remarks</span></span>

<span data-ttu-id="73111-117">Esta operación realiza un único componente bit a bit de 32 bits y de operando *src0* en el *DST* de 32 bits por cada dirección de componente *dstAddress*, que se realiza de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="73111-117">This operation performs a single component 32-bit bitwise AND of operand *src0* into *dst* at 32-bit per component address *dstAddress*, performed atomically.</span></span>

<span data-ttu-id="73111-118">El número de componentes tomado de la dirección viene determinado por la dimensionalidad del *DST* u \# o g \# .</span><span class="sxs-lookup"><span data-stu-id="73111-118">The number of components taken from the address is determined by the dimensionality of *dst* u\# or g\#.</span></span>

<span data-ttu-id="73111-119">Si el *DST* es una u \# , se puede declarar como sin formato, con tipo o estructurada.</span><span class="sxs-lookup"><span data-stu-id="73111-119">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="73111-120">Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="73111-120">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="73111-121">Si *DST* es g \# , debe declararse como RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="73111-121">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="73111-122">No se devuelve nada al sombreador.</span><span class="sxs-lookup"><span data-stu-id="73111-122">Nothing is returned to the shader.</span></span>

<span data-ttu-id="73111-123">Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel/ejemplo para servir como ayudante a un píxel o ejemplo real para los derivados, esta instrucción no modifica la memoria de *DST* en absoluto (en modo silencioso).</span><span class="sxs-lookup"><span data-stu-id="73111-123">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample invocation only exists to serve as a helper to a real pixel/sample for derivatives, this instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="73111-124">Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.</span><span class="sxs-lookup"><span data-stu-id="73111-124">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="73111-125">Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida), hace que todo el contenido de toda la memoria compartida quede sin definir.</span><span class="sxs-lookup"><span data-stu-id="73111-125">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="73111-126">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="73111-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="73111-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="73111-127">Vertex</span></span> | <span data-ttu-id="73111-128">Casco</span><span class="sxs-lookup"><span data-stu-id="73111-128">Hull</span></span> | <span data-ttu-id="73111-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="73111-129">Domain</span></span> | <span data-ttu-id="73111-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="73111-130">Geometry</span></span> | <span data-ttu-id="73111-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="73111-131">Pixel</span></span> | <span data-ttu-id="73111-132">Compute</span><span class="sxs-lookup"><span data-stu-id="73111-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="73111-133">X</span><span class="sxs-lookup"><span data-stu-id="73111-133">X</span></span>     | <span data-ttu-id="73111-134">X</span><span class="sxs-lookup"><span data-stu-id="73111-134">X</span></span>       |



 

<span data-ttu-id="73111-135">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="73111-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="73111-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="73111-136">Vertex</span></span> | <span data-ttu-id="73111-137">Casco</span><span class="sxs-lookup"><span data-stu-id="73111-137">Hull</span></span> | <span data-ttu-id="73111-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="73111-138">Domain</span></span> | <span data-ttu-id="73111-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="73111-139">Geometry</span></span> | <span data-ttu-id="73111-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="73111-140">Pixel</span></span> | <span data-ttu-id="73111-141">Compute</span><span class="sxs-lookup"><span data-stu-id="73111-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="73111-142">X</span><span class="sxs-lookup"><span data-stu-id="73111-142">X</span></span>      | <span data-ttu-id="73111-143">X</span><span class="sxs-lookup"><span data-stu-id="73111-143">X</span></span>    | <span data-ttu-id="73111-144">X</span><span class="sxs-lookup"><span data-stu-id="73111-144">X</span></span>      | <span data-ttu-id="73111-145">X</span><span class="sxs-lookup"><span data-stu-id="73111-145">X</span></span>        | <span data-ttu-id="73111-146">X</span><span class="sxs-lookup"><span data-stu-id="73111-146">X</span></span>     | <span data-ttu-id="73111-147">X</span><span class="sxs-lookup"><span data-stu-id="73111-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="73111-148">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="73111-148">Minimum Shader Model</span></span>

<span data-ttu-id="73111-149">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="73111-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="73111-150">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="73111-150">Shader Model</span></span>                                              | <span data-ttu-id="73111-151">Compatible</span><span class="sxs-lookup"><span data-stu-id="73111-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="73111-152">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="73111-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="73111-153">sí</span><span class="sxs-lookup"><span data-stu-id="73111-153">yes</span></span>       |
| [<span data-ttu-id="73111-154">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="73111-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="73111-155">no</span><span class="sxs-lookup"><span data-stu-id="73111-155">no</span></span>        |
| [<span data-ttu-id="73111-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="73111-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="73111-157">no</span><span class="sxs-lookup"><span data-stu-id="73111-157">no</span></span>        |
| [<span data-ttu-id="73111-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73111-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="73111-159">no</span><span class="sxs-lookup"><span data-stu-id="73111-159">no</span></span>        |
| [<span data-ttu-id="73111-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73111-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="73111-161">no</span><span class="sxs-lookup"><span data-stu-id="73111-161">no</span></span>        |
| [<span data-ttu-id="73111-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73111-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="73111-163">no</span><span class="sxs-lookup"><span data-stu-id="73111-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="73111-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73111-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73111-165">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73111-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





