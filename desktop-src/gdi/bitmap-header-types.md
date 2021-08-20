---
description: Tipos de encabezado de mapa de bits
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: Tipos de encabezado de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c88839947845cc45633cbc07b7c36aec727318c91910bfc277680b1946080531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966415"
---
# <a name="bitmap-header-types"></a>Tipos de encabezado de mapa de bits

El mapa de bits tiene cuatro tipos de encabezado básicos:

-   [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Los cuatro tipos de encabezados de mapa de bits se diferencian por el **miembro Size,** que es el primer **DWORD** en cada una de las estructuras.

La [**estructura BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) es una estructura [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) extendida, que es una estructura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) extendida. Sin embargo, **BITMAPINFOHEADER** y [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) solo tienen el **miembro Size** en común con otras estructuras de encabezado de mapa de bits.

Los [**formatos BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) y [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) se han reemplazado por los formatos [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) y [**BITMAPV5HEADER,**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) respectivamente. Los **formatos BITMAPCOREHEADER** y **BITMAPV4HEADER** se presentan por integridad y compatibilidad con versiones anteriores.

El formato de una DIB es el siguiente (para obtener más información, vea [Bitmap Storage](bitmap-storage.md) ):

-   una [**estructura BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)
-   un [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader), [**un BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**un BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)o una estructura [**BITMAPV5HEADER.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)
-   una tabla de colores opcional, que es un conjunto de estructuras [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) o un conjunto de [**estructuras RGBTRIPLE.**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple)
-   los datos de mapa de bits
-   datos de perfil opcionales

Una tabla de colores describe cómo se corresponden los valores de píxel con los valores de color RGB. RGB es un modelo para describir los colores que se generan mediante la emisión de luz.

*Los datos de perfil* se refieren al nombre del archivo de perfil (perfil vinculado) o a los bits de perfil reales (perfil incrustado). El formato de archivo coloca los datos de perfil al final del archivo. Los datos del perfil se colocan justo después de la tabla de colores (si está presente). Sin embargo, si la función recibe una DIB empaquetada, los datos del perfil vienen después de los bits de mapa de bits, como en el formato de archivo.

Los datos de perfil solo existirán para las estructuras [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) donde **bV5CSType** es PROFILE \_ LINKED o PROFILE \_ EMBEDDED. Para las funciones que reciben DIB empaquetadas, los datos del perfil vienen después de los datos de mapa de bits.

Un dispositivo con problemas es cualquier dispositivo que use paletas para asignar colores. El ejemplo clásico de un dispositivo desenlazado es una pantalla que se ejecuta con una profundidad de color de 8 bits (es decir, 256 colores). La presentación en este modo usa una tabla de colores pequeña para asignar colores a un mapa de bits. Los colores de un mapa de bits se asignan al color más cercano de la paleta que usa el dispositivo. El dispositivo con estado no crea una paleta óptima para mostrar el mapa de bits; simplemente usa lo que se encuentra en la paleta actual. Las aplicaciones son responsables de crear una paleta y seleccionarla en el sistema. En general, los mapas de bits de 16, 24 y 32 bits por píxel (bpp) no contienen tablas de colores (también es decir, paletas óptimas para el mapa de bits); La aplicación es responsable de generar una paleta óptima en este caso. Sin embargo, los mapas de bits de 16, 24 y 32 bpp pueden contener dichas tablas de colores óptimas para mostrarse en dispositivos con color verde. En este caso, la aplicación solo necesita crear una paleta basada en la tabla de colores presente en el archivo de mapa de bits.

Los mapas de bits de 1, 4 u 8 bpp deben tener una tabla de colores con un tamaño máximo basado en bpp. El tamaño máximo de los mapas de bits de 1, 4 y 8 bpp es 2 para la potencia del bpp. Por lo tanto, un mapa de bits de 1 bpp tiene un máximo de dos colores, el mapa de bits de 4 bpp tiene un máximo de 16 colores y el mapa de bits de 8 bpp tiene un máximo de 256 colores.

Los mapas de bits de 16, 24 o 32 bpp no requieren tablas de colores, pero pueden tenerlas para especificar colores para dispositivos con limitaciones. Si hay una tabla de colores para un mapa de bits de 16, 24 o 32 bpp, el miembro **biClrUsed** especifica el tamaño de la tabla de colores y la tabla de colores debe tener tantos colores en ella. Si **biClrUsed** es cero, no hay ninguna tabla de colores.

Las máscaras de campo de bits rojo, verde y azul para los mapas de bits BITFIELD de BI siguen inmediatamente las estructuras \_ [**BITMAPINFOHEADER,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)y [**BITMAPV5HEADER.**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) Las **estructuras BITMAPV4HEADER** y **BITMAPV5HEADER** contienen miembros adicionales para las máscaras de color rojo, verde y azul como se muestra a continuación.



| Miembro        | Significado                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **RedMask**   | Máscara de color que especifica el componente rojo de cada píxel, válido solo si el **miembro Compression** está establecido en BI \_ BITFIELDS.   |
| **Máscara verde** | Máscara de color que especifica el componente verde de cada píxel, válido solo si el **miembro Compression** está establecido en BI \_ BITFIELDS. |
| **BlueMask**  | Máscara de color que especifica el componente azul de cada píxel, válido solo si el **miembro Compression** está establecido en BI \_ BITFIELDS.  |



 

Cuando el **miembro biCompression** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) se establece en BI BITFIELDS y la función recibe un argumento de tipo \_ **LPBITMAPINFO,** las máscaras de color seguirán inmediatamente al encabezado. La tabla de colores, si está presente, seguirá las máscaras de color. [**Los mapas de bits BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) no admiten máscaras de color.

De forma predeterminada, los datos de mapa de bits están de abajo hacia arriba en su formato. De abajo hacia arriba significa que la primera línea de examen de los datos de mapa de bits es la última línea de examen que se va a mostrar. Por ejemplo, el<sup>0</sup> píxel de la línea de examen<sup>0</sup> de los datos de mapa de bits de un mapa de bits de 10 píxeles por 10 píxeles será el<sup>0</sup> píxel de la línea de digitalización<sup>9</sup> de la imagen mostrada o impresa. Los mapas de bits con formato codificado (RLE) de longitud de ejecución y los mapas de [**bits BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) no pueden ser mapas de bits de arriba a abajo. Las líneas de examen están **alineadas con DWORD,** excepto en el caso de los mapas de bits comprimidos con RLE. Se deben agregar para los anchos de línea de examen, en bytes, que no se pueden dividir uniformemente entre cuatro, excepto para los mapas de bits comprimidos de RLE. Por ejemplo, un mapa de bits de 24 bpp de 10 por 10 píxeles tendrá dos bytes de relleno al final de cada línea de examen.

 

 
