---
description: Crea un búfer de transferencia Radiance (PRT) precalculado que se puede comprimir o rellenar con un simulador. Esta función debe usarse para crear búferes de volumen o por vértices.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: Función D3DXCreatePRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718222"
---
# <a name="d3dxcreateprtbuffer-function"></a>D3DXCreatePRTBuffer función)

Crea un búfer de transferencia Radiance (PRT) precalculado que se puede comprimir o rellenar con un simulador. Esta función debe usarse para crear búferes de volumen o por vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumSamples* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices (o textura) muestreados.

</dd> <dt>

*NumCoeffs* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de coeficientes por ubicación de ejemplo. Cuando se usa el PRT esférico (SH) PRT, el número de coeficientes debe ser Order ², donde Order es el orden de la evaluación de SH. El orden debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. El grado de evaluación es order-1.

</dd> <dt>

*NumChannels* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de canales de color que se van a establecer en la malla. Establézcalo en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de sangrado de color.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Cuando se crea el búfer, todos los valores se inicializan en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de transferencia Radiance precalculadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
