---
title: Función InterlockedAnd (referencia hlsl)
description: Realiza un atómico garantizado y .
ms.assetid: 7dc5185a-ea37-493d-975d-dbb803c886d3
keywords:
- Función HlSL de InterlockedAnd
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b058b5d235e04761c24ace1d6f1bb5cca1187f01d8fe0eb1a9d0178c036bf5f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511335"
---
# <a name="interlockedand-function-hlsl-reference"></a>Función InterlockedAnd (referencia hlsl)

Realiza un atómico garantizado y .

## <a name="syntax"></a>Sintaxis

``` syntax
void InterlockedAnd(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*dest* \[ En\]
</dt> <dd>

Tipo: **R**

Dirección de destino.

</dd> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **T**

Valor de entrada.

</dd> <dt>

*valor \_ de salida* \[ original\]
</dt> <dd>

Tipo: **T**

Opcional. Valor de entrada original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta operación solo se puede realizar en recursos con tipo int o uint y variables de memoria compartida. Hay dos usos posibles para esta función. La primera es cuando R es un tipo de variable de memoria compartida. En este caso, la función realiza un atómico y de valor en el registro de memoria compartida al que hace referencia dest. El segundo escenario es cuando R es un tipo de variable de recurso. En este escenario, la función realiza una operación atómica y de valor en la ubicación del recurso a la que hace referencia dest. La función sobrecargada tiene una variable de salida adicional que se establecerá en el valor original de dest. Esta operación sobrecargada solo está disponible cuando R es legible y grabable.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




