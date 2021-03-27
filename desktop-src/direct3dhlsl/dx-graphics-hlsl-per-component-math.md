---
title: Operaciones matemáticas Per-Component
description: Con HLSL, puede programar sombreadores en un nivel de algoritmo.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ff30cd19b7821c9a059251e105f6acfa9cf961e
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/17/2021
ms.locfileid: "104987403"
---
# <a name="per-component-math-operations"></a><span data-ttu-id="8b83b-103">Operaciones matemáticas Per-Component</span><span class="sxs-lookup"><span data-stu-id="8b83b-103">Per-Component Math Operations</span></span>

<span data-ttu-id="8b83b-104">Con HLSL, puede programar sombreadores en un nivel de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="8b83b-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="8b83b-105">Para comprender el lenguaje, debe saber cómo declarar variables y funciones, usar funciones intrínsecas, definir tipos de datos personalizados y usar la semántica para conectar argumentos de sombreador a otros sombreadores y a la canalización.</span><span class="sxs-lookup"><span data-stu-id="8b83b-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="8b83b-106">Una vez que aprenda a crear sombreadores en HLSL, deberá obtener información sobre las llamadas de API para que pueda: compilar un sombreador para hardware determinado, inicializar constantes de sombreador e inicializar otro estado de canalización si es necesario.</span><span class="sxs-lookup"><span data-stu-id="8b83b-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="8b83b-107">Tipo de vector</span><span class="sxs-lookup"><span data-stu-id="8b83b-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="8b83b-108">El tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="8b83b-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="8b83b-109">Ordenación de matrices</span><span class="sxs-lookup"><span data-stu-id="8b83b-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="8b83b-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8b83b-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="8b83b-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b83b-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="8b83b-112">Tipo de vector</span><span class="sxs-lookup"><span data-stu-id="8b83b-112">The Vector Type</span></span>

<span data-ttu-id="8b83b-113">Un vector es una estructura de datos que contiene entre uno y cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="8b83b-114">El entero inmediatamente después del tipo de datos es el número de componentes del vector.</span><span class="sxs-lookup"><span data-stu-id="8b83b-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="8b83b-115">Los inicializadores también se pueden incluir en las declaraciones.</span><span class="sxs-lookup"><span data-stu-id="8b83b-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="8b83b-116">Como alternativa, el tipo de vector se puede usar para realizar las mismas declaraciones:</span><span class="sxs-lookup"><span data-stu-id="8b83b-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="8b83b-117">El tipo de vector usa corchetes angulares para especificar el tipo y el número de componentes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="8b83b-118">Los vectores contienen hasta cuatro componentes, a los que se puede tener acceso a través de uno de los dos conjuntos de nombres:</span><span class="sxs-lookup"><span data-stu-id="8b83b-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="8b83b-119">Conjunto de posiciones: x, y, z, w</span><span class="sxs-lookup"><span data-stu-id="8b83b-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="8b83b-120">Conjunto de colores: r, g, b, a</span><span class="sxs-lookup"><span data-stu-id="8b83b-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="8b83b-121">Estas instrucciones devuelven el valor en el tercer componente.</span><span class="sxs-lookup"><span data-stu-id="8b83b-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="8b83b-122">Los conjuntos de nombres pueden usar uno o varios componentes, pero no se pueden mezclar.</span><span class="sxs-lookup"><span data-stu-id="8b83b-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="8b83b-123">La especificación de uno o más componentes vectoriales al leer componentes se denomina permutación.</span><span class="sxs-lookup"><span data-stu-id="8b83b-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="8b83b-124">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8b83b-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="8b83b-125">Enmascaramiento controla el número de componentes que se escriben.</span><span class="sxs-lookup"><span data-stu-id="8b83b-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="8b83b-126">Las asignaciones no se pueden escribir más de una vez en el mismo componente.</span><span class="sxs-lookup"><span data-stu-id="8b83b-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="8b83b-127">Por lo tanto, el lado izquierdo de esta instrucción no es válido:</span><span class="sxs-lookup"><span data-stu-id="8b83b-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="8b83b-128">Además, los espacios de nombres de componente no se pueden mezclar.</span><span class="sxs-lookup"><span data-stu-id="8b83b-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="8b83b-129">Se trata de una escritura de componente no válida:</span><span class="sxs-lookup"><span data-stu-id="8b83b-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="8b83b-130">El acceso a un vector como escalar tendrá acceso al primer componente del vector.</span><span class="sxs-lookup"><span data-stu-id="8b83b-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="8b83b-131">Las dos instrucciones siguientes son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="8b83b-132">El tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="8b83b-132">The Matrix Type</span></span>

<span data-ttu-id="8b83b-133">Una matriz es una estructura de datos que contiene filas y columnas de datos.</span><span class="sxs-lookup"><span data-stu-id="8b83b-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="8b83b-134">Los datos pueden ser cualquiera de los tipos de datos escalares; sin embargo, todos los elementos de una matriz tienen el mismo tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8b83b-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="8b83b-135">El número de filas y columnas se especifica con la cadena de fila por columna anexada al tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8b83b-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



<span data-ttu-id="8b83b-136">El número máximo de filas o columnas es 4; el número mínimo es 1.</span><span class="sxs-lookup"><span data-stu-id="8b83b-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="8b83b-137">Una matriz se puede inicializar cuando se declara:</span><span class="sxs-lookup"><span data-stu-id="8b83b-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="8b83b-138">O bien, el tipo de matriz se puede usar para realizar las mismas declaraciones:</span><span class="sxs-lookup"><span data-stu-id="8b83b-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="8b83b-139">El tipo de matriz utiliza corchetes angulares para especificar el tipo, el número de filas y el número de columnas.</span><span class="sxs-lookup"><span data-stu-id="8b83b-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="8b83b-140">En este ejemplo se crea una matriz de punto flotante, con dos filas y dos columnas.</span><span class="sxs-lookup"><span data-stu-id="8b83b-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="8b83b-141">Se puede usar cualquiera de los tipos de datos escalares.</span><span class="sxs-lookup"><span data-stu-id="8b83b-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="8b83b-142">Esta declaración define una matriz de valores Float (números de punto flotante de 32 bits) con dos filas y tres columnas:</span><span class="sxs-lookup"><span data-stu-id="8b83b-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="8b83b-143">Una matriz contiene valores organizados en filas y columnas, a los que se puede tener acceso mediante el operador de estructura "." seguido de uno de los dos conjuntos de nombres:</span><span class="sxs-lookup"><span data-stu-id="8b83b-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="8b83b-144">Posición de la columna de fila de base cero:</span><span class="sxs-lookup"><span data-stu-id="8b83b-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="8b83b-145">\_M00, \_ M01, \_ M02, \_ M03</span><span class="sxs-lookup"><span data-stu-id="8b83b-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="8b83b-146">\_M10, \_ M11, \_ M12, \_ M13</span><span class="sxs-lookup"><span data-stu-id="8b83b-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="8b83b-147">\_M20, \_ M21, \_ M22, \_ M23</span><span class="sxs-lookup"><span data-stu-id="8b83b-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="8b83b-148">\_M30, \_ M31, \_ M32, \_ M33</span><span class="sxs-lookup"><span data-stu-id="8b83b-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="8b83b-149">La posición de la columna de fila basada en uno:</span><span class="sxs-lookup"><span data-stu-id="8b83b-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="8b83b-150">\_11, \_ 12, \_ 13, \_ 14</span><span class="sxs-lookup"><span data-stu-id="8b83b-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="8b83b-151">\_21, \_ 22, \_ 23, \_ 24</span><span class="sxs-lookup"><span data-stu-id="8b83b-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="8b83b-152">\_31, \_ 32, \_ 33, \_ 34</span><span class="sxs-lookup"><span data-stu-id="8b83b-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="8b83b-153">\_41, \_ 42, \_ 43, \_ 44</span><span class="sxs-lookup"><span data-stu-id="8b83b-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="8b83b-154">Cada conjunto de nomenclatura comienza con un carácter de subrayado seguido por el número de fila y el número de columna.</span><span class="sxs-lookup"><span data-stu-id="8b83b-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="8b83b-155">La Convención basada en cero también incluye la letra "m" antes del número de fila y columna.</span><span class="sxs-lookup"><span data-stu-id="8b83b-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="8b83b-156">Este es un ejemplo en el que se usan los dos conjuntos de nombres para tener acceso a una matriz:</span><span class="sxs-lookup"><span data-stu-id="8b83b-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



<span data-ttu-id="8b83b-157">Al igual que los vectores, los conjuntos de nomenclatura pueden usar uno o varios componentes de cualquier conjunto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="8b83b-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



<span data-ttu-id="8b83b-158">También se puede tener acceso a una matriz mediante la notación de acceso de matriz, que es un conjunto de índices de base cero.</span><span class="sxs-lookup"><span data-stu-id="8b83b-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="8b83b-159">Cada índice se encuentra entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="8b83b-160">Se tiene acceso a una matriz 4x4 con los índices siguientes:</span><span class="sxs-lookup"><span data-stu-id="8b83b-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="8b83b-161">\[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] , \[ 0 \] \[ 2 \] , \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8b83b-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="8b83b-162">\[1 \] \[ 0 \] , \[ 1 \] \[ 1 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8b83b-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="8b83b-163">\[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] , \[ 2 \] \[ 2 \] , \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8b83b-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="8b83b-164">\[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8b83b-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="8b83b-165">Este es un ejemplo de acceso a una matriz:</span><span class="sxs-lookup"><span data-stu-id="8b83b-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="8b83b-166">Observe que el operador de estructura "." no se utiliza para tener acceso a una matriz.</span><span class="sxs-lookup"><span data-stu-id="8b83b-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="8b83b-167">La notación de acceso a la matriz no puede usar permutación para leer más de un componente.</span><span class="sxs-lookup"><span data-stu-id="8b83b-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="8b83b-168">Sin embargo, el acceso a matrices puede leer un vector de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="8b83b-169">Al igual que con los vectores, la lectura de más de un componente de matriz se denomina permutación.</span><span class="sxs-lookup"><span data-stu-id="8b83b-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="8b83b-170">Se puede asignar más de un componente, siempre que se use un solo espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="8b83b-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="8b83b-171">Estas son todas las asignaciones válidas:</span><span class="sxs-lookup"><span data-stu-id="8b83b-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="8b83b-172">Enmascaramiento controla el número de componentes que se escriben.</span><span class="sxs-lookup"><span data-stu-id="8b83b-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="8b83b-173">Las asignaciones no se pueden escribir más de una vez en el mismo componente.</span><span class="sxs-lookup"><span data-stu-id="8b83b-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="8b83b-174">Por lo tanto, el lado izquierdo de esta instrucción no es válido:</span><span class="sxs-lookup"><span data-stu-id="8b83b-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="8b83b-175">Además, los espacios de nombres de componente no se pueden mezclar.</span><span class="sxs-lookup"><span data-stu-id="8b83b-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="8b83b-176">Se trata de una escritura de componente no válida:</span><span class="sxs-lookup"><span data-stu-id="8b83b-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="8b83b-177">Ordenación de matrices</span><span class="sxs-lookup"><span data-stu-id="8b83b-177">Matrix Ordering</span></span>

<span data-ttu-id="8b83b-178">El orden de empaquetado de la matriz para los parámetros uniformes se establece en columna-principal de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8b83b-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="8b83b-179">Esto significa que cada columna de la matriz se almacena en un único registro constante.</span><span class="sxs-lookup"><span data-stu-id="8b83b-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="8b83b-180">Por otro lado, una matriz de una fila principal de filas empaqueta cada fila de la matriz en un solo registro de constante.</span><span class="sxs-lookup"><span data-stu-id="8b83b-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="8b83b-181">El empaquetado de matrices se puede cambiar con la directiva **\# pragmapack \_ Matrix** o con la **fila \_ major** o la palabra clave **\_ major** .</span><span class="sxs-lookup"><span data-stu-id="8b83b-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="8b83b-182">Los datos de una matriz se cargan en registros de constantes del sombreador antes de que se ejecute un sombreador.</span><span class="sxs-lookup"><span data-stu-id="8b83b-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="8b83b-183">Hay dos opciones para la forma en que se leen los datos de la matriz: en orden de fila principal o en orden de columna principal.</span><span class="sxs-lookup"><span data-stu-id="8b83b-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="8b83b-184">El orden principal de las columnas significa que cada columna de la matriz se almacenará en un único registro constante y el orden principal de la fila significa que cada fila de la matriz se almacenará en un único registro constante.</span><span class="sxs-lookup"><span data-stu-id="8b83b-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="8b83b-185">Esta es una consideración importante para el número de registros constantes que se usan para una matriz.</span><span class="sxs-lookup"><span data-stu-id="8b83b-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="8b83b-186">Una matriz de filas principales se dispone de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8b83b-186">A row-major matrix is laid out like the following:</span></span>



|     |     |     |     |
|-----|-----|-----|-----|
| <span data-ttu-id="8b83b-187">11</span><span class="sxs-lookup"><span data-stu-id="8b83b-187">11</span></span>  | <span data-ttu-id="8b83b-188">12</span><span class="sxs-lookup"><span data-stu-id="8b83b-188">12</span></span>  | <span data-ttu-id="8b83b-189">13</span><span class="sxs-lookup"><span data-stu-id="8b83b-189">13</span></span>  | <span data-ttu-id="8b83b-190">14</span><span class="sxs-lookup"><span data-stu-id="8b83b-190">14</span></span>  |
| <span data-ttu-id="8b83b-191">21</span><span class="sxs-lookup"><span data-stu-id="8b83b-191">21</span></span>  | <span data-ttu-id="8b83b-192">22</span><span class="sxs-lookup"><span data-stu-id="8b83b-192">22</span></span>  | <span data-ttu-id="8b83b-193">23</span><span class="sxs-lookup"><span data-stu-id="8b83b-193">23</span></span>  | <span data-ttu-id="8b83b-194">24</span><span class="sxs-lookup"><span data-stu-id="8b83b-194">24</span></span>  |
| <span data-ttu-id="8b83b-195">31</span><span class="sxs-lookup"><span data-stu-id="8b83b-195">31</span></span>  | <span data-ttu-id="8b83b-196">32</span><span class="sxs-lookup"><span data-stu-id="8b83b-196">32</span></span>  | <span data-ttu-id="8b83b-197">33</span><span class="sxs-lookup"><span data-stu-id="8b83b-197">33</span></span>  | <span data-ttu-id="8b83b-198">34</span><span class="sxs-lookup"><span data-stu-id="8b83b-198">34</span></span>  |
| <span data-ttu-id="8b83b-199">41</span><span class="sxs-lookup"><span data-stu-id="8b83b-199">41</span></span>  | <span data-ttu-id="8b83b-200">42</span><span class="sxs-lookup"><span data-stu-id="8b83b-200">42</span></span>  | <span data-ttu-id="8b83b-201">43</span><span class="sxs-lookup"><span data-stu-id="8b83b-201">43</span></span>  | <span data-ttu-id="8b83b-202">44</span><span class="sxs-lookup"><span data-stu-id="8b83b-202">44</span></span>  |



 

<span data-ttu-id="8b83b-203">Una matriz de columnas principales se dispone de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8b83b-203">A column-major matrix is laid out like the following:</span></span>



|     |     |     |     |
|-----|-----|-----|-----|
| <span data-ttu-id="8b83b-204">11</span><span class="sxs-lookup"><span data-stu-id="8b83b-204">11</span></span>  | <span data-ttu-id="8b83b-205">21</span><span class="sxs-lookup"><span data-stu-id="8b83b-205">21</span></span>  | <span data-ttu-id="8b83b-206">31</span><span class="sxs-lookup"><span data-stu-id="8b83b-206">31</span></span>  | <span data-ttu-id="8b83b-207">41</span><span class="sxs-lookup"><span data-stu-id="8b83b-207">41</span></span>  |
| <span data-ttu-id="8b83b-208">12</span><span class="sxs-lookup"><span data-stu-id="8b83b-208">12</span></span>  | <span data-ttu-id="8b83b-209">22</span><span class="sxs-lookup"><span data-stu-id="8b83b-209">22</span></span>  | <span data-ttu-id="8b83b-210">32</span><span class="sxs-lookup"><span data-stu-id="8b83b-210">32</span></span>  | <span data-ttu-id="8b83b-211">42</span><span class="sxs-lookup"><span data-stu-id="8b83b-211">42</span></span>  |
| <span data-ttu-id="8b83b-212">13</span><span class="sxs-lookup"><span data-stu-id="8b83b-212">13</span></span>  | <span data-ttu-id="8b83b-213">23</span><span class="sxs-lookup"><span data-stu-id="8b83b-213">23</span></span>  | <span data-ttu-id="8b83b-214">33</span><span class="sxs-lookup"><span data-stu-id="8b83b-214">33</span></span>  | <span data-ttu-id="8b83b-215">43</span><span class="sxs-lookup"><span data-stu-id="8b83b-215">43</span></span>  |
| <span data-ttu-id="8b83b-216">14</span><span class="sxs-lookup"><span data-stu-id="8b83b-216">14</span></span>  | <span data-ttu-id="8b83b-217">24</span><span class="sxs-lookup"><span data-stu-id="8b83b-217">24</span></span>  | <span data-ttu-id="8b83b-218">34</span><span class="sxs-lookup"><span data-stu-id="8b83b-218">34</span></span>  | <span data-ttu-id="8b83b-219">44</span><span class="sxs-lookup"><span data-stu-id="8b83b-219">44</span></span>  |



 

<span data-ttu-id="8b83b-220">La ordenación de matrices principal y de columna principal de fila determina el orden en que los componentes de la matriz se leen de las entradas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="8b83b-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="8b83b-221">Una vez que los datos se escriben en registros constantes, el orden de las matrices no tiene ningún efecto en la forma en que se usan los datos o se accede a ellos desde el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="8b83b-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="8b83b-222">Además, las matrices declaradas en un cuerpo del sombreador no se empaquetan en registros constantes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="8b83b-223">El orden de empaquetado principal y de columna principal de fila no tiene influencia en el orden de empaquetado de los constructores (que siempre sigue el orden principal de las filas).</span><span class="sxs-lookup"><span data-stu-id="8b83b-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="8b83b-224">El orden de los datos de una matriz puede declararse en tiempo de compilación, o el compilador ordenará los datos en tiempo de ejecución para obtener el uso más eficaz.</span><span class="sxs-lookup"><span data-stu-id="8b83b-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="8b83b-225">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8b83b-225">Examples</span></span>

<span data-ttu-id="8b83b-226">HLSL usa dos tipos especiales, un tipo de vector y un tipo de matriz para facilitar la programación de gráficos 2D y 3D.</span><span class="sxs-lookup"><span data-stu-id="8b83b-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="8b83b-227">Cada uno de estos tipos contiene más de un componente; un vector contiene hasta cuatro componentes y una matriz que contiene hasta 16 componentes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="8b83b-228">Cuando se usan vectores y matrices en ecuaciones estándar de HLSL, la función matemática realizada está diseñada para trabajar por componente.</span><span class="sxs-lookup"><span data-stu-id="8b83b-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="8b83b-229">Por ejemplo, HLSL implementa esta multiplicación:</span><span class="sxs-lookup"><span data-stu-id="8b83b-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="8b83b-230">como una multiplicación de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-230">as a four-component multiply.</span></span> <span data-ttu-id="8b83b-231">El resultado es cuatro escalares:</span><span class="sxs-lookup"><span data-stu-id="8b83b-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="8b83b-232">Se trata de cuatro multiplicaciones donde cada resultado se almacena en un componente independiente de v.</span><span class="sxs-lookup"><span data-stu-id="8b83b-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="8b83b-233">Esto se denomina multiplicación de cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="8b83b-233">This is called a four-component multiply.</span></span> <span data-ttu-id="8b83b-234">HLSL usa Math de componentes, lo que hace que los sombreadores de escritura sean muy eficaces.</span><span class="sxs-lookup"><span data-stu-id="8b83b-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="8b83b-235">Esto es muy diferente de una multiplicación que normalmente se implementa como un producto punto que genera un único escalar:</span><span class="sxs-lookup"><span data-stu-id="8b83b-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="8b83b-236">Una matriz también usa operaciones por componente en HLSL:</span><span class="sxs-lookup"><span data-stu-id="8b83b-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="8b83b-237">El resultado es una multiplicación por componente de las dos matrices (en lugar de una multiplicación de una matriz de 3x3 estándar).</span><span class="sxs-lookup"><span data-stu-id="8b83b-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="8b83b-238">Una multiplicación por matriz de componentes produce este primer término:</span><span class="sxs-lookup"><span data-stu-id="8b83b-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="8b83b-239">Esto es diferente de la multiplicación de una matriz de 3x3 que produciría este primer término:</span><span class="sxs-lookup"><span data-stu-id="8b83b-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="8b83b-240">Las versiones sobrecargadas de la función intrínseca Multiply controlan los casos en los que un operando es un vector y el otro operando es una matriz.</span><span class="sxs-lookup"><span data-stu-id="8b83b-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="8b83b-241">Como: Vector vectorial \* , matriz vectorial \* , Vector de matriz \* y matriz de matriz \* .</span><span class="sxs-lookup"><span data-stu-id="8b83b-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="8b83b-242">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8b83b-242">For instance:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="8b83b-243">produce el mismo resultado que:</span><span class="sxs-lookup"><span data-stu-id="8b83b-243">produces the same result as:</span></span>


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



<span data-ttu-id="8b83b-244">En este ejemplo se convierte el vector de pos en un vector de columna mediante la conversión (float1x4).</span><span class="sxs-lookup"><span data-stu-id="8b83b-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="8b83b-245">Cambiar un vector mediante la conversión o cambiar el orden de los argumentos proporcionados a Multiply es equivalente a transponer la matriz.</span><span class="sxs-lookup"><span data-stu-id="8b83b-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="8b83b-246">La conversión de conversión automática hace que las funciones intrínsecas Multiply y DOT devuelvan los mismos resultados que se usan aquí:</span><span class="sxs-lookup"><span data-stu-id="8b83b-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="8b83b-247">Este resultado de la multiplicación es un \* Vector 4 TB = 1x1.</span><span class="sxs-lookup"><span data-stu-id="8b83b-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="8b83b-248">Esto es equivalente a un producto DOT:</span><span class="sxs-lookup"><span data-stu-id="8b83b-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="8b83b-249">que devuelve un único valor escalar.</span><span class="sxs-lookup"><span data-stu-id="8b83b-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b83b-250">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b83b-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b83b-251">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8b83b-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




