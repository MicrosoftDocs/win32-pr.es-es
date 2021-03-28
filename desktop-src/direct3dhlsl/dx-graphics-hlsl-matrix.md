---
title: Tipo de matriz
description: Una matriz es un tipo de datos Especial que contiene entre uno y dieciséis componentes. Cada componente de una matriz debe ser del mismo tipo.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Tipo de matriz HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c580706a2ddae3e4a94c138a1ca0f6932457732a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076532"
---
# <a name="matrix-type"></a><span data-ttu-id="f5575-105">Tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="f5575-105">Matrix Type</span></span>

<span data-ttu-id="f5575-106">Una matriz es un tipo de datos Especial que contiene entre uno y dieciséis componentes.</span><span class="sxs-lookup"><span data-stu-id="f5575-106">A matrix is a special data type that contains between one and sixteen components.</span></span> <span data-ttu-id="f5575-107">Cada componente de una matriz debe ser del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="f5575-107">Every component of a matrix must be of the same type.</span></span>



|                         |
|-------------------------|
| <span data-ttu-id="f5575-108">**Nombre de TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="f5575-108">**TypeComponents Name**</span></span> |



 

## <a name="components"></a><span data-ttu-id="f5575-109">Componentes</span><span class="sxs-lookup"><span data-stu-id="f5575-109">Components</span></span>



| <span data-ttu-id="f5575-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f5575-110">Item</span></span>                                                                                                                             | <span data-ttu-id="f5575-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5575-111">Description</span></span>                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5575-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="f5575-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="f5575-113">Un nombre único que contiene tres partes.</span><span class="sxs-lookup"><span data-stu-id="f5575-113">A single name that contains three parts.</span></span> <span data-ttu-id="f5575-114">La primera parte es uno de los tipos [escalares](dx-graphics-hlsl-data-types.md) .</span><span class="sxs-lookup"><span data-stu-id="f5575-114">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="f5575-115">La segunda parte es el número de filas.</span><span class="sxs-lookup"><span data-stu-id="f5575-115">The second part is the number of rows.</span></span> <span data-ttu-id="f5575-116">La tercera parte es el número de columnas.</span><span class="sxs-lookup"><span data-stu-id="f5575-116">The third part is the number of columns.</span></span> <span data-ttu-id="f5575-117">El número de filas y columnas es un entero positivo comprendido entre 1 y 4, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="f5575-117">The number of rows and columns is a positive integer between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="f5575-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span><span class="sxs-lookup"><span data-stu-id="f5575-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="f5575-119">Cadena ASCII que identifica de forma única el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="f5575-119">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a><span data-ttu-id="f5575-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f5575-120">Examples</span></span>

<span data-ttu-id="f5575-121">A continuación se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="f5575-121">Here are some examples:</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="f5575-122">Una matriz se puede declarar con esta sintaxis también:</span><span class="sxs-lookup"><span data-stu-id="f5575-122">A matrix can be declared using this syntax also:</span></span>


```
matrix <Type, Number> VariableName
```



<span data-ttu-id="f5575-123">El tipo de matriz utiliza corchetes angulares para especificar el tipo, el número de filas y el número de columnas.</span><span class="sxs-lookup"><span data-stu-id="f5575-123">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="f5575-124">En este ejemplo se crea una matriz de punto flotante, con dos filas y dos columnas.</span><span class="sxs-lookup"><span data-stu-id="f5575-124">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="f5575-125">Se puede usar cualquiera de los tipos de datos escalares.</span><span class="sxs-lookup"><span data-stu-id="f5575-125">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="f5575-126">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f5575-126">Here is an example:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a><span data-ttu-id="f5575-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5575-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5575-128">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5575-128">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





