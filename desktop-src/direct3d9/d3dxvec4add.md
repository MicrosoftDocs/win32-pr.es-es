---
description: Agrega dos vectores 4D.
ms.assetid: da807dc0-6a31-4315-a32d-a42062c22199
title: Función D3DXVec4Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62747cec15c4a9916dfb42572006cbb9fc908b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649445"
---
# <a name="d3dxvec4add-function"></a>D3DXVec4Add función)

Agrega dos vectores 4D.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR4* D3DXVec4Add(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a la estructura [**D3DXVECTOR4**](d3dxvector4.md) que es el resultado de la operación.

</dd> <dt>

*pV1* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.

</dd> <dt>

*pV2* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Puntero a una estructura [**D3DXVECTOR4**](d3dxvector4.md) que es la suma de los dos vectores.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, la función **D3DXVec4Add** se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Subtract**](d3dxvec4subtract.md)
</dt> <dt>

[**D3DXVec4Scale**](d3dxvec4scale.md)
</dt> </dl>

 

 




