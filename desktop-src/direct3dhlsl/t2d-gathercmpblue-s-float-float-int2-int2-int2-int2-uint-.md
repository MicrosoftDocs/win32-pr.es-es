---
title: 'Texture2D:: GatherCmpBlue (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación junto con el estado de asignación de mosaicos. | Texture2D:: GatherCmpBlue (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)'
ms.assetid: 77051550-B2AC-4C51-9EA2-D803BDB2B153
keywords:
- GatherCmpBlue de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9fbd5c8da7671180ea01f741e85cfc2427f1393
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986331"
---
# <a name="texture2dgathercmpbluesfloatfloatint2int2int2int2uint-function"></a><span data-ttu-id="13e48-105">Texture2D:: GatherCmpBlue (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="13e48-105">Texture2D::GatherCmpBlue(S,float,float,int2,int2,int2,int2,uint) function</span></span>

<span data-ttu-id="13e48-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="13e48-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e48-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13e48-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="13e48-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13e48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e48-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="13e48-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e48-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="13e48-110">Type: **SamplerState**</span></span>

<span data-ttu-id="13e48-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="13e48-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="13e48-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="13e48-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e48-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="13e48-113">Type: **float**</span></span>

<span data-ttu-id="13e48-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="13e48-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="13e48-115">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13e48-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e48-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="13e48-116">Type: **float**</span></span>

<span data-ttu-id="13e48-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="13e48-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="13e48-118">*Offset1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13e48-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e48-119">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="13e48-119">Type: **int2**</span></span>

<span data-ttu-id="13e48-120">Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="13e48-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="13e48-121">*Offset2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13e48-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e48-122">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="13e48-122">Type: **int2**</span></span>

<span data-ttu-id="13e48-123">Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="13e48-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="13e48-124">*Offset3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13e48-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e48-125">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="13e48-125">Type: **int2**</span></span>

<span data-ttu-id="13e48-126">Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="13e48-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="13e48-127">*Offset4* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13e48-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e48-128">Tipo: **INT2**</span><span class="sxs-lookup"><span data-stu-id="13e48-128">Type: **int2**</span></span>

<span data-ttu-id="13e48-129">Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.</span><span class="sxs-lookup"><span data-stu-id="13e48-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="13e48-130">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="13e48-130">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13e48-131">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="13e48-131">Type: **uint**</span></span>

<span data-ttu-id="13e48-132">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="13e48-132">The status of the operation.</span></span> <span data-ttu-id="13e48-133">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="13e48-133">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="13e48-134">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="13e48-134">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="13e48-135">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="13e48-135">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e48-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13e48-136">Return value</span></span>

<span data-ttu-id="13e48-137">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="13e48-137">Type: **TemplateType**</span></span>

<span data-ttu-id="13e48-138">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="13e48-138">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e48-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13e48-139">Remarks</span></span>

<span data-ttu-id="13e48-140">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="13e48-140">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="13e48-141">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="13e48-141">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="13e48-142">Vértice</span><span class="sxs-lookup"><span data-stu-id="13e48-142">Vertex</span></span> | <span data-ttu-id="13e48-143">Casco</span><span class="sxs-lookup"><span data-stu-id="13e48-143">Hull</span></span> | <span data-ttu-id="13e48-144">Dominio</span><span class="sxs-lookup"><span data-stu-id="13e48-144">Domain</span></span> | <span data-ttu-id="13e48-145">Geometría</span><span class="sxs-lookup"><span data-stu-id="13e48-145">Geometry</span></span> | <span data-ttu-id="13e48-146">Píxel</span><span class="sxs-lookup"><span data-stu-id="13e48-146">Pixel</span></span> | <span data-ttu-id="13e48-147">Compute</span><span class="sxs-lookup"><span data-stu-id="13e48-147">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="13e48-148">x</span><span class="sxs-lookup"><span data-stu-id="13e48-148">x</span></span>      | <span data-ttu-id="13e48-149">x</span><span class="sxs-lookup"><span data-stu-id="13e48-149">x</span></span>    | <span data-ttu-id="13e48-150">x</span><span class="sxs-lookup"><span data-stu-id="13e48-150">x</span></span>      | <span data-ttu-id="13e48-151">x</span><span class="sxs-lookup"><span data-stu-id="13e48-151">x</span></span>        | <span data-ttu-id="13e48-152">x</span><span class="sxs-lookup"><span data-stu-id="13e48-152">x</span></span>     | <span data-ttu-id="13e48-153">x</span><span class="sxs-lookup"><span data-stu-id="13e48-153">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="13e48-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="13e48-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e48-155">Métodos GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="13e48-155">GatherCmpBlue methods</span></span>](texture2d-gathercmpblue.md)
</dt> </dl>

 

 
