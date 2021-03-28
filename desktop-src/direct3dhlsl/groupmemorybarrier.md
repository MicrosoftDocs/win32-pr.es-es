---
title: GroupMemoryBarrier función)
description: Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos compartidos de grupo.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- GroupMemoryBarrier de función HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54a140a892b0e9144ef23fc0290ca3bb3747e90a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076470"
---
# <a name="groupmemorybarrier-function"></a><span data-ttu-id="2426f-104">GroupMemoryBarrier función)</span><span class="sxs-lookup"><span data-stu-id="2426f-104">GroupMemoryBarrier function</span></span>

<span data-ttu-id="2426f-105">Bloquea la ejecución de todos los subprocesos de un grupo hasta que se hayan completado todos los accesos compartidos de grupo.</span><span class="sxs-lookup"><span data-stu-id="2426f-105">Blocks execution of all threads in a group until all group shared accesses have been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2426f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2426f-106">Syntax</span></span>

``` syntax
void GroupMemoryBarrier(void);
```

## <a name="parameters"></a><span data-ttu-id="2426f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2426f-107">Parameters</span></span>

<span data-ttu-id="2426f-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2426f-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2426f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2426f-109">Return value</span></span>

<span data-ttu-id="2426f-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2426f-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2426f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2426f-111">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2426f-112">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2426f-112">Minimum Shader Model</span></span>

<span data-ttu-id="2426f-113">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2426f-113">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2426f-114">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2426f-114">Shader Model</span></span>                                                                | <span data-ttu-id="2426f-115">Compatible</span><span class="sxs-lookup"><span data-stu-id="2426f-115">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2426f-116">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="2426f-116">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2426f-117">sí</span><span class="sxs-lookup"><span data-stu-id="2426f-117">yes</span></span>       |



 

<span data-ttu-id="2426f-118">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2426f-118">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2426f-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="2426f-119">Vertex</span></span> | <span data-ttu-id="2426f-120">Casco</span><span class="sxs-lookup"><span data-stu-id="2426f-120">Hull</span></span> | <span data-ttu-id="2426f-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="2426f-121">Domain</span></span> | <span data-ttu-id="2426f-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="2426f-122">Geometry</span></span> | <span data-ttu-id="2426f-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="2426f-123">Pixel</span></span> | <span data-ttu-id="2426f-124">Compute</span><span class="sxs-lookup"><span data-stu-id="2426f-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="2426f-125">x</span><span class="sxs-lookup"><span data-stu-id="2426f-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2426f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2426f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2426f-127">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="2426f-127">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="2426f-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2426f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




