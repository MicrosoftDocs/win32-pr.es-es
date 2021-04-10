---
title: función glColor3iv (GL. h)
description: Establece el color actual de una matriz de valores de color ya existente. | función glColor3iv (GL. h)
ms.assetid: b083fd09-fe92-4afa-bcb7-f36e9eeffbab
keywords:
- glColor3iv (función) OpenGL
topic_type:
- apiref
api_name:
- glColor3iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36734d3e6d5f90283c6298705717e79b98f89474
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280144"
---
# <a name="glcolor3iv-function"></a><span data-ttu-id="c6c17-105">glColor3iv función)</span><span class="sxs-lookup"><span data-stu-id="c6c17-105">glColor3iv function</span></span>

<span data-ttu-id="c6c17-106">Establece el color actual de una matriz de valores de color ya existente.</span><span class="sxs-lookup"><span data-stu-id="c6c17-106">Sets the current color from an already existing array of color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c17-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6c17-107">Syntax</span></span>


```C++
void WINAPI glColor3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="c6c17-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6c17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c17-109">*v*</span><span class="sxs-lookup"><span data-stu-id="c6c17-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c17-110">Puntero a una matriz que contiene los valores rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="c6c17-110">A pointer to an array that contains red, green, and blue values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c17-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6c17-111">Return value</span></span>

<span data-ttu-id="c6c17-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c6c17-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c17-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6c17-113">Remarks</span></span>

<span data-ttu-id="c6c17-114">El libro de contabilidad almacena un índice de color de un solo valor actual y un color RGBA de cuatro valores actual.</span><span class="sxs-lookup"><span data-stu-id="c6c17-114">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="c6c17-115">**glcolor** establece un nuevo color RGBA de cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="c6c17-115">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="c6c17-116">**glcolor** tiene dos variantes principales: **glcolor3** y **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="c6c17-116">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="c6c17-117">las variantes de **glcolor3** especifican nuevos valores rojo, verde y azul explícitamente y establecen el valor alfa actual en 1,0 (intensidad total) implícitamente.</span><span class="sxs-lookup"><span data-stu-id="c6c17-117">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="c6c17-118">las variantes de **glcolor4** especifican los cuatro componentes de color explícitamente.</span><span class="sxs-lookup"><span data-stu-id="c6c17-118">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="c6c17-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** y **glcolor4i** toman tres o cuatro enteros con signo, cortos o largos como argumentos.</span><span class="sxs-lookup"><span data-stu-id="c6c17-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="c6c17-120">Cuando se anexa v al nombre, los comandos de color pueden tomar un puntero a una matriz de estos valores.</span><span class="sxs-lookup"><span data-stu-id="c6c17-120">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="c6c17-121">Los valores de color actuales se almacenan en formato de punto flotante, con la mantisa y los tamaños de exponente no especificados.</span><span class="sxs-lookup"><span data-stu-id="c6c17-121">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="c6c17-122">Los componentes de color de entero sin signo, cuando se especifican, se asignan linealmente a valores de punto flotante, de modo que el mayor valor que se puede representar se asigna a 1,0 (intensidad total) y 0 se asigna a 0,0 (intensidad cero).</span><span class="sxs-lookup"><span data-stu-id="c6c17-122">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="c6c17-123">Los componentes de color de entero con signo, cuando se especifican, se asignan linealmente a valores de punto flotante, de modo que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="c6c17-123">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="c6c17-124">(Tenga en cuenta que esta asignación no convierte 0 exactamente a 0,0). Los valores de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="c6c17-124">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="c6c17-125">Ninguno de los valores de punto flotante ni de entero con signo se fijan en el intervalo de \[ 0 a 1 \] antes de que se actualice el color actual.</span><span class="sxs-lookup"><span data-stu-id="c6c17-125">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="c6c17-126">Sin embargo, los componentes de color se fijan en este intervalo antes de que se interpolen o se escriban en un búfer de color.</span><span class="sxs-lookup"><span data-stu-id="c6c17-126">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c17-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6c17-127">Requirements</span></span>



| <span data-ttu-id="c6c17-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c17-128">Requirement</span></span> | <span data-ttu-id="c6c17-129">Value</span><span class="sxs-lookup"><span data-stu-id="c6c17-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c17-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6c17-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c17-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c6c17-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c6c17-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6c17-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c17-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6c17-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6c17-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6c17-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c17-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c17-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c6c17-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6c17-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6c17-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6c17-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6c17-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6c17-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6c17-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6c17-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c17-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6c17-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c17-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c6c17-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c6c17-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c6c17-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c6c17-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="c6c17-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="c6c17-144">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="c6c17-144">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





