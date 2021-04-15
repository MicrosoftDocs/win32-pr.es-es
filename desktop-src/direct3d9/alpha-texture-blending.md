---
description: El motor de iluminación combina la información sobre el color, el color del vértice y la iluminación para generar un color por vértice.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Combinación de texturas alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677229"
---
# <a name="alpha-texture-blending-direct3d-9"></a>Combinación de texturas alfa (Direct3D 9)

El motor de iluminación combina la información sobre el color, el color del vértice y la iluminación para generar un color por vértice. Una vez interpolado, esto genera un color por píxel que se escribe en el búfer de fotogramas. Si una aplicación habilita la combinación de texturas, el color del píxel se convertirá en una combinación del píxel actual en el búfer de fotogramas y un color de textura.

Esta fórmula determina el color final de los píxeles combinados:


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



Donde:

-   Color es el color de los píxeles de salida.
-   TexelColor es el color de entrada después del filtrado de textura.
-   SourceBlend es el porcentaje del color final del píxel que se compone del color de textura de origen.
-   CurrentPixelColor es el color del píxel actual.
-   DestBlend es el porcentaje del color final del píxel que se compone del color del píxel actual.

La ecuación de combinación final se establece llamando a [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) y especificando el estado de representación de Blend (D3DRS \_ BLENDXXX) con un factor de mezcla correspondiente ([**D3DBLEND**](./d3dblend.md)). Los valores de SourceBlend y DestBlend oscilan entre 0,0 (transparente) y 1,0 (opaco), ambos incluidos. Además, una aplicación puede controlar la transparencia de un píxel estableciendo el valor alfa en una textura. En este caso, use lo siguiente:


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



La ecuación de fusión hará que el píxel representado sea transparente. Los valores predeterminados son:


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de texturas](texture-blending.md)
</dt> <dt>

[Filtrado de texturas (Direct3D 9)](texture-filtering.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
