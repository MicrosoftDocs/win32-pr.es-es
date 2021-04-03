---
title: función gluEndTrim (GLU. h)
description: Las funciones gluBeginTrim y gluEndTrim delimitan una definición de bucle de recorte B-spline racional (NURBS) no uniforme. | función gluEndTrim (GLU. h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- gluEndTrim (función) OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4105cc911105f0444ba17c6b57a3deb048bc96d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083644"
---
# <a name="gluendtrim-function"></a><span data-ttu-id="b426c-105">gluEndTrim función)</span><span class="sxs-lookup"><span data-stu-id="b426c-105">gluEndTrim function</span></span>

<span data-ttu-id="b426c-106">Las funciones [**gluBeginTrim**](glubegintrim.md) y **gluEndTrim** delimitan una definición de bucle de recorte B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.</span><span class="sxs-lookup"><span data-stu-id="b426c-106">The [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming loop definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b426c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b426c-107">Syntax</span></span>


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="b426c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b426c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b426c-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="b426c-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="b426c-110">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="b426c-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b426c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b426c-111">Return value</span></span>

<span data-ttu-id="b426c-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b426c-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b426c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b426c-113">Remarks</span></span>

<span data-ttu-id="b426c-114">Use [**gluBeginTrim**](glubegintrim.md) para marcar el principio de un bucle de recorte y **gluEndTrim** para marcar el final de un bucle de recorte.</span><span class="sxs-lookup"><span data-stu-id="b426c-114">Use [**gluBeginTrim**](glubegintrim.md) to mark the beginning of a trimming loop, and **gluEndTrim** to mark the end of a trimming loop.</span></span> <span data-ttu-id="b426c-115">Un bucle de recorte es un conjunto de segmentos de curva orientado (formando una curva cerrada) que define los límites de una superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="b426c-115">A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface.</span></span> <span data-ttu-id="b426c-116">Estos bucles de recorte se incluyen en la definición de una superficie NURBS, entre las llamadas a [**gluBeginSurface**](glubeginsurface.md) y [**gluEndSurface**](gluendsurface.md).</span><span class="sxs-lookup"><span data-stu-id="b426c-116">You include these trimming loops in the definition of a NURBS surface, between calls to [**gluBeginSurface**](glubeginsurface.md) and [**gluEndSurface**](gluendsurface.md).</span></span>

<span data-ttu-id="b426c-117">La definición de una superficie NURBS puede contener muchos bucles de recorte.</span><span class="sxs-lookup"><span data-stu-id="b426c-117">The definition for a NURBS surface can contain many trimming loops.</span></span> <span data-ttu-id="b426c-118">Por ejemplo, si escribe una definición para una superficie NURBS similar a un rectángulo con un orificio perforado, la definición contendría dos bucles de recorte.</span><span class="sxs-lookup"><span data-stu-id="b426c-118">For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops.</span></span> <span data-ttu-id="b426c-119">Un bucle definiría el borde exterior del rectángulo; la otra definiría el orificio perforado.</span><span class="sxs-lookup"><span data-stu-id="b426c-119">One loop would define the outer edge of the rectangle; the other would define the punched-out hole.</span></span> <span data-ttu-id="b426c-120">Las definiciones de cada uno de estos bucles de recorte estarán entre corchetes por un par de gluEndTrim de [**gluBeginTrim**](glubegintrim.md)  /   .</span><span class="sxs-lookup"><span data-stu-id="b426c-120">The definitions of each of these trimming loops would be bracketed by a [**gluBeginTrim**](glubegintrim.md) / **gluEndTrim** pair.</span></span>

<span data-ttu-id="b426c-121">La definición de un solo bucle de recorte cerrado puede estar formada por varios segmentos de curva, cada uno de los cuales se describe como una serie de segmentos de línea que forman una curva lineal (vea [**gluPwlCurve**](glupwlcurve.md)), como una sola curva de NURBS (vea [**gluNurbsCurve**](glunurbscurve.md)) o como una combinación de ambos en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="b426c-121">The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see [**gluPwlCurve**](glupwlcurve.md)), as a single NURBS curve (see [**gluNurbsCurve**](glunurbscurve.md)), or as a combination of both in any order.</span></span> <span data-ttu-id="b426c-122">Las únicas llamadas de biblioteca que pueden aparecer en una definición de bucle de recorte (entre las llamadas a [**gluBeginTrim**](glubegintrim.md) y **GluEndTrim**) son **gluPwlCurve** y **gluNurbsCurve**.</span><span class="sxs-lookup"><span data-stu-id="b426c-122">The only library calls that can appear in a trimming-loop definition (between the calls to [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim**) are **gluPwlCurve** and **gluNurbsCurve**.</span></span>

<span data-ttu-id="b426c-123">El área mostrada de la superficie de NURBS es la región del dominio a la izquierda de la curva de recorte a medida que aumenta el parámetro de curva.</span><span class="sxs-lookup"><span data-stu-id="b426c-123">The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases.</span></span> <span data-ttu-id="b426c-124">Por lo tanto, la región retenida de la superficie de NURBS está dentro de un bucle de recorte en sentido contrario a las agujas del reloj y fuera de un bucle de recorte.</span><span class="sxs-lookup"><span data-stu-id="b426c-124">Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop.</span></span> <span data-ttu-id="b426c-125">En el caso del rectángulo mencionado anteriormente, el bucle de recorte del borde exterior del rectángulo se ejecuta en sentido contrario a las agujas del reloj, mientras que el bucle de recorte del orificio perforado se ejecuta en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="b426c-125">For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.</span></span>

<span data-ttu-id="b426c-126">Si usa más de una curva para definir un bucle de recorte único, los segmentos de curva deben formar un bucle cerrado (es decir, el extremo de cada curva debe ser el punto inicial de la curva siguiente y el extremo de la curva final debe ser el punto inicial de la primera curva).</span><span class="sxs-lookup"><span data-stu-id="b426c-126">If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve).</span></span> <span data-ttu-id="b426c-127">Si los puntos de conexión de la curva están suficientemente cercanos, pero no exactamente el coincidente, se verán obligados a coincidir.</span><span class="sxs-lookup"><span data-stu-id="b426c-127">If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match.</span></span> <span data-ttu-id="b426c-128">Si los puntos de conexión no están suficientemente cerca, se producirá un error (vea [*gluNurbsCallback*](glunurbs.md)).</span><span class="sxs-lookup"><span data-stu-id="b426c-128">If the endpoints are not sufficiently close, an error results (see [*gluNurbsCallback*](glunurbs.md)).</span></span>

<span data-ttu-id="b426c-129">Si una definición de bucle de recorte contiene varias curvas, la dirección de las curvas debe ser coherente (es decir, el interior debe estar a la izquierda de todas las curvas).</span><span class="sxs-lookup"><span data-stu-id="b426c-129">If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves).</span></span> <span data-ttu-id="b426c-130">Puede utilizar bucles de recorte anidados siempre que las orientaciones de curva alternen correctamente.</span><span class="sxs-lookup"><span data-stu-id="b426c-130">You can use nested trimming loops as long as the curve orientations alternate correctly.</span></span> <span data-ttu-id="b426c-131">Las curvas de recorte no pueden intersectarse por sí mismas ni pueden intersectar entre sí (o un resultado de error).</span><span class="sxs-lookup"><span data-stu-id="b426c-131">Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).</span></span>

<span data-ttu-id="b426c-132">Si no se proporciona información de recorte para una superficie NURBS, se dibuja toda la superficie.</span><span class="sxs-lookup"><span data-stu-id="b426c-132">If no trimming information is given for a NURBS surface, the entire surface is drawn.</span></span>

## <a name="examples"></a><span data-ttu-id="b426c-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b426c-133">Examples</span></span>

<span data-ttu-id="b426c-134">Este fragmento de código define un bucle de recorte que consta de una curva lineal a trozos y dos curvas NURBS:</span><span class="sxs-lookup"><span data-stu-id="b426c-134">This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:</span></span>

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a><span data-ttu-id="b426c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b426c-135">Requirements</span></span>



| <span data-ttu-id="b426c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b426c-136">Requirement</span></span> | <span data-ttu-id="b426c-137">Value</span><span class="sxs-lookup"><span data-stu-id="b426c-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b426c-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b426c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b426c-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b426c-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b426c-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b426c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b426c-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b426c-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b426c-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b426c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b426c-143"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="b426c-143"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b426c-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b426c-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="b426c-145"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b426c-145"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b426c-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b426c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b426c-147"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b426c-147"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b426c-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="b426c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b426c-149">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="b426c-149">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="b426c-150">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="b426c-150">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="b426c-151">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="b426c-151">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="b426c-152">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="b426c-152">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="b426c-153">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="b426c-153">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="b426c-154">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="b426c-154">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





