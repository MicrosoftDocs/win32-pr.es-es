---
title: 'Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, uint) para TextureCube'
description: Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación. Devuelve el estado de la operación. Para TextureCube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
keywords:
- SampleCmpLevelZero de función HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff58c51919e575260c71f7b58d8f3d0fda6c1dd1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987318"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a>Función SampleCmpLevelZero:: SampleCmpLevelZero (S, Float, Float, uint) para TextureCube

Muestrea solo una textura en el nivel 0 del mipmap y compara el resultado con un valor de comparación. Devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

[Métodos SampleCmpLevelZero](texturecube-samplecmplevelzero.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
