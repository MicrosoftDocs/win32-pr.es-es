---
description: Aplica los datos de medianil de textura almacenados a un búfer de textura de ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'ID3DXPRTBuffer:: EvalGH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708118"
---
# <a name="id3dxprtbufferevalgh-method"></a>ID3DXPRTBuffer:: EvalGH (método)

Aplica los datos de medianil de textura almacenados a un búfer de textura de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente.

## <a name="remarks"></a>Observaciones

Este método realiza una llamada interna a [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) para recuperar y aplicar los datos de medianil de textura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




