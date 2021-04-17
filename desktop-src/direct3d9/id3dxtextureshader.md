---
description: La interfaz ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interfaz ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670226"
---
# <a name="id3dxtextureshader-interface"></a>Interfaz ID3DXTextureShader

La interfaz ID3DXTextureShader.

## <a name="members"></a>Miembros

La interfaz **ID3DXTextureShader** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureShader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXTextureShader** tiene estos métodos.



| Método                                                                                       | Descripción                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**GetConstant**](id3dxtextureshader--getconstant.md)                                       | Obtiene una constante mediante la búsqueda de su índice.<br/>                         |
| [**GetConstantBuffer**](id3dxtextureshader--getconstantbuffer.md)                           | Obtiene un puntero a la tabla de constantes.<br/>                             |
| [**GetConstantByName**](id3dxtextureshader--getconstantbyname.md)                           | Obtiene una constante buscando su nombre.<br/>                          |
| [**GetConstantDesc**](id3dxtextureshader--getconstantdesc.md)                               | Obtiene un puntero a la matriz de constantes de la tabla de constantes.<br/>  |
| [**GetConstantElement**](id3dxtextureshader--getconstantelement.md)                         | Obtiene una constante de la tabla de constantes.<br/>                          |
| [**GetDesc**](id3dxtextureshader--getdesc.md)                                               | Obtiene una descripción de la tabla de constantes.<br/>                        |
| [**GetFunction (**](id3dxtextureshader--getfunction.md)                                       | Obtiene un puntero a la secuencia DWORD de la función.<br/>                     |
| [**SetBool**](id3dxtextureshader--setbool.md)                                               | Establece un valor BOOLEANO.<br/>                                               |
| [**SetBoolArray**](id3dxtextureshader--setboolarray.md)                                     | Establece una matriz de valores BOOL.<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | Establece las constantes en los valores predeterminados declarados en el sombreador.<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | Establece un número de punto flotante.<br/>                                    |
| [**SetFloatArray**](id3dxtextureshader--setfloatarray.md)                                   | Establece una matriz de números de punto flotante.<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | Establece un valor entero.<br/>                                           |
| [**SetIntArray**](id3dxtextureshader--setintarray.md)                                       | Establece una matriz de enteros.<br/>                                       |
| [**SetMatrix**](id3dxtextureshader--setmatrix.md)                                           | Establece una matriz no transpuesta.<br/>                                    |
| [**SetMatrixArray**](id3dxtextureshader--setmatrixarray.md)                                 | Establece una matriz de matrices no transpuestas.<br/>                        |
| [**SetMatrixPointerArray**](id3dxtextureshader--setmatrixpointerarray.md)                   | Establece una matriz de punteros a matrices no transpuestas.<br/>            |
| [**SetMatrixTranspose**](id3dxtextureshader--setmatrixtranspose.md)                         | Establece una matriz transpuesta.<br/>                                        |
| [**SetMatrixTransposeArray**](id3dxtextureshader--setmatrixtransposearray.md)               | Establece una matriz de matrices transpuestas.<br/>                            |
| [**SetMatrixTransposePointerArray**](id3dxtextureshader--setmatrixtransposepointerarray.md) | Establece una matriz de punteros a matrices transpuestas.<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | Establece la tabla de constantes con los datos en el búfer.<br/>             |
| [**SetVector**](id3dxtextureshader--setvector.md)                                           | Establece un vector 4D.<br/>                                                |
| [**SetVectorArray**](id3dxtextureshader--setvectorarray.md)                                 | Establece una matriz de vectores 4D.<br/>                                     |



 

## <a name="remarks"></a>Observaciones

La interfaz **ID3DXTextureShader** se obtiene mediante una llamada a la función [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .

La interfaz **ID3DXTextureShader** , al igual que todas las interfaces com, hereda la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

El tipo LPD3DXTEXTURESHADER se define como un puntero a la interfaz **ID3DXTextureShader** .


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
