---
title: Tipo de estructura
description: Tipo de estructura
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo de struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996820"
---
# <a name="struct-type"></a><span data-ttu-id="263a7-104">Tipo de estructura</span><span class="sxs-lookup"><span data-stu-id="263a7-104">Struct Type</span></span>

<span data-ttu-id="263a7-105">Use la siguiente sintaxis para declarar una estructura mediante HLSL.</span><span class="sxs-lookup"><span data-stu-id="263a7-105">Use the following syntax to declare a structure using HLSL.</span></span>



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="263a7-106">*nombre* de struct { \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *memberName*;     ... };</span><span class="sxs-lookup"><span data-stu-id="263a7-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="263a7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="263a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="263a7-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="263a7-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="263a7-109">Cadena ASCII que identifica de forma única el nombre de la estructura.</span><span class="sxs-lookup"><span data-stu-id="263a7-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="263a7-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span><span class="sxs-lookup"><span data-stu-id="263a7-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="263a7-111">Modificador opcional que especifica un tipo de interpolación.</span><span class="sxs-lookup"><span data-stu-id="263a7-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="263a7-112">Consulte [Comentarios](#remarks) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="263a7-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="263a7-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ de *R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="263a7-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="263a7-114">El tipo de miembro con un tamaño de matriz de columna (*C*) x de fila opcional (*R*).</span><span class="sxs-lookup"><span data-stu-id="263a7-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="263a7-115">Una estructura contiene al menos un elemento; Si contiene más de un elemento, los elementos son del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="263a7-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="263a7-116">El número de filas y columnas son enteros sin signo entre 1 y 4, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="263a7-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="263a7-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*NombreDeMiembro*</span><span class="sxs-lookup"><span data-stu-id="263a7-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="263a7-118">Cadena ASCII que identifica de forma única el nombre del miembro.</span><span class="sxs-lookup"><span data-stu-id="263a7-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="263a7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="263a7-119">Remarks</span></span>

<span data-ttu-id="263a7-120">Se puede especificar un modificador de interpolación en cualquier miembro de estructura o en un argumento para una función de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="263a7-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="263a7-121">Si un modificador aparece en ambos lugares, el modificador exterior (el modificador de argumento del sombreador de píxeles) sobreasignará el modificador in (el modificador de estructura).</span><span class="sxs-lookup"><span data-stu-id="263a7-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="263a7-122">Al compilar un sombreador o un efecto, el compilador del sombreador empaqueta los miembros de la estructura de acuerdo con [las reglas de empaquetado de HLSL](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="263a7-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="263a7-123">Modificadores de interpolación introducidos en el modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="263a7-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="263a7-124">Las salidas del sombreador de vértices que se usan para las entradas del sombreador de píxeles se interpolan linealmente para obtener valores por píxel durante la rasterización.</span><span class="sxs-lookup"><span data-stu-id="263a7-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="263a7-125">Para establecer el método de interpolación, use cualquiera de los siguientes valores, que se admiten en el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) o posterior.</span><span class="sxs-lookup"><span data-stu-id="263a7-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="263a7-126">El modificador se omite en cualquier salida del sombreador de vértices que no se use como entrada de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="263a7-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="263a7-127">Modificador de interpolación</span><span class="sxs-lookup"><span data-stu-id="263a7-127">Interpolation Modifier</span></span> | <span data-ttu-id="263a7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="263a7-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="263a7-129">**lineal**</span><span class="sxs-lookup"><span data-stu-id="263a7-129">**linear**</span></span>             | <span data-ttu-id="263a7-130">Interpolar entre las entradas del sombreador; **lineal** es el valor predeterminado si no se especifica ningún modificador de interpolación.</span><span class="sxs-lookup"><span data-stu-id="263a7-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="263a7-131">**centroide**</span><span class="sxs-lookup"><span data-stu-id="263a7-131">**centroid**</span></span>           | <span data-ttu-id="263a7-132">Interpolar entre las muestras que se encuentran en algún lugar dentro del área tratada del píxel (esto puede requerir la extrapolación de los puntos finales de un centro de píxeles).</span><span class="sxs-lookup"><span data-stu-id="263a7-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="263a7-133">El muestreo de centroide puede mejorar el suavizado de contorno si un píxel está parcialmente incluido (aunque no esté incluido el centro de píxeles).</span><span class="sxs-lookup"><span data-stu-id="263a7-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="263a7-134">El modificador **centroide** debe combinarse con el modificador **linear** o **noperspective** .</span><span class="sxs-lookup"><span data-stu-id="263a7-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="263a7-135">**nointerpolación**</span><span class="sxs-lookup"><span data-stu-id="263a7-135">**nointerpolation**</span></span>    | <span data-ttu-id="263a7-136">No se interpolan.</span><span class="sxs-lookup"><span data-stu-id="263a7-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="263a7-137">**noperspective**</span><span class="sxs-lookup"><span data-stu-id="263a7-137">**noperspective**</span></span>      | <span data-ttu-id="263a7-138">No realice correcciones de perspectiva durante la interpolación.</span><span class="sxs-lookup"><span data-stu-id="263a7-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="263a7-139">El modificador **noperspective** se puede combinar con el modificador **centroide** .</span><span class="sxs-lookup"><span data-stu-id="263a7-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="263a7-140">**AdventureWorks**</span><span class="sxs-lookup"><span data-stu-id="263a7-140">**sample**</span></span>             | <span data-ttu-id="263a7-141">**Disponible en el modelo de sombreador 4,1 y versiones posteriores** Interpolación en la ubicación de ejemplo en lugar de en el centro de píxeles.</span><span class="sxs-lookup"><span data-stu-id="263a7-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="263a7-142">Esto hace que el sombreador de píxeles se ejecute por ejemplo en lugar de por píxel.</span><span class="sxs-lookup"><span data-stu-id="263a7-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="263a7-143">Otra manera de producir la ejecución por muestra es tener una entrada con la [ \_ SampleIndex semántica](dx-graphics-hlsl-semantics.md), que indica el ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="263a7-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="263a7-144">Solo las entradas con el **ejemplo** especificado (o la entrada \_ SampleIndex de SV) difieren entre las invocaciones del sombreador en el píxel, mientras que otras entradas que no especifican modificadores (por ejemplo, si se mezclan modificadores en entradas diferentes) todavía se interpolan en el centro de píxeles.</span><span class="sxs-lookup"><span data-stu-id="263a7-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="263a7-145">Tanto la invocación del sombreador de píxeles como la prueba de profundidad y estarcido se producen para cada muestra incluida en el píxel.</span><span class="sxs-lookup"><span data-stu-id="263a7-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="263a7-146">A veces, esto se conoce como *supermuestreo*.</span><span class="sxs-lookup"><span data-stu-id="263a7-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="263a7-147">Por el contrario, en ausencia de una invocación de frecuencia de muestreo, conocida como *multimuestreo*, el sombreador de píxeles se invoca una vez por píxel, independientemente del número de muestras que se cubran, mientras que las pruebas de profundidad y estarcido se producen con frecuencia de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="263a7-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="263a7-148">Ambos modos proporcionan suavizado de contorno de borde equivalente.</span><span class="sxs-lookup"><span data-stu-id="263a7-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="263a7-149">Sin embargo, el supermuestreo proporciona una mejor calidad de sombreado mediante la invocación del sombreador de píxeles con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="263a7-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="263a7-150">1. Cuando se usa un tipo int/uint, la única opción válida es **nointerpolation**.</span><span class="sxs-lookup"><span data-stu-id="263a7-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="263a7-151">Los modificadores de interpolación se pueden aplicar a los miembros de la estructura o a los argumentos de la [función](dx-graphics-hlsl-function-parameters.md), o a ambos.</span><span class="sxs-lookup"><span data-stu-id="263a7-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="263a7-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="263a7-152">Examples</span></span>

<span data-ttu-id="263a7-153">A continuación se muestran algunas declaraciones de estructura de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="263a7-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="263a7-154">Esta Declaración incluye una matriz.</span><span class="sxs-lookup"><span data-stu-id="263a7-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="263a7-155">Esta Declaración incluye un modificador de interpolación.</span><span class="sxs-lookup"><span data-stu-id="263a7-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="263a7-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="263a7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="263a7-157">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="263a7-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





