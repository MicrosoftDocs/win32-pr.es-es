---
description: Describe la resolución de la sombra del búfer de z que se usará en la simulación de iluminación directa de Radiance Transfer (PRT) precalculada en la GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Enumeración D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718420"
---
# <a name="d3dxshgpusimopt-enumeration"></a>Enumeración D3DXSHGPUSIMOPT

Describe la resolución de la sombra del búfer de z que se usará en la simulación de iluminación directa de Radiance Transfer (PRT) precalculada en la GPU. También se puede especificar un búfer z de mayor calidad para reducir el ruido en los resultados de la simulación de iluminación directa, aunque la simulación será más lenta.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**
</dt> <dd>

Simulación de baja resolución. En la simulación se usa una textura de 256 x 256 píxeles para codificar la sombra del búfer de z.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**
</dt> <dd>

Simulación de resolución media. En la simulación se usa una textura de 512 x 512 píxeles para codificar la sombra del búfer de z. Este es el valor predeterminado.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**
</dt> <dd>

Simulación de alta resolución. En la simulación se usa una textura de 1024 x 1024 píxeles para codificar la sombra del búfer de z.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**
</dt> <dd>

Simulación de resolución más alta. En la simulación se usa una textura de 2048 x 2048 píxeles para codificar la sombra del búfer de z.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ highquality**
</dt> <dd>

La simulación es de alta precisión, independientemente de la resolución seleccionada. Si se establece este valor, se reducirá el ruido de los resultados de la simulación de iluminación directa, aunque la simulación será más lenta. Puede combinarse con uno de los valores de resolución.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Solo se puede especificar uno de los valores de resolución y se puede combinar con el valor de alta calidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




