---
title: Función Texture2DArray::GatherCmpRed(S,float,float,int2,int2,int2,int2)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente rojo con un valor de comparación. | Función Texture2DArray::GatherCmpRed(S,float,float,int2,int2,int2,int2)
ms.assetid: B436FB9A-C55C-477F-B8BE-933B1EB04AE1
keywords:
- Función GatherCmpRed HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93ee67c536934adb3187a5e224be0043167f9836e391d86556b8e76871563aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485875"
---
# <a name="texture2darraygathercmpredsfloatfloatint2int2int2int2-function"></a>Función Texture2DArray::GatherCmpRed(S,float,float,int2,int2,int2,int2)

Para cuatro valores de texel que se usarían en una operación de filtrado bi lineal, devuelve una comparación de su componente rojo con un valor de comparación.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherCmpRed(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Índice de sampler de base cero.

</dd> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **float**

Coordenadas de ejemplo (u,v).

</dd> <dt>

*CompareValue* \[ En\]
</dt> <dd>

Tipo: **float**

Valor que se compara con cada valor muestreado.

</dd> <dt>

*Offset1* \[ En\]
</dt> <dd>

Tipo: **int2**

Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset2* \[ En\]
</dt> <dd>

Tipo: **int2**

Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset3* \[ En\]
</dt> <dd>

Tipo: **int2**

Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset4* \[ En\]
</dt> <dd>

Tipo: **int2**

Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Comentarios

Las muestras de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherCmpRed](texture2darray-gathercmpred.md)
</dt> </dl>

 

 




