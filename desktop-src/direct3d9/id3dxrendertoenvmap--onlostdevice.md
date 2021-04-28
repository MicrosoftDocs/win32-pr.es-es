---
description: 'Método ID3DXRenderToEnvMap::OnLostDevice: use este método para liberar todas las referencias a recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.'
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: Método ID3DXRenderToEnvMap::OnLostDevice (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88f27c259262eb7abb57246e547ad66866bb3dcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107203"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a>Método ID3DXRenderToEnvMap::OnLostDevice

Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9::Reset**](/windows/desktop/api). Incluso si el dispositivo no se perdió realmente, **ID3DXRenderToEnvMap::OnLostDevice** es responsable de liberar los bloques de estado y otros recursos que es posible que deba liberar antes de restablecer el dispositivo. Como resultado, el objeto de fuente no se puede usar de nuevo antes de llamar a **IDirect3DDevice9::Reset** y, a continuación, [**ID3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




