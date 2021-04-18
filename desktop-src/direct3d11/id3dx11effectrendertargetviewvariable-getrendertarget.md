---
title: Método ID3DX11EffectRenderTargetViewVariable GetRenderTarget (D3dx11effect. h)
description: Obtiene un destino de representación.
ms.assetid: 96984d0a-b8f4-444a-9683-3c37d8274d75
keywords:
- Método GetRenderTarget Direct3D 11
- Método GetRenderTarget Direct3D 11, interfaz ID3DX11EffectRenderTargetViewVariable
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11, método GetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa86dd3a5c950e18ae97ba1987ee0f44b9f658c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998731"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertarget-method"></a>ID3DX11EffectRenderTargetViewVariable:: GetRenderTarget (método)

Obtiene un destino de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRenderTarget(
   ID3D11RenderTargetView **ppResource
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppResource* 
</dt> <dd>

Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***

Dirección de un puntero a una interfaz de vista de destino de representación. Vea [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





