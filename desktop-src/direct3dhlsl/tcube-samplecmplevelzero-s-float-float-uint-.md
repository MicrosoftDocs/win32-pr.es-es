---
title: Función SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) para TextureCube
description: Muestrea solo una textura en el nivel 0 de mapa mip y compara el resultado con un valor de comparación. Devuelve el estado de la operación. Para TextureCube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
keywords:
- Función HLSL de SampleCmpLevelZero
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5970b2a03a3004269b8ef758569aa6ac222bb60032dcb91e121a342e58cef886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117995"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a>Función SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) para TextureCube

Muestrea solo una textura en el nivel 0 de mapa mip y compara el resultado con un valor de comparación. Devuelve el estado de la operación.

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

Un [estado sampler](dx-graphics-hlsl-sampler.md). Se trata de un objeto declarado en un archivo de efecto que contiene asignaciones de estado.

</dd> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **float**

Las coordenadas de textura. El tipo de argumento depende del tipo texture-object.



| Texture-Object tipo                    | Tipo de parámetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*CompareValue* \[ En\]
</dt> <dd>

Tipo: **float**

Valor de punto flotante que se usará como valor de comparación.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se han tomado valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato de textura, que es uno de los valores con tipo enumerados [**en DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos SampleCmpLevelZero](texturecube-samplecmplevelzero.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
