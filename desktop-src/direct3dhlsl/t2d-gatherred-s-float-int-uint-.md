---
title: 'Texture2D:: GatherRed (S, Float, int, uint) (función)'
description: 'Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos. | Texture2D:: GatherRed (S, Float, int, uint) (función)'
ms.assetid: B49F738F-FB5C-4004-A3F3-D87C566DB597
keywords:
- GatherRed de función HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3381bb6f7388b418e22431575b9a8431ed410b2f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998165"
---
# <a name="texture2dgatherredsfloatintuint-function"></a>Texture2D:: GatherRed (S, Float, int, uint) (función)

Devuelve los componentes rojo de los cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, junto con el estado de asignación de mosaicos.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherRed(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Índice de muestra de base cero.

</dd> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **float**

Coordenadas de ejemplo (u, v).

</dd> <dt>

*Desplazamiento* \[ de\]
</dt> <dd>

Tipo: **int**

Desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Estado* \[ de enuncia\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features). Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Observaciones

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherRed](texture2d-gatherred.md)
</dt> </dl>

 

 
