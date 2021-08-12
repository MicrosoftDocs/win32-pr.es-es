---
description: 'Método ID3DX10Mesh::GetAttributeTable: recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.'
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: Método ID3DX10Mesh::GetAttributeTable (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce1f2464882bfdece8997aeea23f2bb42c276b3f6ce49b13cb242d517a522250
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540295"
---
# <a name="id3dx10meshgetattributetable-method"></a>Método ID3DX10Mesh::GetAttributeTable

Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAttribTable* \[ En\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md)\***

Puntero a una matriz de estructuras D3DX10 ATTRIBUTE RANGE, que representan las entradas de la \_ tabla de atributos de la \_ malla. Especifique **NULL** para recuperar el valor de pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero al número de entradas almacenadas en pAttribTable o un valor que se va a rellenar con el número de entradas almacenadas en la tabla de atributos para la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otros. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado al dibujar el marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
