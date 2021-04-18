---
description: Obtiene el número de vértices a los que afecta un hueso determinado.
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: 'ID3DX10SkinInfo:: GetBoneInfluenceCount (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718231"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a>ID3DX10SkinInfo:: GetBoneInfluenceCount (método)

Obtiene el número de vértices a los que afecta un hueso determinado.

## <a name="syntax"></a>Sintaxis


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BoneIndex* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice que especifica un hueso existente. Debe estar comprendido entre 0 y el valor devuelto por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
