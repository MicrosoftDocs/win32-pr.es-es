---
description: Recupera el dispositivo asociado a la malla.
ms.assetid: 16ff5267-0c64-4c3d-925d-6fc10f54c9c4
title: 'ID3DXBaseMesh:: GetDevice (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b866c86bf759305a4626f0ff5ecaa8e35bfd75d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083750"
---
# <a name="id3dxbasemeshgetdevice-method"></a><span data-ttu-id="e2457-103">ID3DXBaseMesh:: GetDevice (método)</span><span class="sxs-lookup"><span data-stu-id="e2457-103">ID3DXBaseMesh::GetDevice method</span></span>

<span data-ttu-id="e2457-104">Recupera el dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="e2457-104">Retrieves the device associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2457-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2457-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="e2457-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2457-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2457-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e2457-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e2457-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="e2457-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="e2457-109">Dirección de un puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo Direct3D asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="e2457-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2457-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2457-110">Return value</span></span>

<span data-ttu-id="e2457-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2457-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2457-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2457-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e2457-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e2457-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2457-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2457-114">Remarks</span></span>

<span data-ttu-id="e2457-115">Al llamar a este método, se aumentará el recuento de referencias interno en la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="e2457-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="e2457-116">Asegúrese de llamar a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) cuando haya terminado de usar esta interfaz **IDirect3DDevice9** o se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="e2457-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2457-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2457-117">Requirements</span></span>



| <span data-ttu-id="e2457-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2457-118">Requirement</span></span> | <span data-ttu-id="e2457-119">Value</span><span class="sxs-lookup"><span data-stu-id="e2457-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2457-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2457-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e2457-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2457-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e2457-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2457-122">Library</span></span><br/> | <dl> <span data-ttu-id="e2457-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2457-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2457-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2457-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2457-125">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="e2457-125">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
