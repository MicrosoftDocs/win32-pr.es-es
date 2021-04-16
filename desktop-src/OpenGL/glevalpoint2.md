---
title: función glEvalPoint2 (GL. h)
description: Las funciones glEvalPoint1 y glEvalPoint2 generan y evalúan un solo punto en una malla. | función glEvalPoint2 (GL. h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- glEvalPoint2 (función) OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fafe728249f988462b0929873bbb195fed1e7c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689841"
---
# <a name="glevalpoint2-function"></a><span data-ttu-id="c8825-105">glEvalPoint2 función)</span><span class="sxs-lookup"><span data-stu-id="c8825-105">glEvalPoint2 function</span></span>

<span data-ttu-id="c8825-106">Las funciones [**glEvalPoint1**](glevalpoint.md) y **glEvalPoint2** generan y evalúan un solo punto en una malla.</span><span class="sxs-lookup"><span data-stu-id="c8825-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8825-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8825-107">Syntax</span></span>


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a><span data-ttu-id="c8825-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8825-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8825-109">*i*</span><span class="sxs-lookup"><span data-stu-id="c8825-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="c8825-110">Valor entero para la variable de dominio de la cuadrícula *i*.</span><span class="sxs-lookup"><span data-stu-id="c8825-110">The integer value for grid domain variable *i*.</span></span>

</dd> <dt>

<span data-ttu-id="c8825-111">*j*</span><span class="sxs-lookup"><span data-stu-id="c8825-111">*j*</span></span> 
</dt> <dd>

<span data-ttu-id="c8825-112">Valor entero para la variable de dominio de cuadrícula *j* .</span><span class="sxs-lookup"><span data-stu-id="c8825-112">The integer value for grid domain variable *j* .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8825-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8825-113">Return value</span></span>

<span data-ttu-id="c8825-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c8825-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8825-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8825-115">Remarks</span></span>

<span data-ttu-id="c8825-116">Las funciones [**glMapGrid**](glmapgrid-functions.md) y [**glEvalMesh**](glevalmesh-functions.md) se usan en conjunto para generar y evaluar eficazmente una serie de valores de dominio de mapa con espaciado uniforme.</span><span class="sxs-lookup"><span data-stu-id="c8825-116">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="c8825-117">Puede usar **glEvalPoint** para evaluar un solo punto de la cuadrícula en el mismo gridspace que atraviesa **glEvalMesh**.</span><span class="sxs-lookup"><span data-stu-id="c8825-117">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="c8825-118">Llamar a [**glEvalPoint1**](glevalpoint.md) es equivalente a llamar a</span><span class="sxs-lookup"><span data-stu-id="c8825-118">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="c8825-119">**glEvalCoord1** (*i* ?*u*  + *u* 1);</span><span class="sxs-lookup"><span data-stu-id="c8825-119">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="c8825-120">where</span><span class="sxs-lookup"><span data-stu-id="c8825-120">where</span></span>

<span data-ttu-id="c8825-121">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="c8825-121">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="c8825-122">y *n*, *u* 1 y *u* 2 son los argumentos de la función **glMapGrid1** más reciente.</span><span class="sxs-lookup"><span data-stu-id="c8825-122">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="c8825-123">El único requisito absoluto es que *, si*  =  *n*, el valor calculado de (*i* ?*u* + U1) es exactamente *u* 2.</span><span class="sxs-lookup"><span data-stu-id="c8825-123">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="c8825-124">En el caso bidimensional, **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="c8825-124">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="c8825-125">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="c8825-125">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="c8825-126">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="c8825-126">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="c8825-127">donde *n*, *u* 1, *u* 2, *m*, *v* 1 y *v* 2 son los argumentos de la función **glMapGrid2** más reciente.</span><span class="sxs-lookup"><span data-stu-id="c8825-127">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="c8825-128">A continuación, la función **glEvalPoint2** es equivalente a llamar a</span><span class="sxs-lookup"><span data-stu-id="c8825-128">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="c8825-129">**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  1);</span><span class="sxs-lookup"><span data-stu-id="c8825-129">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="c8825-130">Los únicos requisitos numéricos absolutos son que *, si* = *n*, el valor calculado de (*i* ?*u*  +  *u* 1) es exactamente U2 y, si es *j*  =  *m*, el valor calculado desde (*j* ?*v*  +  1) es exactamente *v* 2.</span><span class="sxs-lookup"><span data-stu-id="c8825-130">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="c8825-131">Las siguientes funciones recuperan información relacionada con [**glEvalPoint1**](glevalpoint.md) y **glEvalPoint2**:</span><span class="sxs-lookup"><span data-stu-id="c8825-131">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="c8825-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ MAP1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="c8825-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="c8825-133">**glGet** con el argumento GL \_ MAP2 ( \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="c8825-133">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="c8825-134">**glGet** con el argumento \_ MAP1 \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="c8825-134">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="c8825-135">**glGet** con el argumento \_ MAP2 ( \_ segmentos de cuadrícula de GL \_</span><span class="sxs-lookup"><span data-stu-id="c8825-135">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="c8825-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8825-136">Requirements</span></span>



| <span data-ttu-id="c8825-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8825-137">Requirement</span></span> | <span data-ttu-id="c8825-138">Value</span><span class="sxs-lookup"><span data-stu-id="c8825-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8825-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8825-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c8825-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8825-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c8825-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8825-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c8825-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8825-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c8825-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8825-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8825-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8825-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c8825-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8825-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8825-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8825-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8825-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8825-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8825-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8825-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8825-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8825-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8825-150">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="c8825-150">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c8825-151">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="c8825-151">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="c8825-152">**glGet**</span><span class="sxs-lookup"><span data-stu-id="c8825-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="c8825-153">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="c8825-153">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="c8825-154">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="c8825-154">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="c8825-155">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="c8825-155">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





