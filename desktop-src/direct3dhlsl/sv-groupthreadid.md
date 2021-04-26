---
title: SV_GroupThreadID
description: Índices para los que se ejecuta un subproceso individual dentro de un grupo de subprocesos en el que se ejecuta un sombreador de proceso.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d36e5639b017dfa94e0f3c9f84d6725f6b6a283
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996992"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="a9dff-104">SV \_ GroupThreadID</span><span class="sxs-lookup"><span data-stu-id="a9dff-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="a9dff-105">Índices para los que se ejecuta un subproceso individual dentro de un grupo de subprocesos en el que se ejecuta un sombreador de proceso.</span><span class="sxs-lookup"><span data-stu-id="a9dff-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="a9dff-106">SV \_ GroupThreadID varía según el intervalo especificado para el sombreador de proceso en el [atributo numthreads.](sm5-attributes-numthreads.md)</span><span class="sxs-lookup"><span data-stu-id="a9dff-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="a9dff-107">Por ejemplo, si se especificó numthreads(3,2,1) los valores posibles para el valor de entrada groupThreadID sv tienen este intervalo de valores \_ (0-2,0-1,0).</span><span class="sxs-lookup"><span data-stu-id="a9dff-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="a9dff-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9dff-108">Type</span></span>



|       |
|-------|
| <span data-ttu-id="a9dff-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9dff-109">Type</span></span>  |
| <span data-ttu-id="a9dff-110">uint3</span><span class="sxs-lookup"><span data-stu-id="a9dff-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a9dff-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9dff-111">Remarks</span></span>

<span data-ttu-id="a9dff-112">Este valor del sistema es opcional y siempre está dentro de los límites de los valores pasados al [atributo numthreads.](sm5-attributes-numthreads.md)</span><span class="sxs-lookup"><span data-stu-id="a9dff-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="a9dff-113">En la ilustración siguiente se muestra la relación entre los parámetros pasados a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), los valores especificados en el atributo [numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) y los valores que se pasarán al sombreador de proceso para los valores del sistema relacionados con subprocesos [(SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="a9dff-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![ilustración de la relación entre distribución, grupos de subprocesos y subprocesos](images/threadgroupids.png)

<span data-ttu-id="a9dff-115">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a9dff-115">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="a9dff-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="a9dff-116">Vertex</span></span> | <span data-ttu-id="a9dff-117">Casco</span><span class="sxs-lookup"><span data-stu-id="a9dff-117">Hull</span></span> | <span data-ttu-id="a9dff-118">Domain</span><span class="sxs-lookup"><span data-stu-id="a9dff-118">Domain</span></span> | <span data-ttu-id="a9dff-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="a9dff-119">Geometry</span></span> | <span data-ttu-id="a9dff-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="a9dff-120">Pixel</span></span> | <span data-ttu-id="a9dff-121">Proceso</span><span class="sxs-lookup"><span data-stu-id="a9dff-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="a9dff-122">x</span><span class="sxs-lookup"><span data-stu-id="a9dff-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a9dff-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9dff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9dff-124">Semántica</span><span class="sxs-lookup"><span data-stu-id="a9dff-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="a9dff-125">Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="a9dff-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
