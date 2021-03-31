---
description: Multiplica dos cuaterniones.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Función D3DXQuaternionMultiply (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 753fd206e2b970182ed44c216f1339d56973c416
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157228"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a><span data-ttu-id="52df6-103">Función D3DXQuaternionMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="52df6-103">D3DXQuaternionMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="52df6-104">Multiplica dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="52df6-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="52df6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52df6-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="52df6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52df6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52df6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="52df6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52df6-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="52df6-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52df6-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="52df6-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="52df6-110">*pQ1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52df6-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52df6-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52df6-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52df6-112">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="52df6-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="52df6-113">*pQ2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52df6-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52df6-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="52df6-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52df6-115">Puntero a una estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="52df6-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52df6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52df6-116">Return value</span></span>

<span data-ttu-id="52df6-117">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="52df6-117">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="52df6-118">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el producto de dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="52df6-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="52df6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52df6-119">Remarks</span></span>

<span data-ttu-id="52df6-120">El resultado representa la rotación Q1 seguida de la rotación T2 (out = T2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="52df6-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="52df6-121">Esto se hace para que **D3DXQuaternionMultiply** mantenga la misma semántica que [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) , ya que los cuaterniones unidades se pueden considerar como otra manera de representar matrices de rotación.</span><span class="sxs-lookup"><span data-stu-id="52df6-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="52df6-122">Las transformaciones se concatenan en el mismo orden para las funciones **D3DXQuaternionMultiply** y [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) .</span><span class="sxs-lookup"><span data-stu-id="52df6-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) functions.</span></span> <span data-ttu-id="52df6-123">Por ejemplo, suponiendo que mX y mY representan los mismos giros que qX y qY, tanto m como q representarán los mismos giros.</span><span class="sxs-lookup"><span data-stu-id="52df6-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="52df6-124">La multiplicación de cuaterniones no es conmutativa.</span><span class="sxs-lookup"><span data-stu-id="52df6-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="52df6-125">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="52df6-125">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="52df6-126">De esta manera, la función **D3DXQuaternionMultiply** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="52df6-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="52df6-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="52df6-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="52df6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52df6-128">Requirements</span></span>



| <span data-ttu-id="52df6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="52df6-129">Requirement</span></span> | <span data-ttu-id="52df6-130">Value</span><span class="sxs-lookup"><span data-stu-id="52df6-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52df6-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52df6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="52df6-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="52df6-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="52df6-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52df6-133">Library</span></span><br/> | <dl> <span data-ttu-id="52df6-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52df6-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52df6-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="52df6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52df6-136">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="52df6-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="52df6-137">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="52df6-137">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




