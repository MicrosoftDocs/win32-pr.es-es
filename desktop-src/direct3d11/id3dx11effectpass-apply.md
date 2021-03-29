---
title: Método ID3DX11EffectPass Apply (D3dx11effect. h)
description: Establezca el estado contenido en un paso en el dispositivo.
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Aplicar el método Direct3D 11
- Aplicar método Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método Apply
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a061609953e164524e16722222a5ecea81f275b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986923"
---
# <a name="id3dx11effectpassapply-method"></a><span data-ttu-id="69d8a-106">ID3DX11EffectPass:: Apply (método)</span><span class="sxs-lookup"><span data-stu-id="69d8a-106">ID3DX11EffectPass::Apply method</span></span>

<span data-ttu-id="69d8a-107">Establezca el estado contenido en un paso en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69d8a-107">Set the state contained in a pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d8a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69d8a-108">Syntax</span></span>


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="69d8a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69d8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d8a-110">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="69d8a-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="69d8a-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="69d8a-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="69d8a-112">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="69d8a-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="69d8a-113">*pContext*</span><span class="sxs-lookup"><span data-stu-id="69d8a-113">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="69d8a-114">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="69d8a-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="69d8a-115">[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) al que se va a aplicar el paso.</span><span class="sxs-lookup"><span data-stu-id="69d8a-115">The [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) to apply the pass to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d8a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69d8a-116">Return value</span></span>

<span data-ttu-id="69d8a-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69d8a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69d8a-118">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="69d8a-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69d8a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69d8a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="69d8a-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="69d8a-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="69d8a-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="69d8a-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="69d8a-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="69d8a-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69d8a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d8a-123">Requirements</span></span>



| <span data-ttu-id="69d8a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d8a-124">Requirement</span></span> | <span data-ttu-id="69d8a-125">Value</span><span class="sxs-lookup"><span data-stu-id="69d8a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d8a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69d8a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="69d8a-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="69d8a-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="69d8a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69d8a-128">Library</span></span><br/> | <dl> <span data-ttu-id="69d8a-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="69d8a-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d8a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="69d8a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d8a-131">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="69d8a-131">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

