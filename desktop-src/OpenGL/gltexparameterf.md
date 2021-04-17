---
title: función glTexParameterf (GL. h)
description: Establece los parámetros de textura. | función glTexParameterf (GL. h)
ms.assetid: 20b9f2d5-66e1-41cd-9571-8caa38ef033d
keywords:
- glTexParameterf (función) OpenGL
topic_type:
- apiref
api_name:
- glTexParameterf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f749513757ee32f6fe468dadbe968b8657a06f3d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689772"
---
# <a name="gltexparameterf-function"></a><span data-ttu-id="8cb78-105">glTexParameterf función)</span><span class="sxs-lookup"><span data-stu-id="8cb78-105">glTexParameterf function</span></span>

<span data-ttu-id="8cb78-106">Establece los parámetros de textura.</span><span class="sxs-lookup"><span data-stu-id="8cb78-106">Sets texture parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb78-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cb78-107">Syntax</span></span>


```C++
void WINAPI glTexParameterf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="8cb78-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cb78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb78-109">*Destino*</span><span class="sxs-lookup"><span data-stu-id="8cb78-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8cb78-110">Textura de destino, que debe ser la textura de GL \_ \_ 1D o la textura de GL \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="8cb78-110">The target texture, which must be either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="8cb78-111">*PName*</span><span class="sxs-lookup"><span data-stu-id="8cb78-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="8cb78-112">Nombre simbólico de un parámetro de textura de valor único.</span><span class="sxs-lookup"><span data-stu-id="8cb78-112">The symbolic name of a single valued texture parameter.</span></span> <span data-ttu-id="8cb78-113">Los siguientes símbolos se aceptan en *PName*.</span><span class="sxs-lookup"><span data-stu-id="8cb78-113">The following symbols are accepted in *pname*.</span></span>



| <span data-ttu-id="8cb78-114">Value</span><span class="sxs-lookup"><span data-stu-id="8cb78-114">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="8cb78-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8cb78-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="8cb78-116"><dt>**\_ \_ filtro mínimo de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-116"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="8cb78-117">La función Texture minificar se usa siempre que el píxel al que se aplica la textura se asigna a un área mayor que un elemento de textura.</span><span class="sxs-lookup"><span data-stu-id="8cb78-117">The texture minifying function is used whenever the pixel being textured maps to an area greater than one texture element.</span></span> <span data-ttu-id="8cb78-118">Hay seis funciones minificar definidas.</span><span class="sxs-lookup"><span data-stu-id="8cb78-118">There are six defined minifying functions.</span></span> <span data-ttu-id="8cb78-119">Dos de ellos usan la más cercana, o los cuatro elementos de textura más cercanos, para calcular el valor de textura.</span><span class="sxs-lookup"><span data-stu-id="8cb78-119">Two of them use the nearest one or nearest four texture elements to compute the texture value.</span></span> <span data-ttu-id="8cb78-120">Los otros cuatro mapas de uso.</span><span class="sxs-lookup"><span data-stu-id="8cb78-120">The other four use mipmaps.</span></span><br/> <span data-ttu-id="8cb78-121">Un mipmap es un conjunto ordenado de matrices que representa la misma imagen con una resolución progresivamente inferior.</span><span class="sxs-lookup"><span data-stu-id="8cb78-121">A mipmap is an ordered set of arrays representing the same image at progressively lower resolutions.</span></span> <span data-ttu-id="8cb78-122">Si la textura tiene dimensiones 2nx2<sup>m</sup> , hay un número máximo de mapas de caracteres (n, m) + 1.</span><span class="sxs-lookup"><span data-stu-id="8cb78-122">If the texture has dimensions 2nx2<sup>m</sup> there are max(n, m) + 1 mipmaps.</span></span> <span data-ttu-id="8cb78-123">El primer mipmap es la textura original, con las dimensiones 2nx2<sup>m</sup>.</span><span class="sxs-lookup"><span data-stu-id="8cb78-123">The first mipmap is the original texture, with dimensions 2nx2<sup>m</sup>.</span></span> <span data-ttu-id="8cb78-124">Cada MIP subsiguiente tiene dimensiones 2<sup>k</sup>1x2<sup>l</sup>1, donde 2<sup>k</sup>x2<sup>l</sup> son las dimensiones del mipmap anterior, hasta que k = 0 o l = 0.</span><span class="sxs-lookup"><span data-stu-id="8cb78-124">Each subsequent mipmap has dimensions 2<sup>k</sup>1x2<sup>l</sup>1 where 2<sup>k</sup>x2<sup>l</sup> are the dimensions of the previous mipmap, until either k = 0 or l = 0.</span></span> <span data-ttu-id="8cb78-125">En ese momento, los mapas de operaciones posteriores tienen la dimensión 1x2<sup>l</sup>1 o 2<sup>k</sup>1x1 hasta el mipmap final, que tiene una dimensión 1x1.</span><span class="sxs-lookup"><span data-stu-id="8cb78-125">At that point, subsequent mipmaps have dimension 1x2<sup>l</sup>1 or 2<sup>k</sup>1x1 until the final mipmap, which has dimension 1x1.</span></span> <span data-ttu-id="8cb78-126">Los mapas MIP se definen mediante [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md) con el argumento de nivel de detalle que indica el orden de los mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="8cb78-126">Mipmaps are defined using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md) with the level-of-detail argument indicating the order of the mipmaps.</span></span> <span data-ttu-id="8cb78-127">El nivel 0 es la textura original; el nivel de negrita máximo (n, m) es el mipmap de 1x1 final.</span><span class="sxs-lookup"><span data-stu-id="8cb78-127">Level 0 is the original texture; level bold max(n, m) is the final 1x1 mipmap.</span></span><br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="8cb78-128"><dt>**\_filtro de textura de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-128"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl> | <span data-ttu-id="8cb78-129">La función de aumento de textura se usa cuando el píxel al que se aplica la textura se asigna a un área menor o igual que un elemento de textura.</span><span class="sxs-lookup"><span data-stu-id="8cb78-129">The texture magnification function is used when the pixel being textured maps to an area less than or equal to one texture element.</span></span> <span data-ttu-id="8cb78-130">Establece la función de aumento de la textura en GL \_ más próximo o en GL \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="8cb78-130">It sets the texture magnification function to either GL\_NEAREST or GL\_LINEAR.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="8cb78-131"><dt>**\_ajuste de textura de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-131"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>             | <span data-ttu-id="8cb78-132">Establece el parámetro Wrap para las coordenadas de textura s en la \_ abrazadera de GL o en la repetición de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="8cb78-132">Sets the wrap parameter for texture coordinate s to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="8cb78-133">\_La abrazadera GL hace que las coordenadas s se detengan en el intervalo \[ 0, 1 \] y es útil para evitar los artefactos de ajuste al asignar una sola imagen a un objeto.</span><span class="sxs-lookup"><span data-stu-id="8cb78-133">GL\_CLAMP causes s coordinates to be clamped to the range \[0,1\] and is useful for preventing wrapping artifacts when mapping a single image onto an object.</span></span> <span data-ttu-id="8cb78-134">\_La repetición de GL hace que se omita la parte entera de la coordenada s; OpenGL solo usa la parte fraccionaria, con lo que se crea un patrón de repetición.</span><span class="sxs-lookup"><span data-stu-id="8cb78-134">GL\_REPEAT causes the integer part of the s coordinate to be ignored; OpenGL uses only the fractional part, thereby creating a repeating pattern.</span></span> <span data-ttu-id="8cb78-135">Solo se tiene acceso a los elementos de textura de borde si el ajuste está establecido en abrazadera de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="8cb78-135">Border texture elements are accessed only if wrapping is set to GL\_CLAMP.</span></span> <span data-ttu-id="8cb78-136">Inicialmente, el \_ ajuste de textura de GL \_ \_ se establece en libro de \_ repetición.</span><span class="sxs-lookup"><span data-stu-id="8cb78-136">Initially, GL\_TEXTURE\_WRAP\_S is set to GL\_REPEAT.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="8cb78-137"><dt>**ajuste de textura de GL \_ \_ \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-137"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>             | <span data-ttu-id="8cb78-138">Establece el parámetro Wrap para la coordenada de textura t en la \_ abrazadera de GL o en la repetición de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="8cb78-138">Sets the wrap parameter for texture coordinate t to either GL\_CLAMP or GL\_REPEAT.</span></span> <span data-ttu-id="8cb78-139">Vea la explicación de la sección sobre el ajuste de textura de GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8cb78-139">See the discussion under GL\_TEXTURE\_WRAP\_S.</span></span> <span data-ttu-id="8cb78-140">Inicialmente, el \_ \_ ajuste \_ de textura de GL T se establece en GL \_ REPEAT.</span><span class="sxs-lookup"><span data-stu-id="8cb78-140">Initially, GL\_TEXTURE\_WRAP\_T is set to GL\_REPEAT</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="8cb78-141">*param*</span><span class="sxs-lookup"><span data-stu-id="8cb78-141">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="8cb78-142">El valor de *PName*.</span><span class="sxs-lookup"><span data-stu-id="8cb78-142">The value of *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cb78-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cb78-143">Return value</span></span>

<span data-ttu-id="8cb78-144">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8cb78-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8cb78-145">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8cb78-145">Error codes</span></span>

<span data-ttu-id="8cb78-146">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="8cb78-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8cb78-147">Nombre</span><span class="sxs-lookup"><span data-stu-id="8cb78-147">Name</span></span>                                                                                                  | <span data-ttu-id="8cb78-148">Significado</span><span class="sxs-lookup"><span data-stu-id="8cb78-148">Meaning</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8cb78-149"><dt>**Libro de contabilidad \_ \_enumeración no válida**</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-149"><dt>**GL\_INVALID\_ENUM** </dt></span></span> </dl>     | <span data-ttu-id="8cb78-150">el *destino* o *PName* no era uno de los valores definidos aceptados o cuando el *parámetro* debe tener un valor constante definido (basado en el valor de *PName*) y no lo hizo.</span><span class="sxs-lookup"><span data-stu-id="8cb78-150">*target* or *pname* was not one of the accepted defined values, or when *param* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="8cb78-151"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8cb78-152">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8cb78-152">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="8cb78-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cb78-153">Remarks</span></span>

<span data-ttu-id="8cb78-154">La asignación de texturas es una técnica que aplica una imagen a la superficie de un objeto como si la imagen fuera una Decal o Cellophane shrink-wrap.</span><span class="sxs-lookup"><span data-stu-id="8cb78-154">Texture mapping is a technique that applies an image onto an object's surface as if the image were a decal or cellophane shrink-wrap.</span></span> <span data-ttu-id="8cb78-155">La imagen se crea en el espacio de textura, con un sistema de coordenadas (*s*, *t*).</span><span class="sxs-lookup"><span data-stu-id="8cb78-155">The image is created in texture space, with an (*s*, *t*) coordinate system.</span></span> <span data-ttu-id="8cb78-156">Una textura es una imagen de una o dos dimensiones y un conjunto de parámetros que determinan cómo se derivan los ejemplos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="8cb78-156">A texture is a one- or two-dimensional image and a set of parameters that determine how samples are derived from the image.</span></span>

<span data-ttu-id="8cb78-157">La función **glTexParameter** asigna el valor o los valores de los parámetros al parámetro Texture especificado como PName.</span><span class="sxs-lookup"><span data-stu-id="8cb78-157">The **glTexParameter** function assigns the value or values in params to the texture parameter specified as pname.</span></span> <span data-ttu-id="8cb78-158">El parámetro de destino define la textura de destino, ya sea \_ \_ 1D Texture o textura de GL \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="8cb78-158">The target parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="8cb78-159">A medida que se muestren más elementos de textura en el proceso minificación, se mostrarán menos artefactos de alias.</span><span class="sxs-lookup"><span data-stu-id="8cb78-159">As more texture elements are sampled in the minification process, fewer aliasing artifacts will be apparent.</span></span> <span data-ttu-id="8cb78-160">Aunque las \_ funciones de minificación lineal de GL más próximas y de GL \_ pueden ser más rápidas que las otras cuatro, solo muestrean uno o cuatro elementos de textura para determinar el valor de textura del píxel que se representa y pueden generar patrones Moire o transiciones desiguales.</span><span class="sxs-lookup"><span data-stu-id="8cb78-160">While the GL\_NEAREST and GL\_LINEAR minification functions can be faster than the other four, they sample only one or four texture elements to determine the texture value of the pixel being rendered and can produce moire patterns or ragged transitions.</span></span> <span data-ttu-id="8cb78-161">El valor predeterminado de \_ filtro de textura mín. de la contabilidad \_ \_ es GL \_ más cercano \_ \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="8cb78-161">The default value of GL\_TEXTURE\_MIN\_FILTER is GL\_NEAREST\_MIPMAP\_LINEAR.</span></span>

<span data-ttu-id="8cb78-162">Supongamos que la texturización está habilitada (mediante una llamada a [**glEnable**](glenable.md) con el argumento GL de \_ la textura 1D o la textura de GL \_ \_ \_ 2D) y el \_ \_ \_ filtro mínimo de textura de GL está establecido en una de las funciones que requieren un mipmap.</span><span class="sxs-lookup"><span data-stu-id="8cb78-162">Suppose that texturing is enabled (by calling [**glEnable**](glenable.md) with argument GL\_TEXTURE\_1D or GL\_TEXTURE\_2D) and GL\_TEXTURE\_MIN\_FILTER is set to one of the functions that requires a mipmap.</span></span> <span data-ttu-id="8cb78-163">Si las dimensiones de las imágenes de textura definidas actualmente (con llamadas anteriores a [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md)) no siguen la secuencia adecuada para los mapas MIP, o hay menos imágenes de textura definidas que son necesarias, o el conjunto de imágenes de textura tiene un número diferente de componentes de textura, es como si se hubiera deshabilitado la asignación de textura.</span><span class="sxs-lookup"><span data-stu-id="8cb78-163">If either the dimensions of the texture images currently defined (with previous calls to [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md)) do not follow the proper sequence for mipmaps, or there are fewer texture images defined than are needed, or the set of texture images have differing numbers of texture components, then it is as if texture mapping were disabled.</span></span> <span data-ttu-id="8cb78-164">El filtrado lineal accede a los cuatro elementos de textura más cercanos solo en texturas 2D.</span><span class="sxs-lookup"><span data-stu-id="8cb78-164">Linear filtering accesses the four nearest texture elements only in 2-D textures.</span></span> <span data-ttu-id="8cb78-165">En las texturas 1D, el filtrado lineal tiene acceso a los dos elementos de textura más cercanos.</span><span class="sxs-lookup"><span data-stu-id="8cb78-165">In 1-D textures, linear filtering accesses the two nearest texture elements.</span></span> <span data-ttu-id="8cb78-166">La siguiente función recupera información relacionada con **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** y **glTexParameteriv**.</span><span class="sxs-lookup"><span data-stu-id="8cb78-166">The following function retrieves information related to **glTexParameterf**, **glTexParameteri**, **glTexParameterfv**, and **glTexParameteriv**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb78-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cb78-167">Requirements</span></span>



| <span data-ttu-id="8cb78-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cb78-168">Requirement</span></span> | <span data-ttu-id="8cb78-169">Value</span><span class="sxs-lookup"><span data-stu-id="8cb78-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb78-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cb78-170">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb78-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8cb78-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8cb78-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cb78-172">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb78-173">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cb78-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8cb78-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cb78-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cb78-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8cb78-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cb78-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="8cb78-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8cb78-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8cb78-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cb78-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cb78-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cb78-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cb78-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb78-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8cb78-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8cb78-182">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="8cb78-182">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="8cb78-183">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="8cb78-183">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="8cb78-184">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8cb78-184">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8cb78-185">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8cb78-185">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8cb78-186">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="8cb78-186">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="8cb78-187">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="8cb78-187">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="8cb78-188">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8cb78-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8cb78-189">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="8cb78-189">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="8cb78-190">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="8cb78-190">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="8cb78-191">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="8cb78-191">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="8cb78-192">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="8cb78-192">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="8cb78-193">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="8cb78-193">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="8cb78-194">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="8cb78-194">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="8cb78-195">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8cb78-195">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8cb78-196">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8cb78-196">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8cb78-197">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="8cb78-197">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="8cb78-198">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="8cb78-198">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





