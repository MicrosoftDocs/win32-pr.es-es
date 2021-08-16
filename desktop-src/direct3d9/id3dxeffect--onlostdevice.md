---
description: 'Método ID3DXEffect::OnLostDevice: use este método para liberar todas las referencias a recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.'
ms.assetid: f56925d8-17f7-44c5-a371-3cde41804613
title: Método ID3DXEffect::OnLostDevice (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnLostDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d198cb06461fc377933f2dc90c1e3fb687559ef7b83cc7becd9f04bdf1b78d1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521221"
---
# <a name="id3dxeffectonlostdevice-method"></a>Método ID3DXEffect::OnLostDevice

Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Se debe llamar a este método siempre que se pierda el dispositivo o antes de que el usuario llame a [**IDirect3DDevice9::Reset**](/windows/desktop/api). Aunque el dispositivo no se haya perdido realmente, **ID3DXEffect::OnLostDevice** es responsable de liberar los bloques de estado y otros recursos que es posible que deba liberar antes de restablecer el dispositivo. Como resultado, el objeto de fuente no se puede usar de nuevo antes de llamar a **IDirect3DDevice9::Reset** y, a continuación, [**ID3DXEffect::OnResetDevice**](id3dxeffect--onresetdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




