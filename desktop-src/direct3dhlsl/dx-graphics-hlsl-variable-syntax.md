---
title: Sintaxis de variables
description: Use las siguientes reglas de sintaxis para declarar variables de HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintaxis de variables (DirectX HLSL)
- nointerpolación, sintaxis de variables (DirectX HLSL)
- Sintaxis de variables compartidas (DirectX HLSL)
- groupshared, sintaxis de variables (DirectX HLSL)
- Sintaxis de variables estáticas (DirectX HLSL)
- Sintaxis de variables uniformes (DirectX HLSL)
- Sintaxis volátil y variable (DirectX HLSL)
- Sintaxis de variables precisa (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/11/2020
ms.locfileid: "104997189"
---
# <a name="variable-syntax"></a><span data-ttu-id="03c8d-111">Sintaxis de variables</span><span class="sxs-lookup"><span data-stu-id="03c8d-111">Variable Syntax</span></span>

<span data-ttu-id="03c8d-112">Use las siguientes reglas de sintaxis para declarar variables de HLSL.</span><span class="sxs-lookup"><span data-stu-id="03c8d-112">Use the following syntax rules to declare HLSL variables.</span></span>



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c8d-113">\[*Almacenamiento \_ de* Type ( \] \[ *\_ modificador de tipo* de clase) \]  \[ *index* \] \[ *: Semantic* \] \[ *: Packoffset* \] \[ *: Register* \] ;    \[  \] Anotaciones \[ *= Inicial \_ Valor* de                    \]</span><span class="sxs-lookup"><span data-stu-id="03c8d-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="03c8d-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03c8d-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03c8d-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Clase de almacenamiento \_*</span><span class="sxs-lookup"><span data-stu-id="03c8d-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="03c8d-116">Modificadores de clase de almacenamiento opcionales que proporcionan sugerencias al compilador sobre el ámbito y la duración de las variables. los modificadores se pueden especificar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="03c8d-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03c8d-117">Value</span><span class="sxs-lookup"><span data-stu-id="03c8d-117">Value</span></span></th>
<th><span data-ttu-id="03c8d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="03c8d-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03c8d-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="03c8d-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="03c8d-120">Marque una variable global como entrada externa al sombreador; Este es el marcado predeterminado para todas las variables globales.</span><span class="sxs-lookup"><span data-stu-id="03c8d-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="03c8d-121">No se puede combinar con <strong>static</strong>.</span><span class="sxs-lookup"><span data-stu-id="03c8d-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03c8d-122"><strong>nointerpolación</strong></span><span class="sxs-lookup"><span data-stu-id="03c8d-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="03c8d-123">No interpole las salidas de un sombreador de vértices antes de pasarlas a un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="03c8d-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03c8d-124"><strong>cifras</strong></span><span class="sxs-lookup"><span data-stu-id="03c8d-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="03c8d-125">La palabra clave <strong>precisa</strong> cuando se aplica a una variable restringirá los cálculos utilizados para generar el valor asignado a esa variable de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="03c8d-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="03c8d-126">Las operaciones independientes se mantienen separadas.</span><span class="sxs-lookup"><span data-stu-id="03c8d-126">Separate operations are kept separate.</span></span> <span data-ttu-id="03c8d-127">Por ejemplo, en los casos en los que una operación Mul y Add se ha fusionado en una operación de Mad, <strong>precisa</strong> obliga a las operaciones a permanecer separadas.</span><span class="sxs-lookup"><span data-stu-id="03c8d-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="03c8d-128">En su lugar, debe utilizar explícitamente la función intrínseca Mad.</span><span class="sxs-lookup"><span data-stu-id="03c8d-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="03c8d-129">Se mantiene el orden de las operaciones.</span><span class="sxs-lookup"><span data-stu-id="03c8d-129">Order of operations are maintained.</span></span> <span data-ttu-id="03c8d-130">Cuando el orden de las instrucciones podría haberse aleatorio para mejorar el rendimiento, es <strong>preciso</strong> asegurarse de que el compilador conserva el orden como escrito.</span><span class="sxs-lookup"><span data-stu-id="03c8d-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="03c8d-131">Las operaciones IEEE no seguras están restringidas.</span><span class="sxs-lookup"><span data-stu-id="03c8d-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="03c8d-132">En los casos en los que el compilador podría haber usado operaciones matemáticas rápidas que no tienen en cuenta los valores NaN (no un número) e INF (infinito <strong>), se</strong> deben respetar los requisitos de IEEE relativos a los valores Nan y INF.</span><span class="sxs-lookup"><span data-stu-id="03c8d-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="03c8d-133">Sin <strong>precisión</strong>, estas optimizaciones y operaciones matemáticas no son seguras para IEEE.</span><span class="sxs-lookup"><span data-stu-id="03c8d-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="03c8d-134">La calificación de una variable <strong>precisa</strong> no hace que las operaciones que usan la variable sean <strong>precisas</strong>.</span><span class="sxs-lookup"><span data-stu-id="03c8d-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="03c8d-135">Dado que <strong>precise</strong> se propaga solo a las operaciones que contribuyen a los valores que se asignan a la variable calificada con <strong>precisión</strong>, el hecho de que los cálculos deseados sean <strong>precisos</strong> puede ser complicado, por lo que se recomienda marcar <strong>las salidas del</strong> sombreador exactamente donde se declaran, ya sea en un campo de estructura o en un parámetro de salida, o en el tipo de valor</span><span class="sxs-lookup"><span data-stu-id="03c8d-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="03c8d-136">La capacidad de controlar las optimizaciones de este modo mantiene la inestabilidad de resultados para la variable de salida modificada al deshabilitar las optimizaciones que pueden afectar a los resultados finales debido a las diferencias en las diferencias de precisión acumuladas.</span><span class="sxs-lookup"><span data-stu-id="03c8d-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="03c8d-137">Resulta útil cuando se desea que los sombreadores de teselación mantengan coincidencias de parches con agua apretada o valores de profundidad de coincidencia en varias fases.</span><span class="sxs-lookup"><span data-stu-id="03c8d-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="03c8d-138">[Código de ejemplo](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span><span class="sxs-lookup"><span data-stu-id="03c8d-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="03c8d-139"><strong>recurso</strong></span><span class="sxs-lookup"><span data-stu-id="03c8d-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="03c8d-140">Marcar una variable para compartir entre efectos; Esta es una sugerencia para el compilador.</span><span class="sxs-lookup"><span data-stu-id="03c8d-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03c8d-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="03c8d-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="03c8d-142">Marque una variable para la memoria compartida por el grupo de subprocesos para los sombreadores de cálculo.</span><span class="sxs-lookup"><span data-stu-id="03c8d-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="03c8d-143">En D3D10, el tamaño total máximo de todas las variables con la clase de almacenamiento groupshared es 16 KB, en D3D11 el tamaño máximo es 32 KB.</span><span class="sxs-lookup"><span data-stu-id="03c8d-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="03c8d-144">Vea los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="03c8d-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03c8d-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="03c8d-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="03c8d-146">Marque una variable local para que se inicialice una vez y se conserve entre las llamadas de función.</span><span class="sxs-lookup"><span data-stu-id="03c8d-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="03c8d-147">Si la declaración no incluye un inicializador, el valor se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="03c8d-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="03c8d-148">Una variable global marcada como <strong>static</strong> no es visible para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="03c8d-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03c8d-149"><strong>uniforme</strong></span><span class="sxs-lookup"><span data-stu-id="03c8d-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="03c8d-150">Marque una variable cuyos datos sean constantes a lo largo de la ejecución de un sombreador (por ejemplo, un color material en un sombreador de vértices). de forma predeterminada, las variables globales se consideran <strong>uniformes</strong> .</span><span class="sxs-lookup"><span data-stu-id="03c8d-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03c8d-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="03c8d-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="03c8d-152">Marque una variable que cambie con frecuencia; Esta es una sugerencia para el compilador.</span><span class="sxs-lookup"><span data-stu-id="03c8d-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="03c8d-153">Este modificador de clase de almacenamiento solo se aplica a una variable local.</span><span class="sxs-lookup"><span data-stu-id="03c8d-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="03c8d-154">El compilador de HLSL actualmente omite este modificador de clase de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="03c8d-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="03c8d-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Modificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="03c8d-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-156">Modificador de tipo variable opcional.</span><span class="sxs-lookup"><span data-stu-id="03c8d-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="03c8d-157">Value</span><span class="sxs-lookup"><span data-stu-id="03c8d-157">Value</span></span>             | <span data-ttu-id="03c8d-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="03c8d-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c8d-159">**const**</span><span class="sxs-lookup"><span data-stu-id="03c8d-159">**const**</span></span>         | <span data-ttu-id="03c8d-160">Marque una variable que un sombreador no pueda cambiar; por lo tanto, debe inicializarse en la declaración de la variable.</span><span class="sxs-lookup"><span data-stu-id="03c8d-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="03c8d-161">Las variables globales se consideran **const** de forma predeterminada (suprima este comportamiento mediante la especificación de la marca/GEC en el compilador).</span><span class="sxs-lookup"><span data-stu-id="03c8d-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="03c8d-162">**fila \_ principal**</span><span class="sxs-lookup"><span data-stu-id="03c8d-162">**row\_major**</span></span>    | <span data-ttu-id="03c8d-163">Marque una variable que almacene cuatro componentes en una sola fila para que puedan almacenarse en un solo registro de constante.</span><span class="sxs-lookup"><span data-stu-id="03c8d-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="03c8d-164">**columna \_ principal**</span><span class="sxs-lookup"><span data-stu-id="03c8d-164">**column\_major**</span></span> | <span data-ttu-id="03c8d-165">Marque una variable que almacene 4 componentes en una sola columna para optimizar la aritmética de la matriz.</span><span class="sxs-lookup"><span data-stu-id="03c8d-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="03c8d-166">Si no se especifica un valor de modificador de tipo, el compilador utiliza la **columna \_ major** como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="03c8d-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="03c8d-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Automáticamente*</span><span class="sxs-lookup"><span data-stu-id="03c8d-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-168">Cualquier tipo HLSL mostrado en [tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="03c8d-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="03c8d-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nombre* \[ de *Índice* de\]</span><span class="sxs-lookup"><span data-stu-id="03c8d-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-170">Cadena ASCII que identifica de forma única una variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="03c8d-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="03c8d-171">Para definir una matriz opcional, utilice **index** para el tamaño de la matriz, que es un entero positivo = 1.</span><span class="sxs-lookup"><span data-stu-id="03c8d-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="03c8d-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semántica*</span><span class="sxs-lookup"><span data-stu-id="03c8d-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-173">Información de uso de parámetros opcional utilizada por el compilador para vincular entradas y salidas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="03c8d-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="03c8d-174">Hay varias [semánticas](dx-graphics-hlsl-semantics.md) predefinidas para los sombreadores de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="03c8d-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="03c8d-175">El compilador omite la semántica a menos que se declaren en una variable global o un parámetro pasado a un sombreador.</span><span class="sxs-lookup"><span data-stu-id="03c8d-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="03c8d-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="03c8d-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-177">Palabra clave opcional para empaquetar manualmente las constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="03c8d-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="03c8d-178">Consulte [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span><span class="sxs-lookup"><span data-stu-id="03c8d-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="03c8d-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*El*</span><span class="sxs-lookup"><span data-stu-id="03c8d-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-180">Palabra clave opcional para asignar manualmente una variable de sombreador a un registro determinado.</span><span class="sxs-lookup"><span data-stu-id="03c8d-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="03c8d-181">Consulte [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span><span class="sxs-lookup"><span data-stu-id="03c8d-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="03c8d-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anotación (s)*</span><span class="sxs-lookup"><span data-stu-id="03c8d-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-183">Metadatos opcionales, en forma de cadena, adjuntos a una variable global.</span><span class="sxs-lookup"><span data-stu-id="03c8d-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="03c8d-184">El marco de trabajo usa una anotación y la omite HLSL. para ver una sintaxis más detallada, vea [Sintaxis de anotación](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="03c8d-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="03c8d-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Valor inicial*</span><span class="sxs-lookup"><span data-stu-id="03c8d-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="03c8d-186">Valores iniciales opcionales; el número de valores debe coincidir con el número de componentes de *tipo*.</span><span class="sxs-lookup"><span data-stu-id="03c8d-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="03c8d-187">Cada variable global marcada como **extern** debe inicializarse con un valor literal; cada variable marcada como **static** debe inicializarse con una constante.</span><span class="sxs-lookup"><span data-stu-id="03c8d-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="03c8d-188">Las variables globales que no están marcadas como **static** o **extern** no se compilan en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="03c8d-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="03c8d-189">El compilador no establece automáticamente los valores predeterminados para las variables globales y no puede utilizarlos en las optimizaciones.</span><span class="sxs-lookup"><span data-stu-id="03c8d-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="03c8d-190">Para inicializar este tipo de variable global, utilice la reflexión para obtener su valor y, a continuación, copie el valor en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="03c8d-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="03c8d-191">Por ejemplo, puede usar el método [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) para obtener la variable, usar el método [**ID3D11ShaderReflectionVariable:: GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) para obtener la descripción de la variable de sombreador y obtener el valor inicial del miembro **DefaultValue** de la estructura de la [**\_ \_ variable de \_ sombreador D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) .</span><span class="sxs-lookup"><span data-stu-id="03c8d-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="03c8d-192">Para copiar el valor en el búfer de constantes, debe asegurarse de que el búfer se creó con acceso de escritura de CPU ([**D3D11 de \_ acceso de CPU \_ \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span><span class="sxs-lookup"><span data-stu-id="03c8d-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="03c8d-193">Para obtener más información sobre cómo crear un búfer de constantes, vea [Cómo: crear un búfer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="03c8d-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="03c8d-194">También puede usar el [marco de trabajo de efectos](../direct3d11/d3d11-graphics-programming-guide-effects.md) para procesar automáticamente el reflejo y establecer el valor inicial.</span><span class="sxs-lookup"><span data-stu-id="03c8d-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="03c8d-195">Por ejemplo, puede usar el método [**ID3DX11EffectPass:: Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .</span><span class="sxs-lookup"><span data-stu-id="03c8d-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="03c8d-196">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="03c8d-196">Examples</span></span>

<span data-ttu-id="03c8d-197">Estos son algunos ejemplos de declaraciones de variables de sombreador.</span><span class="sxs-lookup"><span data-stu-id="03c8d-197">Here are several examples of shader-variable declarations.</span></span>


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a><span data-ttu-id="03c8d-198">Grupo compartido</span><span class="sxs-lookup"><span data-stu-id="03c8d-198">Group Shared</span></span>

<span data-ttu-id="03c8d-199">HLSL permite a los subprocesos de un sombreador de cálculo intercambiar valores a través de la memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="03c8d-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="03c8d-200">HLSL proporciona primitivas de barrera como [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), y así sucesivamente para garantizar el orden correcto de las lecturas y escrituras en la memoria compartida del sombreador y para evitar carreras de datos.</span><span class="sxs-lookup"><span data-stu-id="03c8d-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="03c8d-201">El hardware ejecuta subprocesos en grupos (alabeos o frontales) y la sincronización de barrera a veces se puede omitir para aumentar el rendimiento cuando solo se sincronizan los subprocesos que pertenecen al mismo grupo.</span><span class="sxs-lookup"><span data-stu-id="03c8d-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="03c8d-202">Pero se desaconseja encarecidamente esta omisión por estos motivos:</span><span class="sxs-lookup"><span data-stu-id="03c8d-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="03c8d-203">Esta omisión produce código no portable, que podría no funcionar en algún hardware y no funciona en rasterizadores de software que normalmente ejecutan subprocesos en grupos más pequeños.</span><span class="sxs-lookup"><span data-stu-id="03c8d-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="03c8d-204">Las mejoras de rendimiento que puede lograr con esta omisión serán menores en comparación con el uso de la barrera de todos los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="03c8d-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="03c8d-205">En Direct3D 10 no hay ninguna sincronización de subprocesos al escribir en **groupshared**, por lo que cada subproceso se limita a una única ubicación en una matriz para su escritura.</span><span class="sxs-lookup"><span data-stu-id="03c8d-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="03c8d-206">Use el valor del sistema [VP \_ GroupIndex](dx-graphics-hlsl-semantics.md) para indexar en esta matriz al escribir para asegurarse de que no haya dos subprocesos que puedan entrar en conflicto.</span><span class="sxs-lookup"><span data-stu-id="03c8d-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="03c8d-207">En cuanto a la lectura, todos los subprocesos tienen acceso a toda la matriz para su lectura.</span><span class="sxs-lookup"><span data-stu-id="03c8d-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a><span data-ttu-id="03c8d-208">Envase</span><span class="sxs-lookup"><span data-stu-id="03c8d-208">Packing</span></span>

<span data-ttu-id="03c8d-209">Empaquete subcomponentes de vectores y escalares cuyo tamaño sea lo suficientemente grande como para evitar límites de registro de cruce.</span><span class="sxs-lookup"><span data-stu-id="03c8d-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="03c8d-210">Por ejemplo, todos son válidos:</span><span class="sxs-lookup"><span data-stu-id="03c8d-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="03c8d-211">No se pueden mezclar tipos de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="03c8d-211">Cannot mix packing types.</span></span>

<span data-ttu-id="03c8d-212">Al igual que la palabra clave Register, un packoffset puede ser específico del destino.</span><span class="sxs-lookup"><span data-stu-id="03c8d-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="03c8d-213">El empaquetado de subcomponentes solo está disponible con la palabra clave packoffset, no con la palabra clave Register.</span><span class="sxs-lookup"><span data-stu-id="03c8d-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="03c8d-214">Dentro de una declaración de CBuffer, la palabra clave Register se omite para los destinos de Direct3D 10, ya que se supone que es para la compatibilidad entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="03c8d-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="03c8d-215">Los elementos empaquetados se pueden superponer y el compilador no proporcionará ningún error o advertencia.</span><span class="sxs-lookup"><span data-stu-id="03c8d-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="03c8d-216">En este ejemplo, Elemento2 y Element3 se superpondrán con Element1. x y Element1. y.</span><span class="sxs-lookup"><span data-stu-id="03c8d-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="03c8d-217">Un ejemplo que usa packoffset es: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="03c8d-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03c8d-218">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03c8d-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03c8d-219">Variables (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03c8d-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

