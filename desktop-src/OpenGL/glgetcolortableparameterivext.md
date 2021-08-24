---
title: Función glGetColorTableParameterivEXT (Gl.h)
description: Las funciones glGetColorTableParameterfvEXT y glGetColorTableParameterivEXT obtienen parámetros de paleta de tablas de colores. | Función glGetColorTableParameterivEXT (Gl.h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- Función GlGetColorTableParameterivEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc45217d420aab9c5db3b1ceb416c369b5fb948df2911ea20e6e174eeed0649f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742044"
---
# <a name="glgetcolortableparameterivext-function"></a>Función glGetColorTableParameterivEXT

Las [**funciones glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) y **glGetColorTableParameterivEXT** obtienen parámetros de paleta de tablas de colores.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Textura de destino de la paleta para la que desea datos de parámetros. Debe ser TEXTURE \_ 1D, TEXTURE \_ 2D, PROXY \_ TEXTURE \_ 1D o PROXY \_ TEXTURE \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Constante simbólica para el tipo de datos de parámetros de paleta a los que *apuntan los parámetros*.

Las siguientes son las constantes simbólicas aceptadas y sus significados.



| Value                                                                                                                                                                                                             | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ FORMAT \_ EXT**</dt> </dl>              | Devuelve el formato interno especificado por la llamada más reciente [**a glColorTableEXT**](glcolortableext.md) o el valor predeterminado.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ WIDTH \_ EXT**</dt> </dl>                 | Devuelve el ancho de la paleta actual.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ RED \_ SIZE \_ EXT**</dt> </dl>       | Devuelve el tamaño real usado internamente para almacenar el componente rojo de los datos de la paleta.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ GREEN \_ SIZE \_ EXT**</dt> </dl> | Devuelve el tamaño real usado internamente para almacenar el componente verde de los datos de la paleta.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ BLUE \_ SIZE \_ EXT**</dt> </dl>    | Devuelve el tamaño real usado internamente para almacenar el componente azul de los datos de la paleta.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ ALPHA \_ SIZE \_ EXT**</dt> </dl> | Devuelve el tamaño real usado internamente para almacenar el componente alfa de los datos de la paleta.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Apunta a los datos de parámetros de tabla de colores especificados por el *parámetro pname.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use las funciones **glGetColorTableParameterivEXT** y [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para recuperar datos de parámetros específicos de tablas de colores establecidas [**con glColorTableEXT**](glcolortableext.md) para las paletas de texturas de destino. También puede usar estas funciones para determinar el número de entradas de tabla de colores que **devuelve glGetColorTableEXT.**

Cuando  el parámetro de destino es GL PROXY TEXTURE 1D o GL PROXY TEXTURE 2D, y la implementación no admite los valores especificados para formato o \_ \_ \_ \_ \_ \_ ancho, **glColorTableEXT**  puede no crear la tabla de colores solicitada. En este caso, la tabla de colores está vacía y todos los parámetros recuperados serán cero. Puede determinar si OpenGL admite un tamaño y formato de tabla de colores determinados llamando a **glColorTableEXT con** un destino de proxy y, a continuación, llamando a **glGetColorTableParameterivEXT** o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) para determinar si el parámetro width coincide con el establecido por **glColorTableEXT.** Si el ancho recuperado es cero, se ha producido un error en la solicitud de tabla de colores **de glColorTable.** Si el ancho recuperado no es cero, puede llamar a **glColorTable** con el destino real con TEXTURE 1D o TEXTURE 2D para establecer \_ \_ la tabla de colores.

Las **funciones glGetColorTableParameterivEXT** y [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) son funciones de extensión que no forman parte de la biblioteca OpenGL estándar, pero forman parte de la extensión de textura con paleta \_ GL \_ \_ EXT. Para comprobar si la implementación de OpenGL admite **glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT,** llame [**a glGetString**](glgetstring.md)**(GL** \_ EXTENSIONS **)**. Si devuelve la textura de paleta \_ GL \_ \_ EXT, **se admiten glGetColorTableParameterivEXT** y **glGetColorTableParameterfvEXT.** Para obtener la dirección de función de una función de extensión, llame [**a wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





