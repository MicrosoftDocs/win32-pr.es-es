---
title: ISHR (SM5-ASM)
description: Desplazamiento aritmético a la derecha (signo de extensión). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998244"
---
# <a name="ishr-sm5---asm"></a>ISHR (SM5-ASM)

Desplazamiento aritmético a la derecha (signo de extensión).



| ishl dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\] |
|--------------------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] contiene los resultados del desplazamiento.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el número de bits que se va a desplazar.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los valores de 32 bits que se van a desplazar.<br/>        |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un cambio aritmético de modo de componente de cada valor de 32 bits de *src0* a la derecha por un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) en *SRC1*, replicando el valor de bit 31. El resultado de 32 bits por componente se coloca en el *destino*.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





