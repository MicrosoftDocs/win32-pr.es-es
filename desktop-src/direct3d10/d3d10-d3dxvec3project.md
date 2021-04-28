---
description: 'Función D3DXVec3Project (D3DX10Math.h): proyecta un vector 3D desde el espacio de objetos en el espacio de la pantalla.'
ms.assetid: 6fc59788-c3f7-4f47-a345-9108105e820e
title: Función D3DXVec3Project (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: f4a2cffa77b2a66267daf0a67a59698ae3e3b8eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108173"
---
# <a name="d3dxvec3project-function-d3dx10mathh"></a>Función D3DXVec3Project (D3DX10Math.h)

Proyecta un vector 3D desde el espacio del objeto en el espacio de la pantalla.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a [**D3DXVECTOR3 que**](d3d10-d3dxvector3.md) es el resultado de la operación.

</dd> <dt>

*pV* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntero a la estructura D3DXVECTOR3 de origen.

</dd> <dt>

*pViewport* \[ En\]
</dt> <dd>

Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***

Puntero a una [**ventanilla D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), que representa la ventanilla.

</dd> <dt>

*pProjection* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a una [**estructura D3DXMATRIX,**](d3d10-d3dxmatrix.md) que representa la matriz de proyección.

</dd> <dt>

*pView* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a una estructura D3DXMATRIX, que representa la matriz de vistas.

</dd> <dt>

*pWorld* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Puntero a una estructura D3DXMATRIX, que representa la matriz mundial.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntero a una estructura D3DXVECTOR3 que es el vector proyectado desde el espacio del objeto al espacio de pantalla.

## <a name="remarks"></a>Comentarios

El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut. De esta manera, la función D3DXVec3Project se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
