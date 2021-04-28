---
description: 'Método ID3DXConstantTable::SetMatrixArray: establece una matriz de matrices no transaccionadas.'
ms.assetid: f36b8e8a-c22f-41e6-acb1-6298291b002f
title: Método ID3DXConstantTable::SetMatrixArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 02e115cf4526ab065d2613636427059826f450f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115103"
---
# <a name="id3dxconstanttablesetmatrixarray-method"></a><span data-ttu-id="8f049-103">Método ID3DXConstantTable::SetMatrixArray</span><span class="sxs-lookup"><span data-stu-id="8f049-103">ID3DXConstantTable::SetMatrixArray method</span></span>

<span data-ttu-id="8f049-104">Establece una matriz de matrices no transaccionadas.</span><span class="sxs-lookup"><span data-stu-id="8f049-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f049-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f049-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="8f049-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f049-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8f049-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f049-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8f049-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8f049-109">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="8f049-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="8f049-110">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8f049-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f049-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8f049-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8f049-112">Identificador único de la matriz de matrices constantes.</span><span class="sxs-lookup"><span data-stu-id="8f049-112">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="8f049-113">Vea [D3DXHANDLE.](dx9-graphics-reference-effects-constants.md)</span><span class="sxs-lookup"><span data-stu-id="8f049-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f049-114">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8f049-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f049-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f049-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8f049-116">Matriz de matrices no transaccionadas.</span><span class="sxs-lookup"><span data-stu-id="8f049-116">Array of nontransposed matrices.</span></span> <span data-ttu-id="8f049-117">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="8f049-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f049-118">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8f049-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f049-119">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f049-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f049-120">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8f049-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f049-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f049-121">Return value</span></span>

<span data-ttu-id="8f049-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8f049-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8f049-123">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8f049-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8f049-124">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8f049-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f049-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f049-125">Requirements</span></span>



| <span data-ttu-id="8f049-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f049-126">Requirement</span></span> | <span data-ttu-id="8f049-127">Value</span><span class="sxs-lookup"><span data-stu-id="8f049-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f049-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f049-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8f049-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="8f049-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8f049-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f049-130">Library</span></span><br/> | <dl> <span data-ttu-id="8f049-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f049-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8f049-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f049-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f049-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="8f049-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
