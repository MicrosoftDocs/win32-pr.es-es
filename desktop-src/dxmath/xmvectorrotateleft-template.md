---
description: Gira el vector a la izquierda un número determinado de elementos de 32 bits.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Plantilla XMVectorRotateLeft (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649896"
---
# <a name="xmvectorrotateleft-template"></a>Plantilla XMVectorRotateLeft

Gira el vector a la izquierda un número determinado de elementos de 32 bits.

## <a name="syntax"></a>Sintaxis

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[en \] vector para girar a la izquierda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**XMVECTOR**](xmvector-data-type.md)girado.

## <a name="remarks"></a>Observaciones

Esta función es una versión de plantilla de [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , donde el argumento *Elements* es un valor de plantilla.

> [!Note]  
> La `XMVectorRotateLeft` plantilla es nueva para DirectXMath y no está disponible para XNAMath 2. x.

 

**Espacio de nombres**: usar DirectX

### <a name="platform-requirements"></a>Requisitos de la plataforma

Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con el Windows SDK para Windows 8. Se admite para aplicaciones de escritorio de Win32, aplicaciones de la tienda Windows y Windows Phone 8 aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de plantilla de la biblioteca de DirectXMath](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
