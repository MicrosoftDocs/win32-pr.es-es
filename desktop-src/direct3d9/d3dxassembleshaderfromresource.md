---
description: Ensamble un sombreador.
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: Función D3DXAssembleShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e748764eec94ea1f555c225c34680392610c9f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649455"
---
# <a name="d3dxassembleshaderfromresource-function"></a>D3DXAssembleShaderFromResource función)

Ensamble un sombreador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSrcModule* \[ de\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador de un módulo que contiene la descripción del efecto. Si este parámetro es **null**, se usará el módulo actual.

</dd> <dt>

*pSrcResource* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre del recurso. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR. Vea la sección Comentarios.

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

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de compilación identificadas por varias marcas. El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado. Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.

</dd> <dt>

*ppShader* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene el sombreador creado. Este búfer contiene el código del sombreador compilado, así como cualquier información de la tabla de símbolos y de depuración incrustada.

</dd> <dt>

*ppErrorMsgs* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación. Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración. Este valor puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXAssembleShaderFromResourceW. De lo contrario, la llamada de función se resuelve como D3DXAssembleShaderFromResourceA porque se usan cadenas ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones del sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXCompileShader**](d3dxcompileshader.md)
</dt> <dt>

[**D3DXCompileShaderFromResource**](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
