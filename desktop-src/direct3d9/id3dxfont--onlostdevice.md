---
description: 'Método ID3DXFont::OnLostDevice: use este método para liberar todas las referencias a recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.'
ms.assetid: 1abc4e01-65c6-4034-8cbb-891a2234ad33
title: Método ID3DXFont::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c484d7867745805e29bda88e2f8d49ca8bc21be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090373"
---
# <a name="id3dxfontonlostdevice-method"></a><span data-ttu-id="7e79c-104">Método ID3DXFont::OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="7e79c-104">ID3DXFont::OnLostDevice method</span></span>

<span data-ttu-id="7e79c-105">Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado.</span><span class="sxs-lookup"><span data-stu-id="7e79c-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="7e79c-106">Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e79c-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e79c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e79c-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="7e79c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e79c-108">Parameters</span></span>

<span data-ttu-id="7e79c-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7e79c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e79c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e79c-110">Return value</span></span>

<span data-ttu-id="7e79c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e79c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e79c-112">Si el método se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e79c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7e79c-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7e79c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e79c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e79c-114">Remarks</span></span>

<span data-ttu-id="7e79c-115">Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="7e79c-115">This method should be called whenever the device is lost or before the user calls [**Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="7e79c-116">Incluso si el dispositivo no se perdió realmente, **OnLostDevice** es responsable de liberar los bloques de estado y otros recursos que es posible que deba liberar antes de restablecer el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e79c-116">Even if the device was not actually lost, **OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="7e79c-117">Como resultado, el objeto de fuente no se puede usar de nuevo antes de llamar a **Reset** y, a continuación, [**OnResetDevice**](id3dxfont--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e79c-117">As a result, the font object cannot be used again before calling **Reset** and then [**OnResetDevice**](id3dxfont--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e79c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e79c-118">Requirements</span></span>



| <span data-ttu-id="7e79c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e79c-119">Requirement</span></span> | <span data-ttu-id="7e79c-120">Value</span><span class="sxs-lookup"><span data-stu-id="7e79c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e79c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e79c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7e79c-122"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="7e79c-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7e79c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e79c-123">Library</span></span><br/> | <dl> <span data-ttu-id="7e79c-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e79c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e79c-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e79c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e79c-126">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="7e79c-126">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




