---
title: Función glGetMapfv (Gl.h)
description: Las funciones glGetMapdv, glGetMapfv y glGetMapiv devuelven parámetros del evaluador. | Función glGetMapfv (Gl.h)
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- Función glGetMapfv OpenGL
topic_type:
- apiref
api_name:
- glGetMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1bedb1b5ff07b7331eb740c46392e80ad324c6cef7f843978d9a5a41edf8da1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741595"
---
# <a name="glgetmapfv-function"></a>Función glGetMapfv

Las [**funciones glGetMapdv**](glgetmapdv.md), **glGetMapfv y** [**glGetMapiv**](glgetmapiv.md) devuelven parámetros del evaluador.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetMapfv(
   GLenum  target,
   GLenum  query,
   GLfloat *v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Nombre simbólico de un mapa. Los siguientes son valores aceptados: GL \_ MAP1 \_ COLOR \_ 4, GL \_ MAP1 \_ INDEX, GL \_ MAP1 \_ NORMAL, GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL MAP1 TEXTURE \_ \_ \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP1 VERTEX \_ \_ 3, GL \_ MAP1 VERTEX \_ \_ 4, \_ GL \_ MAP2 COLOR \_ 4, GL \_ MAP2 \_ INDEX, GL \_ MAP2 \_ NORMAL, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 VERTEX 3 Y GL \_ \_ \_ MAP2 VERTEX \_ \_ 4.

</dd> <dt>

*consulta* 
</dt> <dd>

Especifica qué parámetro se va a devolver. Se aceptan los siguientes nombres simbólicos.



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**GL \_ COEFF**</dt> </dl>    | El *parámetro v* devuelve los puntos de control para la función del evaluador. Los evaluadores unidimensionales *devuelven* puntos de control de orden y los evaluadores bidimensionales devuelven puntos de control *uorder* *x* *vorder.* Cada punto de control consta de uno, dos, tres o cuatro valores enteros, de punto flotante de precisión sencilla o de punto flotante de precisión doble, según el tipo del evaluador. Los puntos de control bidimensionales se devuelven en orden de fila principal, lo que incrementa rápidamente el índice *uorder* y el índice *de vorder* después de cada fila. Los valores enteros, cuando se solicitan, se calculan redondeando los valores de punto flotante internos a los valores enteros más cercanos.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**PEDIDO \_ DE GL**</dt> </dl>    | El *parámetro v* devuelve el orden de la función del evaluador. Los evaluadores unidimensionales devuelven un valor único, *order*. Los evaluadores bidimensionales devuelven dos valores, *uorder* y *vorder*.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**DOMINIO \_ GL**</dt> </dl> | El *parámetro v* devuelve los parámetros de asignación *U* y *v* lineales. Los evaluadores unidimensionales devuelven dos valores, *u* 1 y *u* 2, tal y como especifica [**glMap1**](glmap1.md). Los evaluadores bidimensionales devuelven cuatro valores *(u1,* *u2,* *v1* y *v2),* tal y como especifica [**glMap2**](glmap2.md). Los valores enteros, cuando se solicitan, se calculan redondeando los valores de punto flotante internos a los valores enteros más cercanos.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*V* 
</dt> <dd>

Devuelve los datos solicitados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target* o *query* no era un valor aceptado.<br/>                                                                             |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glGetMap** devuelve parámetros del evaluador. (Las **funciones glMap1** **y glMap2** definen evaluadores). El *parámetro* de destino especifica una asignación, *la consulta* selecciona un parámetro específico y *v* apunta al almacenamiento donde se devolverán los valores.

Los valores aceptables para el *parámetro de* destino se describen [**en glMap1**](glmap1.md) y [**glMap2.**](glmap2.md)

Si se genera un error, no se realiza ningún cambio en el contenido de *v*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





