---
description: 'Función D3DXVec3BaryCentric (D3DX10Math.h): devuelve un punto en coordenadas centradas en Barycentric, mediante los vectores 3D especificados.'
ms.assetid: 572e151d-8044-480e-92b2-3f973d92d03e
title: Función D3DXVec3BaryCentric (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a0911a3e9e5bf0d1aa1df4d09f0b1fbcda0db2bc0bfe0c4c4b31da0f47c62999
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990645"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a>Función D3DXVec3BaryCentric (D3DX10Math.h)

Devuelve un punto en coordenadas centradas en Barycentric, utilizando los vectores 3D especificados.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _In_       D3DXVECTOR3 *pOut,
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2,
  _In_ const D3DXVECTOR3 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a [**D3DXVECTOR3 que**](d3d10-d3dxvector3.md) es el resultado de la operación.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3 de origen.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3 de origen.

</dd> <dt>

*pV3* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura D3DXVECTOR3 de origen.

</dd> <dt>

*f* \[ in\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> <dt>

*g* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura D3DXVECTOR3 en coordenadas centradas en Barycentric.

## <a name="remarks"></a>Comentarios

La función D3DXVec3BaryCentric proporciona una manera de comprender los puntos dentro y alrededor de un triángulo, independientemente de dónde se encuentra realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: V1 + f(V2-V1) + g(V3-V1).

Cualquier punto del plano V1V2V3 se puede representar mediante la coordenada Barycentric (f,g). El parámetro f controla la cantidad de V2 que se pondera en el resultado y el parámetro g controla la cantidad de V3 que se pondera en el resultado. Por último, 1-f-g controla la cantidad de V1 que se pondera en el resultado.

Tenga en cuenta las siguientes relaciones.

-   Si (f>=0 &, & g>=0 &, & 1-f-g>=0), el punto está dentro del triángulo V1V2V3.
-   Si (f==0 &, & g>=0 &, & 1-f-g>=0), el punto está en la línea V1V3.
-   Si (f>=0 &, & g==0 &, & 1-f-g>=0), el punto está en la línea V1V2.
-   Si (f>=0 &, & g>=0 &, & 1-f-g==0), el punto está en la línea V2V3.

Las coordenadas centradas en barras son una forma de coordenadas generales. En este contexto, el uso de coordenadas centradas en Bary representa un cambio en los sistemas de coordenadas. Lo que es cierto para las coordenadas cartesianas es true para las coordenadas barícéntricas.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXVec3BaryCentric se puede usar como parámetro para otra función.

Las coordenadas centradas en barras definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas centradas en barras, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
