---
description: 'Función D3DXFresnelTerm (D3dx9math.h): calcule el término Fresnel.'
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: Función D3DXFresnelTerm (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5472f9839928fd3b4c1830bc309c7f610d487864
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114483"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a><span data-ttu-id="097c4-103">Función D3DXFresnelTerm (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="097c4-103">D3DXFresnelTerm function (D3dx9math.h)</span></span>

<span data-ttu-id="097c4-104">Calcule el término Fresnel.</span><span class="sxs-lookup"><span data-stu-id="097c4-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="097c4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="097c4-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="097c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="097c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097c4-107">*CosTheta* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="097c4-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097c4-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="097c4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="097c4-109">El valor debe estar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="097c4-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="097c4-110">*RefracciónIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="097c4-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097c4-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="097c4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="097c4-112">Índice de retracción de un material.</span><span class="sxs-lookup"><span data-stu-id="097c4-112">The refraction index of a material.</span></span> <span data-ttu-id="097c4-113">El valor debe ser mayor que 1.</span><span class="sxs-lookup"><span data-stu-id="097c4-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097c4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="097c4-114">Return value</span></span>

<span data-ttu-id="097c4-115">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="097c4-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="097c4-116">Esta función devuelve el término Fresnel para la luz nopolarizada.</span><span class="sxs-lookup"><span data-stu-id="097c4-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="097c4-117">CosTheta es el coseno del ángulo del incidente.</span><span class="sxs-lookup"><span data-stu-id="097c4-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="097c4-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="097c4-118">Remarks</span></span>

<span data-ttu-id="097c4-119">Para buscar el término Fresnel (F):</span><span class="sxs-lookup"><span data-stu-id="097c4-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="097c4-120">Si A es ángulo de incidencia y B es el ángulo de retracción, entonces</span><span class="sxs-lookup"><span data-stu-id="097c4-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="097c4-121">A continuación, al expandir mediante las identidades trig y simplificar, obtiene lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="097c4-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="097c4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="097c4-122">Requirements</span></span>



| <span data-ttu-id="097c4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="097c4-123">Requirement</span></span> | <span data-ttu-id="097c4-124">Value</span><span class="sxs-lookup"><span data-stu-id="097c4-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="097c4-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="097c4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="097c4-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="097c4-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="097c4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="097c4-127">Library</span></span><br/> | <dl> <span data-ttu-id="097c4-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="097c4-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="097c4-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="097c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097c4-130">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="097c4-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
