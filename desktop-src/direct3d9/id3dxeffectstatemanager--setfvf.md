---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer un código FVF.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'ID3DXEffectStateManager:: SetFVF (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698304"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a><span data-ttu-id="24e1a-103">ID3DXEffectStateManager:: SetFVF (método)</span><span class="sxs-lookup"><span data-stu-id="24e1a-103">ID3DXEffectStateManager::SetFVF method</span></span>

<span data-ttu-id="24e1a-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer un código FVF.</span><span class="sxs-lookup"><span data-stu-id="24e1a-104">A callback function that must be implemented by a user to set a FVF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24e1a-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="24e1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24e1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24e1a-107">*FVF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24e1a-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24e1a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24e1a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24e1a-109">La constante FVF, que determina cómo interpretar los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="24e1a-109">The FVF constant, that determines how to interpret vertex data.</span></span> <span data-ttu-id="24e1a-110">Vea [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="24e1a-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24e1a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24e1a-111">Return value</span></span>

<span data-ttu-id="24e1a-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24e1a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24e1a-113">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="24e1a-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="24e1a-114">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="24e1a-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="24e1a-115">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="24e1a-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="24e1a-116">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)).</span><span class="sxs-lookup"><span data-stu-id="24e1a-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="24e1a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24e1a-117">Requirements</span></span>



| <span data-ttu-id="24e1a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24e1a-118">Requirement</span></span> | <span data-ttu-id="24e1a-119">Value</span><span class="sxs-lookup"><span data-stu-id="24e1a-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="24e1a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24e1a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="24e1a-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e1a-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="24e1a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24e1a-122">Library</span></span><br/> | <dl> <span data-ttu-id="24e1a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24e1a-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="24e1a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="24e1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e1a-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="24e1a-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
