---
description: Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: 'ID3DXKeyframedAnimationSet:: GetCallbackKey (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a3f5a97b84862a66d18b60a3776e183df36444
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708077"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a><span data-ttu-id="6284a-103">ID3DXKeyframedAnimationSet:: GetCallbackKey (método)</span><span class="sxs-lookup"><span data-stu-id="6284a-103">ID3DXKeyframedAnimationSet::GetCallbackKey method</span></span>

<span data-ttu-id="6284a-104">Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="6284a-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6284a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6284a-105">Syntax</span></span>


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="6284a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6284a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6284a-107">*Animación* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6284a-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6284a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6284a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6284a-109">Índice de animación.</span><span class="sxs-lookup"><span data-stu-id="6284a-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="6284a-110">*pCallbackKeys* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6284a-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6284a-111">Tipo: **[ **\_ devolución de llamada LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="6284a-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="6284a-112">Puntero a la [**función de devolución de llamada**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="6284a-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6284a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6284a-113">Return value</span></span>

<span data-ttu-id="6284a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6284a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6284a-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6284a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6284a-116">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6284a-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6284a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6284a-117">Requirements</span></span>



| <span data-ttu-id="6284a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6284a-118">Requirement</span></span> | <span data-ttu-id="6284a-119">Value</span><span class="sxs-lookup"><span data-stu-id="6284a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6284a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6284a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6284a-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6284a-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6284a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6284a-122">Library</span></span><br/> | <dl> <span data-ttu-id="6284a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6284a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6284a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6284a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6284a-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="6284a-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
