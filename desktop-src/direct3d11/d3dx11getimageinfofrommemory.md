---
title: Función D3DX11GetImageInfoFromMemory (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, GetMetadataFromXXXMemory (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos). Obtenga información sobre una imagen ya cargada en la memoria.
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- Función D3DX11GetImageInfoFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64db94fd0827e1168c599c3a4b959da097faaf43231943d323a19917e18a8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124710"
---
# <a name="d3dx11getimageinfofrommemory-function"></a>Función D3DX11GetImageInfoFromMemory

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex,](https://github.com/Microsoft/DirectXTex) **GetMetadataFromXXXMemory** (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos).

 

Obtenga información sobre una imagen ya cargada en la memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Puntero a la imagen en memoria.

</dd> <dt>

*SrcDataSize* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Tamaño de la imagen en memoria, en bytes.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Bomba de subproceso opcional que se puede usar para cargar la información de forma asincrónica. Puede ser **NULL.** Vea [**Id3DX11ThreadPump (interfaz).**](id3dx11threadpump.md)

</dd> <dt>

*pSrcInfo* \[ En\]
</dt> <dd>

Tipo: **[ **INFORMACIÓN DE \_ IMAGEN \_ D3DX11**](d3dx11-image-info.md)\***

Información sobre la imagen en memoria.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.** Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

