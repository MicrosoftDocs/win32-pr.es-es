---
title: IMAX (SM4-ASM)
description: Entero de tipo de componente máximo.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc1bc6311573b1e7b39fbeaa93904203e7aae2ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148985"
---
# <a name="imax-sm4---asm"></a>IMAX (SM4-ASM)

Entero de tipo de componente máximo.



| IMAX dest \[ . Mask \] , \[  - \] src0 \[ . swizzle \] , \[ - \] SRC1 \[ . swizzle \] , |
|--------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el resultado de la operación.<br/> *dest*  =  *src0*  >  *SRC1* ? *src0* : *SRC1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el valor que se va a comparar con *SRC1*.<br/>                                                       |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] el valor que se va a comparar con *src0*.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

El modificador opcional Negate en los operandos de origen toma el complemento de 2 antes de realizar la operación.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





