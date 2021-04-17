---
description: Devuelve un punto en coordenadas de Barycentric, usando los vectores 3D especificados.
ms.assetid: 572e151d-8044-480e-92b2-3f973d92d03e
title: Función D3DXVec3BaryCentric (D3DX10Math. h)
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
ms.openlocfilehash: 3c14d01acc71a13cabb810d5b26d0afaf7f67f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698274"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a>Función D3DXVec3BaryCentric (D3DX10Math. h)

Devuelve un punto en coordenadas de Barycentric, usando los vectores 3D especificados.

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

*pOut* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero al [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura de D3DXVECTOR3 de origen.

</dd> <dt>

*pV2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura de D3DXVECTOR3 de origen.

</dd> <dt>

*pV3* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a una estructura de D3DXVECTOR3 de origen.

</dd> <dt>

*f* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> <dt>

*g* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura D3DXVECTOR3 en coordenadas Barycentric.

## <a name="remarks"></a>Observaciones

La función D3DXVec3BaryCentric proporciona una manera de comprender los puntos en y alrededor de un triángulo, independientemente de dónde se encuentre realmente el triángulo. Esta función devuelve el punto resultante mediante la siguiente ecuación: v1 + f (V2-V1) + g (V3-V1).

Cualquier punto del V1V2V3 de plano se puede representar mediante la coordenada Barycentric (f, g). El parámetro f controla la cantidad de v2 que se pondera en el resultado y el parámetro g controla la cantidad de V3 que se pondera en el resultado. Por último, 1-f-g controla la cantidad de la versión 1 que se pondera en el resultado.

Tenga en cuenta las siguientes relaciones.

-   Si (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), el punto está dentro del triángulo V1V2V3.
-   Si (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), el punto se encuentra en la línea V1V3.
-   Si (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), el punto se encuentra en la línea V1V2.
-   Si (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), el punto se encuentra en la línea V2V3.

Las coordenadas de Barycentric son una forma de coordenadas generales. En este contexto, el uso de coordenadas Barycentric representa un cambio en los sistemas de coordenadas. Lo que sucede para las coordenadas cartesianas es true para las coordenadas Barycentric.

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut. De esta manera, la función D3DXVec3BaryCentric se puede usar como parámetro de otra función.

Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
