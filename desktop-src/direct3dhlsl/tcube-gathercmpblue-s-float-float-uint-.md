---
title: 'TextureCube:: GatherCmpBlue (S, Float, Float, uint) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación junto con el estado de asignación de mosaicos. | TextureCube:: GatherCmpBlue (S, Float, Float, uint) (función)'
ms.assetid: 1D1FFF0E-9CA7-48A4-A305-C0B6059056E7
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
ms.openlocfilehash: 2022546bb01137e730b4e0f720dbb2c3c091d609
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986319"
---
# <a name="texturecubegathercmpbluesfloatfloatuint-function"></a><span data-ttu-id="25826-105">TextureCube:: GatherCmpBlue (S, Float, Float, uint) (función)</span><span class="sxs-lookup"><span data-stu-id="25826-105">TextureCube::GatherCmpBlue(S,float,float,uint) function</span></span>

<span data-ttu-id="25826-106">En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente azul con respecto a un valor de comparación junto con el estado de asignación de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="25826-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value along with tile-mapping status.</span></span>

## <a name="syntax"></a><span data-ttu-id="25826-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25826-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpBlue(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="25826-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25826-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25826-109">*S* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="25826-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25826-110">Tipo: **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="25826-110">Type: **SamplerState**</span></span>

<span data-ttu-id="25826-111">Índice de muestra de base cero.</span><span class="sxs-lookup"><span data-stu-id="25826-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="25826-112">*Ubicación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="25826-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25826-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="25826-113">Type: **float**</span></span>

<span data-ttu-id="25826-114">Coordenadas de ejemplo (u, v).</span><span class="sxs-lookup"><span data-stu-id="25826-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="25826-115">*CompareValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="25826-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25826-116">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="25826-116">Type: **float**</span></span>

<span data-ttu-id="25826-117">Valor que se va a comparar cada uno con cada valor muestreado.</span><span class="sxs-lookup"><span data-stu-id="25826-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="25826-118">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="25826-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25826-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="25826-119">Type: **uint**</span></span>

<span data-ttu-id="25826-120">Estado de la operación.</span><span class="sxs-lookup"><span data-stu-id="25826-120">The status of the operation.</span></span> <span data-ttu-id="25826-121">No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="25826-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="25826-122">**CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="25826-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="25826-123">Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="25826-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25826-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25826-124">Return value</span></span>

<span data-ttu-id="25826-125">Tipo: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="25826-125">Type: **TemplateType**</span></span>

<span data-ttu-id="25826-126">Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="25826-126">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="25826-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25826-127">Remarks</span></span>

<span data-ttu-id="25826-128">Los ejemplos de textura se pueden usar para la interpolación bilineal.</span><span class="sxs-lookup"><span data-stu-id="25826-128">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="25826-129">Esta función se admite para los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="25826-129">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="25826-130">Vértice</span><span class="sxs-lookup"><span data-stu-id="25826-130">Vertex</span></span> | <span data-ttu-id="25826-131">Casco</span><span class="sxs-lookup"><span data-stu-id="25826-131">Hull</span></span> | <span data-ttu-id="25826-132">Dominio</span><span class="sxs-lookup"><span data-stu-id="25826-132">Domain</span></span> | <span data-ttu-id="25826-133">Geometría</span><span class="sxs-lookup"><span data-stu-id="25826-133">Geometry</span></span> | <span data-ttu-id="25826-134">Píxel</span><span class="sxs-lookup"><span data-stu-id="25826-134">Pixel</span></span> | <span data-ttu-id="25826-135">Compute</span><span class="sxs-lookup"><span data-stu-id="25826-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="25826-136">x</span><span class="sxs-lookup"><span data-stu-id="25826-136">x</span></span>      | <span data-ttu-id="25826-137">x</span><span class="sxs-lookup"><span data-stu-id="25826-137">x</span></span>    | <span data-ttu-id="25826-138">x</span><span class="sxs-lookup"><span data-stu-id="25826-138">x</span></span>      | <span data-ttu-id="25826-139">x</span><span class="sxs-lookup"><span data-stu-id="25826-139">x</span></span>        | <span data-ttu-id="25826-140">x</span><span class="sxs-lookup"><span data-stu-id="25826-140">x</span></span>     | <span data-ttu-id="25826-141">x</span><span class="sxs-lookup"><span data-stu-id="25826-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="25826-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="25826-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25826-143">Métodos GatherCmpBlue</span><span class="sxs-lookup"><span data-stu-id="25826-143">GatherCmpBlue methods</span></span>](texturecube-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="25826-144">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="25826-144">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
