---
title: atomic_iadd (sm5 - asm)
description: Entero atómico que se agrega a la memoria.
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d582cdb4951cecc845cb868e7eee64be61b8f2d7387a0548c43e094cf308226f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287758"
---
# <a name="atomic_iadd-sm5---asm"></a>atomic \_ iadd (sm5 - asm)

Entero atómico que se agrega a la memoria.



| atomic \_ iadd dst, dstAddress \[ .swzzle, \] src0 \[ .select \_ component\] |
|----------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[en \] Componentes que se agregarán con *src0*. Este valor debe ser una vista de acceso no ordenado (UAV) (u \# ). En el sombreador de proceso también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] La dirección de memoria.<br/>                                                                                                                                                 |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] Componentes que se agregarán a *dst*.<br/>                                                                                                                                     |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza una adición de entero de 32 bits de componente único de operando *src0* a *dst* a 32 bits por dirección de componente *dstAddress,* realizada de forma atómica. Esta instrucción no es sensible a la firma.

El número de componentes tomados de la dirección viene determinado por la dimensionalidad *de dst* u \# o g \# .

Si *dst* es un u \# , se puede declarar como sin formato, con tipo o estructurado. Si se escribe, se debe declarar como UINT/SINT con el formato de recurso enlazado R32 \_ \_ UINT/SINT.

Si *dst* es g \# , debe declararse como sin formato o estructurado.

No se devuelve nada al sombreador.

Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel o muestra para servir como asistente de un píxel o muestra real para derivados, esta instrucción no modifica la memoria *dst* en absoluto (silenciosamente).

El direccionamiento fuera de los límites en u hace que no se escriba nada en la memoria, excepto si la u está estructurada y el desplazamiento de bytes en la estructura (segundo componente de la dirección) está causando el acceso fuera de los límites, todo el contenido del UAV se vuelve \# \# indefinido.

El direccionamiento fuera de límites en g (los límites de ese g determinado, en lugar de toda la memoria compartida) hace que todo el contenido de toda la memoria compartida se vuelva \# \# indefinido.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible. |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





