---
description: 'Una aplicación implementa esta interfaz para controlar las devoluciones de llamada en conjuntos de animación generados por llamadas a ID3DXAnimationController:: AdvanceTime.'
ms.assetid: 5a24ac96-2e68-49c0-acf6-8715d87b202d
title: Interfaz ID3DXAnimationCallbackHandler (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb3b58c58c6a0bd71924fb207170a177797b9f84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698389"
---
# <a name="id3dxanimationcallbackhandler-interface"></a>Interfaz ID3DXAnimationCallbackHandler

Una aplicación implementa esta interfaz para controlar las devoluciones de llamada en conjuntos de animación generados por llamadas a [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="members"></a>Miembros

La interfaz **ID3DXAnimationCallbackHandler** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationCallbackHandler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXAnimationCallbackHandler** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HandleCallback**](id3dxanimationcallbackhandler--handlecallback.md) | La aplicación implementa este método. Se llama a este método cuando se produce una devolución de llamada para un conjunto de animaciones en una de las pistas durante una llamada a [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).<br/> |



 

## <a name="remarks"></a>Observaciones

El tipo LPD3DXANIMATIONCALLBACKHANDLER se define como un puntero a esta interfaz.


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
