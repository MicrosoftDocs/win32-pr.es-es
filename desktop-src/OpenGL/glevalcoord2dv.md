---
title: Función glEvalCoord2dv (Gl.h)
description: La función glEvalCoord2dv evalúa los mapas bidimensionales habilitados.
ms.assetid: 726a0c0c-d69e-46dc-b78e-a0d1e9ad97cd
keywords:
- Función GlEvalCoord2dv OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72a81fc0892a9d72d3991884dd472b89458beed2e64d8dd986cbebb3cfee865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625645"
---
# <a name="glevalcoord2dv-function"></a>Función glEvalCoord2dv

La **función glEvalCoord2dv** evalúa los mapas bidimensionales habilitados.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEvalCoord2dv(
   const GLdouble *u
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*u* 
</dt> <dd>

Puntero a una matriz que contiene la coordenada de *dominio u*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función glEvalCoord2dv** evalúa los mapas bidimensionales habilitados mediante dos valores de dominio, *u* y *v*. Defina mapas con [**glMap1.**](glmap1.md) Habilite o deshabilite con [**glEnable**](glenable.md) [**y glDisable**](gldisable.md).

Cuando se emite una de las funciones **glEvalCoord,** se evalúan todos los mapas habilitados actualmente de la dimensión indicada. A continuación, para cada asignación habilitada, es como si la función OpenGL correspondiente se emitiese con el valor calculado. Es decir, si GL \_ MAP1 \_ INDEX o GL \_ MAP2 INDEX están \_ habilitados, se simula una función [**glIndex.**](glindex-functions.md) Si GL \_ MAP1 \_ COLOR \_ 4 o GL \_ MAP2 \_ COLOR \_ 4 están habilitados, se simula una función **glcolor.** Si GL MAP1 NORMAL o GL MAP2 NORMAL están habilitados, Se genera un vector normal y, si se habilita alguna de LAS FUNCIONES \_ \_ \_ \_ \_ MAP1 \_ TEXTURE \_ COORD \_ 1, GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2, GL \_ \_ MAP1 TEXTURE \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ \_ COORD 4, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD 3 y GL \_ MAP2 TEXTURE COORD 4, \_ \_ \_ \_ [](gltexcoord-functions.md) se simula una función glTexCoord adecuada.

OpenGL usa valores evaluados en lugar de valores actuales para las evaluaciones habilitadas y los valores actuales en caso contrario, para las coordenadas de color, índice de color, normal y textura. Sin embargo, los valores evaluados no actualizan los valores actuales. Por lo tanto, si las funciones [**glVertex**](glvertex-functions.md) se intercalan con funciones **glEvalCoord,** las coordenadas de color, normal y textura asociadas a las funciones **glVertex** no se ven afectadas por los valores generados por las funciones **glEvalCoord,** sino solo por las funciones [**glColor**](glcolor-functions.md), [**glIndex,**](glindex-functions.md) [**glNormal**](glnormal-functions.md)y [**glTexCoord**](gltexcoord-functions.md) más recientes.

Si la generación normal automática está habilitada, **glEvalCoord2dv** llama [**a glEnable**](glenable.md) con el argumento GL AUTO NORMAL para generar normales de superficie de forma analítica, independientemente del contenido o de la habilitación del mapa \_ NORMAL DE GL \_ \_ \_ MAP2. Let

![Ecuación que muestra un valor entre productos para un mapa m.](images/evlcrd01.png)

El n normal **generado es**

![Ecuación que muestra el n normal generado para el mapa.](images/evlcrd02.png)

Las siguientes funciones recuperan información relacionada con **la función glEvalCoord2dv:**

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ VERTEX \_ 3

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ VERTEX \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ INDEX

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ COLOR \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ NORMAL

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ VERTEX \_ 3

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ VERTEX \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ INDEX

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ COLOR \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ NORMAL

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ AUTO \_ NORMAL

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





