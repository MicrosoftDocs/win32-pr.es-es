---
description: Devuelve la versión normalizada de un vector 3D.
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: Función D3DXVec3Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 413b807c53e0b46b115af2aa283e4902a45f5979
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914782"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="34554-103">Función D3DXVec3Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="34554-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="34554-104">Devuelve la versión normalizada de un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="34554-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="34554-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34554-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="34554-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34554-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34554-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="34554-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34554-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="34554-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="34554-109">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="34554-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="34554-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34554-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34554-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="34554-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="34554-112">Puntero a la estructura de D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="34554-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34554-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34554-113">Return value</span></span>

<span data-ttu-id="34554-114">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="34554-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="34554-115">Puntero a una estructura D3DXVECTOR3 que es la versión normalizada del vector especificado.</span><span class="sxs-lookup"><span data-stu-id="34554-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="34554-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34554-116">Remarks</span></span>

<span data-ttu-id="34554-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="34554-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="34554-118">De esta manera, la función D3DXVec3Normalize se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="34554-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="34554-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34554-119">Requirements</span></span>



| <span data-ttu-id="34554-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="34554-120">Requirement</span></span> | <span data-ttu-id="34554-121">Value</span><span class="sxs-lookup"><span data-stu-id="34554-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34554-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34554-122">Header</span></span><br/> | <dl> <span data-ttu-id="34554-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="34554-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34554-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="34554-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34554-125">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="34554-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
