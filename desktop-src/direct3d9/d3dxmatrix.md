---
description: Matriz 4x4 que contiene métodos y sobrecargas de operador.
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: Estructura D3DXMATRIX (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 2b09691ff27307e041a79b57e9d32c7e74e5eef1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707838"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a>Estructura D3DXMATRIX (D3dx9math. h)

Matriz 4x4 que contiene métodos y sobrecargas de operador.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_ij**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

El componente (i, j) de la matriz, donde i es el número de fila y j es el número de columna. Por ejemplo, \_ 34 significa lo mismo que \[ ₃ ₄ \] , el componente de la tercera fila y la cuarta columna.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los programadores de C no pueden usar la estructura D3DXMATRIX, deben usar la estructura [**D3DMATRIX**](d3dmatrix.md) . Los programadores de C++ pueden aprovechar las ventajas de los constructores sobrecargados y los operadores de asignación, unario y binario (incluida la igualdad).

En D3DX, el \_ elemento 34 de una matriz de proyección no puede ser un número negativo. Si su aplicación necesita usar un valor negativo en esta ubicación, debe escalar toda la matriz de proyección en-1 en su lugar.

### <a name="d3dxmatrix-extensions"></a>Extensiones de D3DXMATRIX

**D3DXMATRIX** tiene las siguientes extensiones de C++.


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DMATRIX**](d3dmatrix.md)
</dt> </dl>

 

 
