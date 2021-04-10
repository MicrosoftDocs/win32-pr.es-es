---
description: Describe un parámetro utilizado para un objeto de efecto.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: D3DXPARAMETER_DESC estructura (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280243"
---
# <a name="d3dxparameter_desc-structure"></a>D3DXPARAMETER \_ DESC (estructura)

Describe un parámetro utilizado para un objeto de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre del parámetro.

</dd> <dt>

**Semántica**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Significado semántico, también denominado uso.

</dd> <dt>

**Clase**
</dt> <dd>

Type: **[ **\_ clase D3DXPARAMETER**](./d3dxparameter-class.md)**

</dd> <dd>

Clase de parámetro. Establézcalo en uno de los valores de la [**\_ clase D3DXPARAMETER**](./d3dxparameter-class.md).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_ Type**](./d3dxparameter-type.md)**

</dd> <dd>

Tipo de parámetro. Establézcalo en uno de los valores del [**\_ tipo D3DXPARAMETER**](./d3dxparameter-type.md).

</dd> <dt>

**Filas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de filas de la matriz.

</dd> <dt>

**Columnas**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de columnas de la matriz.

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de elementos de la matriz.

</dd> <dt>

**Anotaciones**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de anotaciones.

</dd> <dt>

**StructMembers**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de miembros de estructura.

</dd> <dt>

**Marcas**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Atributos de parámetro. Vea [constantes de efecto](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

**Bytes**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamaño del parámetro, en bytes.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
