---
title: CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar que se usa para describir un PSO almacenado en memoria caché como un solo objeto adecuado para una descripción de flujo.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Estructura de CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698199"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a><span data-ttu-id="bbf40-104">\_Secuencia de estado de canalización CD3DX12 \_ \_ \_ en caché del \_ PSO</span><span class="sxs-lookup"><span data-stu-id="bbf40-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO structure</span></span>

<span data-ttu-id="bbf40-105">Una estructura de aplicación auxiliar que se usa para describir un PSO almacenado en memoria caché como un solo objeto adecuado para una descripción de flujo.</span><span class="sxs-lookup"><span data-stu-id="bbf40-105">A helper structure used to describe a cached PSO as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf40-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbf40-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a><span data-ttu-id="bbf40-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bbf40-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bbf40-108">**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ en caché \_ PSO**</span><span class="sxs-lookup"><span data-stu-id="bbf40-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>
</dt> <dd>

<span data-ttu-id="bbf40-109">Crea una nueva instancia no inicializada de un flujo de estado de la \_ canalización CD3DX12 \_ \_ \_ en caché \_ .</span><span class="sxs-lookup"><span data-stu-id="bbf40-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO.</span></span>

</dd> <dt>

<span data-ttu-id="bbf40-110">**\_Flujo de estado de canalización de CD3DX12 \_ \_ \_ en caché \_ PSO (D3D12 \_ Estado de canalización en caché \_ \_ const &i)**</span><span class="sxs-lookup"><span data-stu-id="bbf40-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO(D3D12\_CACHED\_PIPELINE\_STATE const &i)**</span></span>
</dt> <dd>

<span data-ttu-id="bbf40-111">Crea una nueva instancia de un flujo de estado de la \_ canalización de CD3DX12 \_ \_ \_ en caché \_ PSO, inicializado con un tipo de subobjeto de **tipo de \_ subobjeto de estado de canalización D3D12 \_ \_ \_ \_ en memoria caché del \_ PSO** y los datos de subobjeto copiados de *i*, una estructura de [**\_ Estado de \_ canalización \_ de D3D12 almacenada en caché**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="bbf40-111">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO, initialized with a subobject type of **D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE\_CACHED\_PSO** and subobject data copied from *i*, a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bbf40-112">**operador = ( \_ Estado de canalización D3D12 en caché \_ \_ const& i)**</span><span class="sxs-lookup"><span data-stu-id="bbf40-112">**operator=(D3D12\_CACHED\_PIPELINE\_STATE const& i)**</span></span>
</dt> <dd>

<span data-ttu-id="bbf40-113">Operador de asignación de copia.</span><span class="sxs-lookup"><span data-stu-id="bbf40-113">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="bbf40-114">**operador D3D12 de \_ \_ canalización en caché \_ () Const**</span><span class="sxs-lookup"><span data-stu-id="bbf40-114">**operator D3D12\_CACHED\_PIPELINE\_STATE() const**</span></span>
</dt> <dd>

<span data-ttu-id="bbf40-115">Conversión implícita a una estructura de estado de la [**\_ \_ canalización \_ de D3D12 en caché**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .</span><span class="sxs-lookup"><span data-stu-id="bbf40-115">Implicit conversion to a [**D3D12\_CACHED\_PIPELINE\_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbf40-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbf40-116">Remarks</span></span>

<span data-ttu-id="bbf40-117">\_ \_ \_ El flujo de estado \_ de canalización de CD3DX12 en caché \_ PSO es una especialización de TypeDef de la plantilla de [**\_ \_ \_ \_ subobjeto de flujo de estado de canalización CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) y se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="bbf40-117">CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO is a typedef specialization of the [**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) template, and is defined as follows:</span></span>


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
```



## <a name="requirements"></a><span data-ttu-id="bbf40-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbf40-118">Requirements</span></span>



| <span data-ttu-id="bbf40-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbf40-119">Requirement</span></span> | <span data-ttu-id="bbf40-120">Value</span><span class="sxs-lookup"><span data-stu-id="bbf40-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf40-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbf40-121">Header</span></span><br/> | <dl> <span data-ttu-id="bbf40-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbf40-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf40-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbf40-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbf40-124">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="bbf40-124">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="bbf40-125">**Subobjeto de \_ flujo de estado de canalización CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bbf40-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[<span data-ttu-id="bbf40-126">**\_Tipo de \_ subobjeto de estado de CANALización D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bbf40-126">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

