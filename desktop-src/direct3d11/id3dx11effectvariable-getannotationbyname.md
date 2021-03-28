---
title: Método ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
description: Obtiene una anotación por nombre. | Método ID3DX11EffectVariable GetAnnotationByName (D3dx11effect. h)
ms.assetid: 0ca3df07-c721-48c4-9422-f6af24acbaef
keywords:
- Método GetAnnotationByName Direct3D 11
- Método GetAnnotationByName Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37efcd773728e563a4112f61a7c6c965d05bad4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362623"
---
# <a name="id3dx11effectvariablegetannotationbyname-method"></a><span data-ttu-id="15d02-107">ID3DX11EffectVariable:: GetAnnotationByName (método)</span><span class="sxs-lookup"><span data-stu-id="15d02-107">ID3DX11EffectVariable::GetAnnotationByName method</span></span>

<span data-ttu-id="15d02-108">Obtiene una anotación por nombre.</span><span class="sxs-lookup"><span data-stu-id="15d02-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d02-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15d02-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="15d02-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15d02-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15d02-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="15d02-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="15d02-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="15d02-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="15d02-113">Nombre de la anotación.</span><span class="sxs-lookup"><span data-stu-id="15d02-113">The annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15d02-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15d02-114">Return value</span></span>

<span data-ttu-id="15d02-115">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="15d02-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="15d02-116">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="15d02-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="15d02-117">Tenga en cuenta que si no se encuentra la anotación, el **ID3DX11EffectVariable** devuelto estará vacío.</span><span class="sxs-lookup"><span data-stu-id="15d02-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="15d02-118">Se debe llamar al método [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) para determinar si se encontró la anotación.</span><span class="sxs-lookup"><span data-stu-id="15d02-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="15d02-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15d02-119">Remarks</span></span>

<span data-ttu-id="15d02-120">Annonations se puede adjuntar a una técnica, un paso o una variable global.</span><span class="sxs-lookup"><span data-stu-id="15d02-120">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="15d02-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="15d02-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="15d02-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="15d02-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="15d02-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="15d02-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15d02-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15d02-124">Requirements</span></span>



| <span data-ttu-id="15d02-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d02-125">Requirement</span></span> | <span data-ttu-id="15d02-126">Value</span><span class="sxs-lookup"><span data-stu-id="15d02-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d02-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15d02-127">Header</span></span><br/>  | <dl> <span data-ttu-id="15d02-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="15d02-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="15d02-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15d02-129">Library</span></span><br/> | <dl> <span data-ttu-id="15d02-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="15d02-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15d02-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="15d02-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d02-132">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="15d02-132">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

