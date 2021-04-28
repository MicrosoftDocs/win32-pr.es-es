---
description: 'Función D3DXVec4Hermite (D3dx9math.h): realiza una interpolación spline de Hermite con los vectores 4D especificados.'
ms.assetid: 687d4dcf-ee75-4dda-b6d2-5ba0b5281a64
title: Función D3DXVec4Hermite (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08ed785c24ba9580be0fc7f620a471ea96184a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097703"
---
# <a name="d3dxvec4hermite-function-d3dx9mathh"></a>Función D3DXVec4Hermite (D3dx9math.h)

Realiza una interpolación spline de Hermite, utilizando los vectores 4D especificados.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a la [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen, un vector de posición.

</dd> <dt>

*pT1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen, un vector tangente.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen, un vector de posición.

</dd> <dt>

*pT2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura [**D3DXVECTOR4 de**](d3dxvector4.md) origen, un vector tangente.

</dd> <dt>

*s* \[ en\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Factor de ponderación. Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a una [**estructura D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la interpolación spline de Hermite.

## <a name="remarks"></a>Comentarios

La **función D3DXVec4Hermite** interpola de (positionA, tangentA) a (positionB, tangentB) mediante la interpolación spline de Hermite.

La interpolación spline es una generalización de la spline de facilidad de entrada y salida. La rampa es una función de preguntas y respuestas con las siguientes propiedades.

Q(s) = Aszos + Bs' + Cs + D (y, por lo tanto, Q's) = 3Asmiento + 2B + C)

a) Q(0) = v1, por lo que Q'(0) = t1

b) Q(1) = v2, por lo que Q'(1) = t2

v1 es el contenido de pV1, v2 en el contenido de pV2, t1 es el contenido de pT1 y t2 es el contenido de pT2.

Estas propiedades se usan para resolver A, B, C, D.

Conecte las soluciones para A, B, C y D para generar preguntas y respuestas.

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

El resultado es:

Q(s) = (2v1 - 2v2 + t2 + t1)s así + (3v2 - 3v1 - 2t1 - t2)sntes + t1 + v1

Que se puede reorganizar como:

Q(s) = (2sntes - 3s además de 1)v1 + (-2sntes + 3s así)v2 + (sntes - 2s además de s)t1 + (sntes - sntes)t2

Las curvas spline de Hermite son útiles para controlar la animación porque la curva se ejecuta a través de todos los puntos de control. Además, dado que la posición y la tangente se especifican explícitamente en los extremos de cada segmento, es fácil crear una curva continua C2 siempre que se asegúrese de que la posición inicial y la tangente coinciden con los valores finales del último segmento.

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De este modo, la **función D3DXVec4Hermite** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
