---
description: Compara dos instancias de tipos de datos numéricos, o dos instancias de un objeto que admite una sobrecarga de <, y devuelve el mayor de las dos instancias. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Plantilla XMMax (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f8de32a32004289249cea269400d711831d640
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708935"
---
# <a name="xmmax-template"></a><span data-ttu-id="ca703-104">Plantilla XMMax</span><span class="sxs-lookup"><span data-stu-id="ca703-104">XMMax template</span></span>

<span data-ttu-id="ca703-105">Compara dos instancias de tipos de datos numéricos, o dos instancias de un objeto que admite una sobrecarga de <, y devuelve el mayor de las dos instancias.</span><span class="sxs-lookup"><span data-stu-id="ca703-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the larger one of the two instances.</span></span> <span data-ttu-id="ca703-106">El tipo de datos de los argumentos y el valor devuelto es el mismo.</span><span class="sxs-lookup"><span data-stu-id="ca703-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca703-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca703-107">Syntax</span></span>

``` syntax
template<class T> T XMMax(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="ca703-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca703-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca703-109"><span id="a"></span><span id="A"></span>*un*</span><span class="sxs-lookup"><span data-stu-id="ca703-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="ca703-110">\[en \] especifica el primero de dos objetos.</span><span class="sxs-lookup"><span data-stu-id="ca703-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="ca703-111"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="ca703-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="ca703-112">\[en \] especifica dos de los dos objetos.</span><span class="sxs-lookup"><span data-stu-id="ca703-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca703-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca703-113">Return Value</span></span>

<span data-ttu-id="ca703-114">Devuelve el mayor de los dos objetos de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca703-114">Returns the larger of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca703-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca703-115">Remarks</span></span>

<span data-ttu-id="ca703-116">`XMMax` es una plantilla y el tipo T se especifica cuando se crea una instancia de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="ca703-116">`XMMax` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="ca703-117">La `XMMax` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="ca703-117">The `XMMax` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="ca703-118">`XMMax` está disponible como una macro en XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="ca703-118">`XMMax` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="ca703-119">Idealmente, se usa STD:: Max en lugar de `XMMax` .</span><span class="sxs-lookup"><span data-stu-id="ca703-119">Ideally use std::max instead of `XMMax`.</span></span> <span data-ttu-id="ca703-120">Para evitar conflictos con los encabezados de Windows con STD:: Max, debe \# definir NOMINMAX antes de incluir los encabezados de Windows.</span><span class="sxs-lookup"><span data-stu-id="ca703-120">To avoid conflicts with Windows headers with std::max, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="ca703-121">**Espacio de nombres**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="ca703-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ca703-122">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="ca703-122">Platform Requirements</span></span>

<span data-ttu-id="ca703-123">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ca703-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="ca703-124">Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ca703-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca703-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca703-125">Requirements</span></span>



| <span data-ttu-id="ca703-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca703-126">Requirement</span></span> | <span data-ttu-id="ca703-127">Value</span><span class="sxs-lookup"><span data-stu-id="ca703-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca703-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca703-128">Header</span></span><br/> | <dl> <span data-ttu-id="ca703-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca703-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca703-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca703-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca703-131">Funciones de plantilla de la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="ca703-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="ca703-132">**XMMin**</span><span class="sxs-lookup"><span data-stu-id="ca703-132">**XMMin**</span></span>](xmmin-template.md)
</dt> </dl>

 

 




