---
description: 'Función D3DXFresnelTerm (D3dx9math.h): calcule el término Fresnel.'
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: Función D3DXFresnelTerm (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15f0c5bac66d0c1b43bf3938e4ecb1f2fffd8dd235532b5dddc27eb5923ef5f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027655"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a>Función D3DXFresnelTerm (D3dx9math.h)

Calcule el término Fresnel.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CosTheta* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

El valor debe estar entre 0 y 1.

</dd> <dt>

*RefracciónIndex* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Índice de reanuración de un material. El valor debe ser mayor que 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Esta función devuelve el término Fresnel para la luz nopolarizada. CosTheta es el coseno del ángulo del incidente.

## <a name="remarks"></a>Comentarios

Para buscar el término Fresnel (F):

Si A es el ángulo de la incidencia y B es el ángulo de reanguía,


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



A continuación, al expandir con las identidades trig y simplificar, obtiene lo siguiente:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
