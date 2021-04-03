---
title: función glTexCoord4s (GL. h)
description: Establece las coordenadas de textura actuales. | función glTexCoord4s (GL. h)
ms.assetid: 948c63f5-a94d-4e55-9aa4-a320452fc29f
keywords:
- glTexCoord4s (función) OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a164b091c62b31523baa5be96d1578e1cbfa80
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914573"
---
# <a name="gltexcoord4s-function"></a>glTexCoord4s función)

Establece las coordenadas de textura actuales.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexCoord4s(
   GLshort s,
   GLshort t,
   GLshort r,
   GLshort q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* 
</dt> <dd>

Coordenada de textura s.

</dd> <dt>

*t* 
</dt> <dd>

Coordenada de textura de t.

</dd> <dt>

*r* 
</dt> <dd>

Coordenada de textura de r.

</dd> <dt>

*respuestas* 
</dt> <dd>

Coordenada de textura q.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función [**glTexCoord**](gltexcoord-functions.md) establece las coordenadas de textura actuales que forman parte de los datos asociados a los vértices del polígono. La función **glTexCoord** especifica coordenadas de textura en una, dos, tres o cuatro dimensiones. La función glTexCoord1 establece las coordenadas de textura actuales en (s, 0, 0, 1); una llamada a glTexCoord2 lo establece en (s, t, 0, 1). Del mismo modo, glTexCoord3 especifica las coordenadas de textura como (s, t, r, 1) y glTexCoord4 define los cuatro componentes explícitamente como (s, t, r, q). Puede actualizar las coordenadas de textura actuales en cualquier momento. En concreto, puede llamar a glTexCoord entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md). La siguiente función recupera información relacionada con **glTexCoord**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ coordenadas de \_ textura \_ actual de GL

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





