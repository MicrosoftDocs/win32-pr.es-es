---
title: Interfaz ID3DX11EffectGroup (D3dx11effect. h)
description: La interfaz ID3DX11EffectGroup obtiene acceso a un grupo de efectos. La duración de un objeto ID3DX11EffectGroup es igual a la duración de su objeto ID3DX11Effect primario.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interfaz ID3DX11EffectGroup Direct3D 11
- Interfaz ID3DX11EffectGroup Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986953"
---
# <a name="id3dx11effectgroup-interface"></a>Interfaz ID3DX11EffectGroup

La interfaz **ID3DX11EffectGroup** obtiene acceso a un grupo de efectos.

La duración de un objeto **ID3DX11EffectGroup** es igual a la duración de su objeto [**ID3DX11Effect**](id3dx11effect.md) primario.

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11EffectGroup** tiene estos métodos.



| Método                                                                  | Descripción                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetAnnotationByIndex**](id3dx11effectgroup-getannotationbyindex.md) | Obtiene una anotación por índice.<br/>                        |
| [**GetAnnotationByName**](id3dx11effectgroup-getannotationbyname.md)   | Obtiene una anotación por nombre.<br/>                         |
| [**GetDesc**](id3dx11effectgroup-getdesc.md)                           | Obtiene una descripción del grupo.<br/>                          |
| [**GetTechniqueByIndex**](id3dx11effectgroup-gettechniquebyindex.md)   | Obtiene una técnica por índice.<br/>                          |
| [**GetTechniqueByName**](id3dx11effectgroup-gettechniquebyname.md)     | Obtener una técnica por nombre.<br/>                           |
| [**IsValid**](id3dx11effectgroup-isvalid.md)                           | Pruebe un efecto para ver si contiene una sintaxis válida.<br/> |



 

## <a name="remarks"></a>Observaciones

Para obtener una interfaz **ID3DX11EffectGroup** , llame a un método como [**ID3DX11Effect:: GetGroupByName**](id3dx11effect-getgroupbyname.md).

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





