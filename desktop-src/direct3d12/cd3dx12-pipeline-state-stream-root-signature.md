---
title: CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir la firma raíz como un solo objeto adecuado para una descripción de la secuencia.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a97402fa267693de23ed2085b3d41973dc409e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698408"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a><span data-ttu-id="28c7e-104">\_Estructura de \_ la \_ \_ firma raíz de flujo de estado de canalización CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="28c7e-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE structure</span></span>

<span data-ttu-id="28c7e-105">Una estructura de aplicación auxiliar que se usa para describir la firma raíz como un solo objeto adecuado para una descripción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="28c7e-105">A helper structure used to describe the root signature as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c7e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28c7e-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a><span data-ttu-id="28c7e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="28c7e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="28c7e-108">**\_ \_ \_ \_ Firma raíz de la secuencia de estado de canalización CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="28c7e-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="28c7e-109">Crea una instancia nueva, no inicializada, de una firma raíz de la secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="28c7e-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE.</span></span>

</dd> <dt>

<span data-ttu-id="28c7e-110">**Firma raíz de la secuencia de estado de la \_ canalización CD3DX12 \_ \_ \_ \_ (ID3D12RootSignature \* const &i)**</span><span class="sxs-lookup"><span data-stu-id="28c7e-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE(ID3D12RootSignature\* const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="28c7e-111">Crea una nueva instancia de una \_ firma raíz de flujo de estado de canalización de CD3DX12 \_ \_ \_ \_ , inicializada con un tipo de subobjeto de **tipo de \_ subobjeto de estado de canalización D3D12 \_ \_ \_ \_ \_ firma raíz** y datos de subobjeto copiados de *i*, una estructura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="28c7e-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_ROOT\_SIGNATURE** and subobject data copied from *i*, a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure.</span></span>

</dd> <dt>

<span data-ttu-id="28c7e-112">**Operator = (ID3D12RootSignature \* const& i)**</span><span class="sxs-lookup"><span data-stu-id="28c7e-112">**operator=(ID3D12RootSignature\* const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="28c7e-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="28c7e-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="28c7e-114">**operador ID3D12RootSignature \* () Const**</span><span class="sxs-lookup"><span data-stu-id="28c7e-114">**operator ID3D12RootSignature\*() const**</span></span>
</dt> <dd>

<span data-ttu-id="28c7e-115">Conversión implícita a un puntero de estructura [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .</span><span class="sxs-lookup"><span data-stu-id="28c7e-115">Implicit conversion to a [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) structure pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28c7e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28c7e-116">Remarks</span></span>

<span data-ttu-id="28c7e-117">\_ \_ \_ \_ \_ La firma raíz de la secuencia de estado de canalización de CD3DX12 es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="28c7e-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
```



## <a name="requirements"></a><span data-ttu-id="28c7e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c7e-118">Requirements</span></span>



| <span data-ttu-id="28c7e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c7e-119">Requirement</span></span> | <span data-ttu-id="28c7e-120">Value</span><span class="sxs-lookup"><span data-stu-id="28c7e-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="28c7e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28c7e-121">Header</span></span><br/> | <dl> <span data-ttu-id="28c7e-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c7e-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c7e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="28c7e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c7e-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="28c7e-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="28c7e-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28c7e-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="28c7e-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28c7e-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

