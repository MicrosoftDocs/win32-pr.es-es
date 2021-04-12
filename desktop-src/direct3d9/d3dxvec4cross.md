---
description: Determina el producto cruzado en cuatro dimensiones.
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: Función D3DXVec4Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91e6e5662bff503ba96d96f135f98e60cf15c8fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280358"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="c482d-103">Función D3DXVec4Cross (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c482d-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="c482d-104">Determina el producto cruzado en cuatro dimensiones.</span><span class="sxs-lookup"><span data-stu-id="c482d-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c482d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c482d-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="c482d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c482d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c482d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c482d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c482d-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c482d-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c482d-109">Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c482d-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c482d-110">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c482d-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c482d-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c482d-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c482d-112">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c482d-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c482d-113">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c482d-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c482d-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c482d-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c482d-115">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c482d-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c482d-116">*pV3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c482d-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c482d-117">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c482d-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c482d-118">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="c482d-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c482d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c482d-119">Return value</span></span>

<span data-ttu-id="c482d-120">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c482d-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c482d-121">Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el producto cruzado.</span><span class="sxs-lookup"><span data-stu-id="c482d-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="c482d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c482d-122">Remarks</span></span>

<span data-ttu-id="c482d-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="c482d-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c482d-124">De esta manera, la función **D3DXVec4Cross** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="c482d-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c482d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c482d-125">Requirements</span></span>



| <span data-ttu-id="c482d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c482d-126">Requirement</span></span> | <span data-ttu-id="c482d-127">Value</span><span class="sxs-lookup"><span data-stu-id="c482d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c482d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c482d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c482d-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c482d-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c482d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c482d-130">Library</span></span><br/> | <dl> <span data-ttu-id="c482d-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c482d-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c482d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c482d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c482d-133">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c482d-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c482d-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="c482d-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




