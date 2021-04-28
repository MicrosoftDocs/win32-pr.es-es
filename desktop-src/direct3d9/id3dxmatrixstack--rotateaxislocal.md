---
description: 'Método ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h): gira (con respecto al espacio de coordenadas local del objeto) alrededor de un eje arbitrario.'
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: Método ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfcfd7301f90dcf49b03e7bbb3fd7e3b0de6c3e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093473"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="2b2c7-103">Método ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="2b2c7-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="2b2c7-104">Gira (en relación con el espacio de coordenadas local del objeto) alrededor de un eje arbitrario.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b2c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b2c7-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="2b2c7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b2c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b2c7-107">*pV* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b2c7-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2c7-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b2c7-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b2c7-109">Puntero al eje arbitrario de rotación.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="2b2c7-110">Vea [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="2b2c7-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b2c7-111">*Ángulo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2b2c7-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b2c7-112">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b2c7-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b2c7-113">Ángulo de rotación sobre el eje arbitrario, en radianes.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="2b2c7-114">Los ángulos se miden en sentido contrario a las agujas del reloj al mirar a lo largo del eje arbitrario hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b2c7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b2c7-115">Return value</span></span>

<span data-ttu-id="2b2c7-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b2c7-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b2c7-117">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b2c7-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b2c7-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b2c7-119">Remarks</span></span>

<span data-ttu-id="2b2c7-120">Este método agrega la rotación a la pila de matriz con la matriz de rotación calculada similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="2b2c7-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="2b2c7-121">Dado que la rotación se multiplica a la izquierda en la pila de matriz, la rotación es relativa al espacio de coordenadas local del objeto.</span><span class="sxs-lookup"><span data-stu-id="2b2c7-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b2c7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b2c7-122">Requirements</span></span>



| <span data-ttu-id="2b2c7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b2c7-123">Requirement</span></span> | <span data-ttu-id="2b2c7-124">Value</span><span class="sxs-lookup"><span data-stu-id="2b2c7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2c7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b2c7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2b2c7-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2b2c7-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2b2c7-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b2c7-127">Library</span></span><br/> | <dl> <span data-ttu-id="2b2c7-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b2c7-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b2c7-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2b2c7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2c7-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="2b2c7-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2b2c7-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="2b2c7-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="2b2c7-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="2b2c7-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="2b2c7-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="2b2c7-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="2b2c7-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="2b2c7-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
