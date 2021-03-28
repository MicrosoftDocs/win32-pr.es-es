---
title: 'SampleBias:: SampleBias (S, Float, Float, Float, uint) (función)'
description: 'Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. Devuelve el estado de la operación. | SampleBias:: SampleBias (S, Float, Float, Float, uint) (función)'
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
keywords:
- SampleBias de función HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f3a994d7b0f0c2d55ae3203db9f3205932c1a25
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280099"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function"></a><span data-ttu-id="63048-106">SampleBias:: SampleBias (S, Float, Float, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="63048-106">SampleBias::SampleBias(S,float,float,float,uint) function</span></span>

<span data-ttu-id="63048-107">Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.</span><span class="sxs-lookup"><span data-stu-id="63048-107">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="63048-108">Devuelve el estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="63048-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="63048-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63048-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="63048-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63048-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63048-111">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="63048-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63048-112">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="63048-112">Type: **SamplerState**</span></span>

<span data-ttu-id="63048-113">Un [Estado de muestra](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="63048-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="63048-114">Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.</span><span class="sxs-lookup"><span data-stu-id="63048-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="63048-115">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="63048-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63048-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="63048-116">Type: **float**</span></span>

<span data-ttu-id="63048-117">Las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="63048-117">The texture coordinates.</span></span> <span data-ttu-id="63048-118">El tipo de argumento depende del tipo de objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="63048-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="63048-119">Tipo de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="63048-119">Texture-Object Type</span></span>                    | <span data-ttu-id="63048-120">Tipo de parámetro</span><span class="sxs-lookup"><span data-stu-id="63048-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="63048-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="63048-121">Texture1D</span></span>                              | <span data-ttu-id="63048-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="63048-122">float</span></span>          |
| <span data-ttu-id="63048-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="63048-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="63048-124">float2</span><span class="sxs-lookup"><span data-stu-id="63048-124">float2</span></span>         |
| <span data-ttu-id="63048-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="63048-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="63048-126">float3</span><span class="sxs-lookup"><span data-stu-id="63048-126">float3</span></span>         |
| <span data-ttu-id="63048-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="63048-127">TextureCubeArray</span></span>                       | <span data-ttu-id="63048-128">float4</span><span class="sxs-lookup"><span data-stu-id="63048-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="63048-129">*Bias* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63048-129">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63048-130">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="63048-130">Type: **float**</span></span>

<span data-ttu-id="63048-131">El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="63048-131">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="63048-132">*Abrazadera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63048-132">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63048-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="63048-133">Type: **float**</span></span>

<span data-ttu-id="63048-134">Un valor opcional en el que se van a fijar los valores LOD de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="63048-134">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="63048-135">Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.</span><span class="sxs-lookup"><span data-stu-id="63048-135">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="63048-136">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="63048-136">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63048-137">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="63048-137">Type: **uint**</span></span>

<span data-ttu-id="63048-138">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="63048-138">The status of the operation.</span></span> <span data-ttu-id="63048-139">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="63048-139">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="63048-140">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="63048-140">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="63048-141">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="63048-141">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63048-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63048-142">Return value</span></span>

<span data-ttu-id="63048-143">Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="63048-143">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="63048-144">Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="63048-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="63048-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="63048-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63048-146">Métodos SampleBias</span><span class="sxs-lookup"><span data-stu-id="63048-146">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="63048-147">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="63048-147">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
