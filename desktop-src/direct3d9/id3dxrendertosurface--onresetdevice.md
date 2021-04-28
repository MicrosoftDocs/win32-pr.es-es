---
description: 'Método ID3DXRenderToSurface::OnResetDevice: use este método para volver a adquirir recursos y guardar el estado inicial.'
ms.assetid: a326a465-ee90-466d-8e46-22e082e9533c
title: Método ID3DXRenderToSurface::OnResetDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17af145a236d2b3a51d271c6687d78d81a387363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107193"
---
# <a name="id3dxrendertosurfaceonresetdevice-method"></a><span data-ttu-id="2979a-103">Método ID3DXRenderToSurface::OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="2979a-103">ID3DXRenderToSurface::OnResetDevice method</span></span>

<span data-ttu-id="2979a-104">Use este método para volver a adquirir recursos y guardar el estado inicial.</span><span class="sxs-lookup"><span data-stu-id="2979a-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="2979a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2979a-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="2979a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2979a-106">Parameters</span></span>

<span data-ttu-id="2979a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2979a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2979a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2979a-108">Return value</span></span>

<span data-ttu-id="2979a-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2979a-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2979a-110">Si el método se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2979a-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2979a-111">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2979a-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2979a-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2979a-112">Remarks</span></span>

<span data-ttu-id="2979a-113">Se debe llamar a ID3DXRenderToSurface::OnResetDevice cada vez que se restablezca el dispositivo (mediante [**IDirect3DDevice9::Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)antes de llamar a cualquier otro método.</span><span class="sxs-lookup"><span data-stu-id="2979a-113">ID3DXRenderToSurface::OnResetDevice should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="2979a-114">Este es un buen lugar para volver a adquirir recursos de memoria de vídeo y capturar bloques de estado.</span><span class="sxs-lookup"><span data-stu-id="2979a-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="2979a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2979a-115">Requirements</span></span>



| <span data-ttu-id="2979a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2979a-116">Requirement</span></span> | <span data-ttu-id="2979a-117">Value</span><span class="sxs-lookup"><span data-stu-id="2979a-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2979a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2979a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2979a-119"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="2979a-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2979a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2979a-120">Library</span></span><br/> | <dl> <span data-ttu-id="2979a-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2979a-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2979a-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2979a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2979a-123">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="2979a-123">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
