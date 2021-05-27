---
title: Estructura XMUINT4
description: Describe un vector entero 4D sin signo.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- HLSL de la estructura XMUINT4
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e424b4e5fd1c97f5aec01571d887b54dbb143b7
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549900"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="14c5c-104">Estructura XMUINT4</span><span class="sxs-lookup"><span data-stu-id="14c5c-104">XMUINT4 structure</span></span>

<span data-ttu-id="14c5c-105">Describe un vector entero 4D sin signo.</span><span class="sxs-lookup"><span data-stu-id="14c5c-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c5c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14c5c-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="14c5c-107">Members</span><span class="sxs-lookup"><span data-stu-id="14c5c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="14c5c-108">**x**</span><span class="sxs-lookup"><span data-stu-id="14c5c-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="14c5c-109">Componente x del vector.</span><span class="sxs-lookup"><span data-stu-id="14c5c-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="14c5c-110">**y**</span><span class="sxs-lookup"><span data-stu-id="14c5c-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="14c5c-111">Componente y del vector.</span><span class="sxs-lookup"><span data-stu-id="14c5c-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="14c5c-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="14c5c-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="14c5c-113">Componente z del vector.</span><span class="sxs-lookup"><span data-stu-id="14c5c-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="14c5c-114">**w**</span><span class="sxs-lookup"><span data-stu-id="14c5c-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="14c5c-115">w-component del vector.</span><span class="sxs-lookup"><span data-stu-id="14c5c-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="14c5c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14c5c-116">Remarks</span></span>

<span data-ttu-id="14c5c-117">Esta estructura se define en el encabezado del ``D3DX\_DXGIFormatConvert.inl`` SDK de DirectX (junio de 2010) para su uso desde C++.</span><span class="sxs-lookup"><span data-stu-id="14c5c-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="14c5c-118">La versión más reciente de este encabezado en el paquete NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) ya no lo define y se basa en [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) en DirectXMath en su lugar.</span><span class="sxs-lookup"><span data-stu-id="14c5c-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="14c5c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14c5c-119">Requirements</span></span>



| <span data-ttu-id="14c5c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c5c-120">Requirement</span></span> | <span data-ttu-id="14c5c-121">Value</span><span class="sxs-lookup"><span data-stu-id="14c5c-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c5c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14c5c-122">Header</span></span><br/> | <dl> <span data-ttu-id="14c5c-123"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="14c5c-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c5c-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="14c5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c5c-125">Estructuras</span><span class="sxs-lookup"><span data-stu-id="14c5c-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="14c5c-126">Desempaquetar y empaquetar DXGI \_ FORMAT para In-Place de imágenes</span><span class="sxs-lookup"><span data-stu-id="14c5c-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>