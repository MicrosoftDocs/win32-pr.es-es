---
description: 'Función D3DXVec3ProjectArray (D3dx9math.h): proyecta una matriz (x, y, z, 0) desde el espacio del objeto al espacio de pantalla.'
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: Función D3DXVec3ProjectArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7ffc42934b9c341f4d07ef48a39470158155b4dfbcd352ffbc5e0ea188785752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749395"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a>Función D3DXVec3ProjectArray (D3dx9math.h)

Proyecta una matriz (x, y, z, 0) desde el espacio del objeto al espacio de pantalla.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a la [**estructura D3DXVECTOR3**](d3dxvector3.md) que es el resultado de la operación.

</dd> <dt>

*OutStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Pasos entre vectores en el flujo de datos de salida.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a la estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen.

</dd> <dt>

*VStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Pasos entre vectores en el flujo de datos de entrada.

</dd> <dt>

*pViewport* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Puntero a una [**estructura D3DVIEWPORT9,**](d3dviewport9.md) que representa la ventanilla.

</dd> <dt>

*pProjection* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz de proyección.

</dd> <dt>

*pView* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz de vistas.

</dd> <dt>

*pWorld* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una [**estructura D3DXMATRIX,**](d3dxmatrix.md) que representa la matriz mundial.

</dd> <dt>

*n* \[ en\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es la matriz proyectada desde el espacio de objetos al espacio de pantalla.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De este modo, la **función D3DXVec3ProjectArray** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Unproject**](d3dxvec3unproject.md)
</dt> </dl>

 

 
