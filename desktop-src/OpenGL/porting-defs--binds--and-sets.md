---
title: Portabilidad de los conjuntos, enlaces y conjuntos
description: Portabilidad de los conjuntos, enlaces y conjuntos
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Migración de la contabilidad de IRIS, definiciones
- trasladar de IRIS GL, definiciones
- trasladar a OpenGL desde IRIS GL, definiciones
- Exportación de OpenGL desde IRIS GL, definiciones
- Migración de la contabilidad de IRIS, enlaces
- portabilidad de IRIS GL, enlaces
- trasladar a OpenGL desde IRIS GL, enlaces
- Exportación de OpenGL desde IRIS GL, enlaces
- Migración de la contabilidad de IRIS, conjuntos
- portabilidad de IRIS GL, conjuntos
- trasladar a OpenGL desde IRIS GL, conjuntos
- Exportación de OpenGL desde IRIS GL, conjuntos
- definitions
- enlaza
- conjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665606"
---
# <a name="porting-defs-binds-and-sets"></a>Portabilidad de los conjuntos, enlaces y conjuntos

OpenGL no tiene tablas de definiciones almacenadas. no se pueden definir modelos de iluminación, material, texturas, estilos de línea o patrones como objetos independientes como se puede hacer en la contabilidad de IRIS. Por lo tanto, OpenGL no tiene equivalentes directos a las siguientes funciones de GL de IRIS:

-   **Imdef** e **inbind**
-   **tevdef** y **tevbind**
-   **textdef** y **textbind**
-   **definestyle** y **setStyle**
-   **defpattern** y **setpattern**

Puede usar listas de visualización de OpenGL para imitar el mecanismo de Def/BIND de IRIS. Por ejemplo, aquí se muestra una definición de material en IRIS GL:


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



El siguiente ejemplo de código OpenGL define el mismo material en una lista de visualización a la que se hace referencia mediante el número de lista definido por el **valor de la función.**


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




