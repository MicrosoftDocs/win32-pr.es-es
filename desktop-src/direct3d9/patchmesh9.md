---
description: PatchMesh9 define una malla definida por las revisiones de Bézier, incluida una lista de vértices y las revisiones de la malla mediante la indexación en la matriz de vértices.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404708"
---
# <a name="patchmesh9"></a>PatchMesh9

Define una malla definida por las revisiones de Bézier. La primera matriz es una lista de vértices y la segunda matriz define las revisiones de la malla mediante la indexación en la matriz de vértices.

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

Donde:

-   Tipo: tipo de malla de revisión: rectángulo, triángulo o N revisiones.
-   Degree: grado de las variables de la ecuación de curva.
-   Base: tipo base de una superficie de revisión de orden superior.
-   nVertices: número de vértices.
-   vértices \[ nVertices: \] matriz de vértices. Vea [**Vector**](vector.md).
-   nPatches: número de revisiones.
-   patches \[ nPatches: \] matriz de revisiones. Consulte [**Revisión**](patch.md)de .
-   \[ ... \] - Cualquier plantilla de archivo .x se puede usar aquí. Esto hace que la arquitectura sea extensible.

Las revisiones usan los vértices de la matriz de vértices como puntos de control para cada revisión.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



