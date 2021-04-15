---
description: Crea un cuaternión con el guiñada, el tono y el rollo dados.
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: Función D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d0df60149643db0d9243afe57e394320f81d08c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707867"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="fcbda-103">Función D3DXQuaternionRotationYawPitchRoll (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fcbda-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="fcbda-104">Crea un cuaternión con el guiñada, el tono y el rollo dados.</span><span class="sxs-lookup"><span data-stu-id="fcbda-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbda-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcbda-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="fcbda-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcbda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbda-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fcbda-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbda-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcbda-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fcbda-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fcbda-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fcbda-110">*Guiñada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcbda-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbda-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcbda-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcbda-112">Guiña alrededor del eje y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="fcbda-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="fcbda-113">*Paso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcbda-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbda-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcbda-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcbda-115">Paso alrededor del eje x, en radianes.</span><span class="sxs-lookup"><span data-stu-id="fcbda-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="fcbda-116">Poner al *día* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fcbda-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbda-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcbda-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcbda-118">Desplazarse alrededor del eje z, en radianes.</span><span class="sxs-lookup"><span data-stu-id="fcbda-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbda-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcbda-119">Return value</span></span>

<span data-ttu-id="fcbda-120">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcbda-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fcbda-121">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) con el guiñada, el tono y el rollo especificados.</span><span class="sxs-lookup"><span data-stu-id="fcbda-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcbda-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcbda-122">Remarks</span></span>

<span data-ttu-id="fcbda-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="fcbda-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fcbda-124">De esta manera, la función **D3DXQuaternionRotationYawPitchRoll** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="fcbda-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fcbda-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="fcbda-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcbda-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcbda-126">Requirements</span></span>



| <span data-ttu-id="fcbda-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcbda-127">Requirement</span></span> | <span data-ttu-id="fcbda-128">Value</span><span class="sxs-lookup"><span data-stu-id="fcbda-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbda-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcbda-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fcbda-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcbda-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fcbda-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcbda-131">Library</span></span><br/> | <dl> <span data-ttu-id="fcbda-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcbda-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fcbda-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcbda-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbda-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fcbda-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fcbda-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="fcbda-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="fcbda-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="fcbda-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
