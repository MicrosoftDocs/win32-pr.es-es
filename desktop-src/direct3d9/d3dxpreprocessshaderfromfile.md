---
description: Preprocesa un archivo de sombreador sin realizar la compilación. Esto resuelve todas las \# definiciones e \# incluye, y proporciona un sombreador independiente para la compilación posterior.
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: Función D3DXPreprocessShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba9cf35418bbbe6fe4b39341031fd1e056b27dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362555"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a>D3DXPreprocessShaderFromFile función)

Preprocesa un archivo de sombreador sin realizar la compilación. Esto resuelve todas las \# definiciones e \# incluye, y proporciona un sombreador independiente para la compilación posterior.

> [!Note]  
> En lugar de usar esta función heredada, se recomienda usar la API de [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo del sombreador.

</dd> <dt>

*pDefines* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***

Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** . Este valor puede ser **null**.

</dd> <dt>

*pInclude* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include. Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.

</dd> <dt>

*ppShaderText* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una sola cadena grande que representa la secuencia de token con formato resultante.

</dd> <dt>

*ppErrorMsgs* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación. Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración. Este valor puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones del sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXPreprocessShader**](d3dxpreprocessshader.md)
</dt> <dt>

[**D3DXPreprocessShaderFromResource**](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
