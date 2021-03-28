---
title: Método ID3DX11EffectConstantBuffer GetConstantBuffer (D3dx11effect. h)
description: Obtiene un búfer de constantes.
ms.assetid: 857b3dc2-41ae-4a52-904a-9ca8f0afeb9e
keywords:
- Método GetConstantBuffer Direct3D 11
- Método GetConstantBuffer Direct3D 11, interfaz ID3DX11EffectConstantBuffer
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11, método GetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041ca2fea028cb86d0959313bae73c320e6e5a36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083811"
---
# <a name="id3dx11effectconstantbuffergetconstantbuffer-method"></a><span data-ttu-id="5c5f9-106">ID3DX11EffectConstantBuffer:: GetConstantBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="5c5f9-106">ID3DX11EffectConstantBuffer::GetConstantBuffer method</span></span>

<span data-ttu-id="5c5f9-107">Obtiene un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="5c5f9-107">Get a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5f9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c5f9-108">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
   ID3D11Buffer **ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="5c5f9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c5f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c5f9-110">*ppConstantBuffer*</span><span class="sxs-lookup"><span data-stu-id="5c5f9-110">*ppConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="5c5f9-111">Tipo: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="5c5f9-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span></span>

<span data-ttu-id="5c5f9-112">Dirección de un puntero a una interfaz de búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="5c5f9-112">The address of a pointer to a constant-buffer interface.</span></span> <span data-ttu-id="5c5f9-113">Vea [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span><span class="sxs-lookup"><span data-stu-id="5c5f9-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c5f9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c5f9-114">Return value</span></span>

<span data-ttu-id="5c5f9-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c5f9-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c5f9-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f9-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c5f9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c5f9-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5c5f9-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="5c5f9-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5c5f9-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5c5f9-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5c5f9-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5c5f9-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c5f9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c5f9-121">Requirements</span></span>



| <span data-ttu-id="5c5f9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c5f9-122">Requirement</span></span> | <span data-ttu-id="5c5f9-123">Value</span><span class="sxs-lookup"><span data-stu-id="5c5f9-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5f9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c5f9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5c5f9-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c5f9-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5c5f9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c5f9-126">Library</span></span><br/> | <dl> <span data-ttu-id="5c5f9-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="5c5f9-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c5f9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c5f9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5f9-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="5c5f9-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





