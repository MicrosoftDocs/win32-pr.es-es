---
title: Método ID3DX11EffectVariable GetMemberByIndex (D3dx11effect. h)
description: Obtiene un miembro de estructura por índice.
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- Método GetMemberByIndex Direct3D 11
- Método GetMemberByIndex Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método GetMemberByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4be490251a83907dcd16231d62d492caf05768f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998491"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a><span data-ttu-id="cc295-106">ID3DX11EffectVariable:: GetMemberByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="cc295-106">ID3DX11EffectVariable::GetMemberByIndex method</span></span>

<span data-ttu-id="cc295-107">Obtiene un miembro de estructura por índice.</span><span class="sxs-lookup"><span data-stu-id="cc295-107">Get a structure member by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc295-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc295-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="cc295-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc295-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc295-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="cc295-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="cc295-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc295-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc295-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="cc295-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc295-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc295-113">Return value</span></span>

<span data-ttu-id="cc295-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc295-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="cc295-115">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="cc295-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc295-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc295-116">Remarks</span></span>

<span data-ttu-id="cc295-117">Si la variable de efecto es una estructura, use este método para buscar un miembro por índice.</span><span class="sxs-lookup"><span data-stu-id="cc295-117">If the effect variable is an structure, use this method to look up a member by index.</span></span>

> [!Note]  
> <span data-ttu-id="cc295-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="cc295-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cc295-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="cc295-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cc295-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cc295-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc295-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc295-121">Requirements</span></span>



| <span data-ttu-id="cc295-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc295-122">Requirement</span></span> | <span data-ttu-id="cc295-123">Value</span><span class="sxs-lookup"><span data-stu-id="cc295-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc295-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc295-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cc295-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc295-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cc295-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc295-126">Library</span></span><br/> | <dl> <span data-ttu-id="cc295-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="cc295-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc295-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc295-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc295-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="cc295-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

