---
title: función glGetColorTableEXT (GL. h)
description: La función glGetColorTableEXT obtiene los datos de la tabla de colores de la paleta de texturas de destino actual.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- glGetColorTableEXT (función) OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686250"
---
# <a name="glgetcolortableext-function"></a>glGetColorTableEXT función)

La función **glGetColorTableEXT** obtiene los datos de la tabla de colores de la paleta de texturas de destino actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de destino que va a cambiar su paleta. Debe ser \_ de textura 1D o textura \_ 2D.

</dd> <dt>

*format* 
</dt> <dd>

Formato de los datos de píxeles. Se aceptan las siguientes constantes simbólicas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>Cada píxel es un grupo de cuatro componentes en el siguiente orden: rojo, verde, azul, alfa. El formato RGBA se determina de esta manera: <br/>
<ol>
<li>La función <strong>glGetColorTableEXT</strong> convierte los valores de punto flotante directamente a un formato interno con una precisión no especificada. Los valores enteros con signo se asignan linealmente al formato interno, de modo que el valor entero representable más positivo se asigna a 1,0 y el valor entero representable más negativo se asigna a-1,0. Los datos enteros sin signo se asignan de forma similar: el valor entero más grande se asigna a 1,0 y cero se asigna a 0,0.</li>
<li>La función <strong>glGetColorTableEXT</strong> multiplica los valores de color resultantes por GL_c_SCALE y los agrega a GL_c_BIAS, donde <em>c</em> es rojo, verde, azul y alfa para los componentes de color respectivos. Los resultados se fijan en el intervalo [0, 1].</li>
<li>Si GL_MAP_COLOR es <strong>true</strong>, <strong>glGetColorTableEXT</strong> escala cada componente de color por el tamaño de la tabla de búsqueda GL_PIXEL_MAP_c_TO_c y, a continuación, reemplaza el componente por el valor al que hace referencia en esa tabla; <em>c</em> es R, G, B o A, respectivamente.</li>
<li>La función <strong>glGetColorTableEXT</strong> convierte los colores RGBA resultantes en fragmentos adjuntando las coordenadas z y de textura de la posición de la trama actual a cada píxel y asignando las coordenadas de la ventana <em>x</em> e <em>y</em> al fragmento <em>n</em>, tal que <em>x</em>? = <em>ancho</em> <em>x</em><sub>r</sub> + <em>n</em> mod<br/> ¿ <em>y</em>? = <em></em><sub></sub> + <em>n/ancho</em> de r<br/> donde (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) es la posición de la trama actual.<br/></li>
<li>Estos fragmentos de píxeles se tratan a continuación como los fragmentos generados mediante la rasterización de puntos, líneas o polígonos. La función <strong>glGetColorTableEXT</strong> aplica la asignación de texturas, la niebla y todas las operaciones de fragmento antes de escribir los fragmentos en el fotogramas.</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>Cada píxel es un único componente rojo.<br/> La función <strong>glGetColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente rojo de un píxel RGBA es, lo convierte en un píxel RGBA con el verde y el azul establecidos en 0,0 y el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>Cada píxel es un único componente verde.<br/> La función <strong>glGetColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente verde de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con el rojo y el azul establecidos en 0,0 y el alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>Cada píxel es un único componente azul.<br/> La función <strong>glGetColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente azul de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo y verde establecido en 0,0 y el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>Cada píxel es un único componente alfa.<br/> La función <strong>glGetColorTableEXT</strong> convierte este componente al formato interno de la misma manera que el componente alfa de un píxel RGBA es y, a continuación, lo convierte en un píxel RGBA con rojo, verde y azul establecido en 0,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>Cada píxel es un grupo de tres componentes en este orden: rojo, verde, azul.<br/> La función <strong>glGetColorTableEXT</strong> convierte cada componente al formato interno de la misma manera que los componentes rojo, verde y azul de un píxel RGBA. El color triple se convierte en un píxel RGBA con el valor alfa establecido en 1,0. Después de esta conversión, el píxel se trata como si se hubiera leído como un píxel RGBA.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>Cada píxel es un grupo de tres componentes en este orden: azul, verde, rojo.<br/> GL_BGR_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Microsoft Windows. Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>Cada píxel es un grupo de cuatro componentes en este orden: azul, verde, rojo y alfa.<br/> GL_BGRA_EXT proporciona un formato que coincide con el diseño de memoria de los mapas de bits independientes del dispositivo (DIB) de Windows. Por lo tanto, las aplicaciones pueden usar los mismos datos con llamadas de función de Windows y llamadas de función de píxeles de OpenGL.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

El tipo de datos para los *datos*. A continuación se indican las constantes simbólicas aceptadas y su significado.



| Value                                                                                                                                                                      | Significado                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**\_byte sin signo de \_ GL**</dt> </dl>    | Entero de 8 bits sin signo<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**BYTE de GL \_**</dt> </dl>                                | Entero de 8 bits con signo<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**libro de contabilidad \_ corto sin signo \_**</dt> </dl> | Entero de 16 bits sin signo<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**CONTABILIDAD \_ breve**</dt> </dl>                             | Entero de 16 bits con signo<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**libro de contabilidad \_ sin signo \_**</dt> </dl>       | Entero de 32 bits sin signo<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ int**</dt> </dl>                                   | Entero de 32 bits<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**valor \_ float de GL**</dt> </dl>                             | Valor de punto flotante de precisión sencilla<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

Apunta a la ubicación donde se va a almacenar la información de la tabla de colores devuelta. Cada entrada de la tabla de colores se almacena como si fuera un solo píxel de una textura 1D. Dado que todas las texturas tienen una paleta predeterminada, **glGetColorTableEXT** siempre devuelve la información de la paleta aunque los datos de la textura no estén en un formato de paleta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *destino*, *formato* o *tipo* no era un valor aceptado.<br/>                                                                   |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glGetColorTableEXT** obtiene los datos de la tabla de colores reales especificados por [**glColorTableEXT**](glcolortableext.md) y [**glColorSubTableEXT**](glcolorsubtableext.md).

La función **glGetColorTableEXT** es una función de extensión que no forma parte de la biblioteca estándar de OpenGL, pero que forma parte de la extensión de textura de la paleta de GL \_ ext \_ \_ . Para comprobar si la implementación de OpenGL es compatible con **glGetColorTableEXT**, llame a [**glGetString**](glgetstring.md)(extensiones de GL \_ ). Si devuelve la \_ \_ textura de paleta ext \_ de GL, se admite **glGetColorTableEXT** . Para obtener la dirección de la función de una función de extensión, llame a [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                            |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





