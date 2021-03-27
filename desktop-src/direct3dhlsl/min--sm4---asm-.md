---
title: min (SM4-ASM)
description: Valor Float mínimo de componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584aee077735b717bf76d148d4d0db4357a7d95
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104149005"
---
# <a name="min-sm4---asm"></a>min (SM4-ASM)

Valor Float mínimo de componente.



| min \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el resultado de la operación.<br/> *dest*  =  *src0*  <  *SRC1* ? *src0* : *SRC1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes que se van a comparar con *SRC1*.<br/>                                                  |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los componentes que se van a comparar con *src0*.<br/>                                                  |



 

## <a name="remarks"></a>Observaciones

>= se usa en lugar de > para que, si es min (x, y) = x, entonces Max (x, y) = y.

NaN tiene un tratamiento especial. Si un operando de origen es NaN, se devuelve el otro operando de origen y la elección se realiza por componente. Si ambos son NaN, se devuelve cualquier representación NaN. Esto se ajusta a las nuevas reglas de IEEE 754R.

Las desnormaciones se vacían, con el signo conservado, antes de la comparación. Sin embargo, el resultado que se escribe en *dest* puede o no ser de desnormalización.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produce desbordamiento o subdesbordamiento. F significa un número real finito.



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| **src0 SRC1->** | **-INF** | **F**        | **+ INF** | **NaN** |
| **-INF**           | -inf     | -inf         | -inf     | -inf    |
| **F**              | -inf     | src0 o SRC1 | src0     | src0    |
| **-INF**           | -inf     | src1         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

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

 

 





