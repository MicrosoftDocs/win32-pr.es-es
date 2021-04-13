---
description: Proyecta un vector 3D desde el espacio de objetos en el espacio de pantalla.
ms.assetid: 6fc59788-c3f7-4f47-a345-9108105e820e
title: Función D3DXVec3Project (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c8d86949f754afb7639a0c28ff6d8b14c0e40ff0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362594"
---
# <a name="d3dxvec3project-function-d3dx10mathh"></a><span data-ttu-id="4c406-103">Función D3DXVec3Project (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4c406-103">D3DXVec3Project function (D3DX10Math.h)</span></span>

<span data-ttu-id="4c406-104">Proyecta un vector 3D desde el espacio de objetos en el espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="4c406-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c406-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c406-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="4c406-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c406-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c406-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4c406-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c406-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c406-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c406-109">Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="4c406-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c406-110">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c406-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c406-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c406-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c406-112">Puntero a la estructura de D3DXVECTOR3 de origen.</span><span class="sxs-lookup"><span data-stu-id="4c406-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c406-113">*pViewport* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c406-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c406-114">Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="4c406-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="4c406-115">Puntero a una [**\_ ventanilla D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)que representa la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="4c406-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="4c406-116">*pProjection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c406-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c406-117">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c406-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c406-118">Puntero a una estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que representa la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="4c406-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="4c406-119">*pView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c406-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c406-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c406-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c406-121">Puntero a una estructura D3DXMATRIX que representa la matriz de la vista.</span><span class="sxs-lookup"><span data-stu-id="4c406-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="4c406-122">*pWorld* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c406-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c406-123">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c406-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c406-124">Puntero a una estructura D3DXMATRIX que representa la matriz universal.</span><span class="sxs-lookup"><span data-stu-id="4c406-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c406-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c406-125">Return value</span></span>

<span data-ttu-id="4c406-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c406-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="4c406-127">Puntero a una estructura D3DXVECTOR3 que es el vector proyectado desde el espacio de objeto hasta el espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="4c406-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c406-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c406-128">Remarks</span></span>

<span data-ttu-id="4c406-129">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="4c406-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4c406-130">De esta manera, la función D3DXVec3Project se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="4c406-130">In this way, the D3DXVec3Project function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c406-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c406-131">Requirements</span></span>



| <span data-ttu-id="4c406-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c406-132">Requirement</span></span> | <span data-ttu-id="4c406-133">Value</span><span class="sxs-lookup"><span data-stu-id="4c406-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c406-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c406-134">Header</span></span><br/> | <dl> <span data-ttu-id="4c406-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c406-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c406-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c406-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c406-137">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="4c406-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
