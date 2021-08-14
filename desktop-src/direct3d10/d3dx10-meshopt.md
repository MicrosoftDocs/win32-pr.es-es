---
description: 'D3DX10_MESHOPT enumeración : especifica el tipo de optimización de malla que se va a realizar.'
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: D3DX10_MESHOPT enumeración (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 193bf832f00c9812a515ae9b5c478f6baed637d87605e9f8d04349a12d79aac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989225"
---
# <a name="d3dx10_meshopt-enumeration"></a>Enumeración D3DX10 \_ MESHOPT

Especifica el tipo de optimización de malla que se va a realizar.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ COMPACT**
</dt> <dd>

Reordena las caras para quitar los vértices y las caras no usados.

</dd> <dt>

<span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ ATTR \_ SORT**
</dt> <dd>

Reordena las caras para optimizar para menos cambios de estado de agrupación de atributos y un rendimiento mejorado de DrawSubset.

</dd> <dt>

<span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10 \_ MESHOPT \_ VERTEX \_ CACHE**
</dt> <dd>

Reordena las caras para aumentar la tasa de aciertos de caché de las cachés de vértices.

</dd> <dt>

<span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**REORDENACIÓN DE \_ BANDAS DE MESHOPT \_ D3DX10 \_**
</dt> <dd>

Reordena las caras para maximizar la longitud de los triángulos adyacentes.

</dd> <dt>

<span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ IGNORE \_ VERTS**
</dt> <dd>

Optimizar solo las caras; no optimice los vértices.

</dd> <dt>

<span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ NO SE \_ \_ DIVIDE**
</dt> <dd>

Durante la ordenación de atributos, no divida los vértices que se comparten entre grupos de atributos.

</dd> <dt>

<span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ DEVICE \_ INDEPENDENT**
</dt> <dd>

Afecta al tamaño de la caché de vértices. Con esta marca se especifica un tamaño de caché de vértices predeterminado que funciona bien en hardware heredado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las marcas de optimización D3DXMESHOPT \_ STRIPREORDER y D3DXMESHOPT \_ VERTEXCACHE son mutuamente excluyentes.

La marca D3DXMESHOPT \_ SHAREVB se ha quitado de esta enumeración. Use D3DXMESH VB SHARE en su \_ \_ lugar, en D3DXMESH.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




