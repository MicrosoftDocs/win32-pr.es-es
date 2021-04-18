---
title: Método ID3DX12PipelineParserCallbacks SampleMaskCb (D3DX12. h)
description: Llama a la devoluciones de llamada de subobjeto de la máscara de ejemplo de un objeto que implementa esta interfaz.
ms.assetid: 4D729414-1E04-407B-B32F-ECE1EA9FF414
keywords:
- Método SampleMaskCb
- Método SampleMaskCb, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método SampleMaskCb
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.SampleMaskCb
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0124b228056089e21c078ffce25ce59eef0e3dee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717577"
---
# <a name="id3dx12pipelineparsercallbackssamplemaskcb-method"></a><span data-ttu-id="06c0d-106">ID3DX12PipelineParserCallbacks:: SampleMaskCb (método)</span><span class="sxs-lookup"><span data-stu-id="06c0d-106">ID3DX12PipelineParserCallbacks::SampleMaskCb method</span></span>

<span data-ttu-id="06c0d-107">Llama a la devoluciones de llamada de subobjeto de la máscara de ejemplo de un objeto que implementa esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="06c0d-107">Calls the sample mask subobject callback of an object that implements this interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c0d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06c0d-108">Syntax</span></span>


```C++
void SampleMaskCb(
   
        UINT
           SampleMask
);
```



## <a name="parameters"></a><span data-ttu-id="06c0d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06c0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c0d-110">*SampleMask*</span><span class="sxs-lookup"><span data-stu-id="06c0d-110">*SampleMask*</span></span> 
</dt> <dd>

<span data-ttu-id="06c0d-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="06c0d-111">Type: **UINT**</span></span>

<span data-ttu-id="06c0d-112">Detalles del subobjeto de máscara de ejemplo analizado desde una secuencia de estado de canalización.</span><span class="sxs-lookup"><span data-stu-id="06c0d-112">Details of the sample mask subobject parsed from a pipeline state stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c0d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06c0d-113">Return value</span></span>

<span data-ttu-id="06c0d-114">No devuelve nada.</span><span class="sxs-lookup"><span data-stu-id="06c0d-114">Returns nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c0d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c0d-115">Requirements</span></span>



| <span data-ttu-id="06c0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c0d-116">Requirement</span></span> | <span data-ttu-id="06c0d-117">Value</span><span class="sxs-lookup"><span data-stu-id="06c0d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="06c0d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06c0d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="06c0d-119"><dt>D3DX12. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c0d-119"><dt>D3DX12.h</dt></span></span> </dl>  |
| <span data-ttu-id="06c0d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06c0d-120">Library</span></span><br/> | <dl> <span data-ttu-id="06c0d-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06c0d-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="06c0d-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06c0d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="06c0d-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c0d-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c0d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="06c0d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c0d-125">Interfaces auxiliares de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="06c0d-125">Helper Interfaces for Direct3D 12</span></span>](helper-interfaces-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="06c0d-126">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="06c0d-126">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





