---
title: Direccionamiento relativo (referencia de HLSL VS)
description: En el caso de los sombreadores de vértices, la sintaxis \ \ solo se puede usar en tipos de registro que se puedan abordar relativamente en determinados modelos de sombreador.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406698"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Direccionamiento relativo (referencia de HLSL VS)

La \[ \] sintaxis solo se puede usar en tipos de registro que se puedan abordar relativamente en determinados modelos de sombreador. Las formas de \[ \] sintaxis admitidas se enumeran de la siguiente manera:

Donde:

-   "R" denota cualquier tipo de registro que se pueda abordar relativamente.
-   "A" denota cualquier registro que se pueda usar como índice para abordar relativamente otros registros.
-   n0 - ni, m0 - mj y k son enteros >= 0.



| \[\]sintaxis                              | Índice efectivo                       | Ejemplos                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + m0 + ... + mj \]                  | A + m0 + ... + mj                     | c \[ a0.x + 3 + 7 \]              |
| R \[ k ( = \] Rk )                         | k                                     | c \[ 10 \] ( = c10 )              |
| R \[ A \]                                  | A                                     | c \[ a0.y \]                      |
| Rk \[ n0 + ... + ni + A + m0 + ... + mj \] | A + k + n0 + ... + ni + m0 + ... + mj | c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \] |
| R \[ n0 + ... + ni + A + m0 + ... + mj \]  | A + n0 + ... + ni + m0 + ... + mj     | c \[ 2 + 1 + aL + 3 + 4 + 5 \]    |
| Rk \[ A \]                                 | A + k                                 | c12 \[ aL \] , c0 \[ a0.z \]        |
| Rk \[ A + m0 + ... + mj \]                 | A + k + m0 + ... + mj                 | v1 \[ aL + 4 + 8 \]               |
| R \[ n0 + ... + ni + A \]                  | A + n0 + ... + ni                     | o \[ 3 + 1 + aL \]                |
| Rk \[ n0 + ... + ni + A \]                 | A + k + n0 + ... + ni                 | o1 \[ 2 + 1 + 3 + aL \]           |



 

Los registros están disponibles en las siguientes versiones:



| Tipo de registro | Versiones del sombreador de vértices |
|---------------|------------------------|
| a0            | Todo                    |
| aL            | vs \_ 2 \_ 0 y superiores    |
| cn            | vs \_ 1 \_ 1 y superiores    |
| on            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




