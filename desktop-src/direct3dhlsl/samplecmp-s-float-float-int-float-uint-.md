---
title: 'Función SampleCmp:: SampleCmp (S, Float, Float, int, Float, uint) para Texture2D'
description: Obtenga información sobre cómo esta función muestrea un Texture2D, con un valor de comparación para rechazar muestras, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. Devuelve el estado de la operación.
ms.assetid: 039EA69B-DFE0-4351-963A-C0326FDEF844
keywords:
- SampleCmp de función HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b4667594a4b4eeaf9e533338411b79810fee5eb
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987373"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture2d"></a>Función SampleCmp:: SampleCmp (S, Float, Float, int, Float, uint) para Texture2D

Muestrea un [**Texture2D**](sm5-object-texture2d.md), con un valor de comparación para rechazar ejemplos, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. Devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Un [Estado de muestra](dx-graphics-hlsl-sampler.md). Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.

</dd> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **float**

Las coordenadas de textura. El tipo de argumento depende del tipo de objeto de textura.



| Tipo de Texture-Object                    | Tipo de parámetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*CompareValue* \[ de\]
</dt> <dd>

Tipo: **float**

Un valor de punto flotante que se va a utilizar como valor de comparación.

</dd> <dt>

*Desplazamiento* \[ de\]
</dt> <dd>

Tipo: **int**

Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo. Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware. El tipo de argumento depende del tipo de objeto de textura. Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).



| Tipo de Texture-Object           | Tipo de parámetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | no admitido  |



 

</dd> <dt>

*Abrazadera* \[ de\]
</dt> <dd>

Tipo: **float**

Un valor opcional en el que se van a fijar los valores LOD de ejemplo. Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.

</dd> <dt>

*Estado* \[ de enuncia\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features). Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos SampleCmp](texture2d-samplecmp.md)
</dt> </dl>

 

 
