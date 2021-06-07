---
title: Uso de funciones de GDI con WCS
description: Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que usan o funcionan con datos de color.
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- Sistema de colores de Windows (WCS), interfaz de dispositivo gráfico (GDI)
- WCS (Sistema de colores de Windows), interfaz de dispositivo gráfico (GDI)
- administración del color de la imagen, interfaz de dispositivo gráfico (GDI)
- administración de colores, interfaz de dispositivo gráfico (GDI)
- colors,graphics device interface (GDI)
- interfaz de dispositivo gráfico (GDI)
- GDI (interfaz de dispositivo gráfico)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fad8445623efb8854e81e7e1569beab9ed4169b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443656"
---
# <a name="using-gdi-functions-with-wcs"></a>Uso de funciones de GDI con WCS

Hay varias funciones en la interfaz de dispositivo gráfico (GDI) que usan o funcionan con datos de color. Algunas están habilitadas para su uso con WCS y otras no. Las siguientes funciones GDI son relevantes para ICM:

-   [Funciones de contexto de dispositivo con WCS](#device-context-functions-with-wcs)
-   [Funciones de lápiz y pincel con WCS](#pen-and-brush-functions-with-wcs)
-   [Funciones de salida de texto con WCS](#text-output-functions-with-wcs)
-   [Funciones de mapa de bits con WCS](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>Funciones de contexto de dispositivo con WCS



|    Función                |   Descripción                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | Si el contexto de dispositivo (DC) que se pasa a esta función a través de su parámetro hdc está habilitado para ICM, el controlador de dominio que crea la función también está habilitado para ICM. Los espacios de color de origen y destino se especifican en el controlador de dominio. |
| CreateDC           | ICM se puede habilitar estableciendo el miembro dmICMMethod de la estructura DEVMODE a la que apunta el parámetro pInitData en el valor adecuado. Para más información, consulte la documentación de Platform SDK en la estructura DEVMODE.  |
| ResetDC            | El perfil de color del contexto de dispositivo especificado por el parámetro hdc se restablecerá en función de la información de la estructura DEVMODE especificada por el parámetro lpInitData.                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>Funciones de lápiz y pincel con WCS



|    Función                |   Descripción                                                                                                                                                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Funciones de pincel | No se realiza ninguna administración de colores durante la creación del pincel. Sin embargo, la administración de colores se realizará cuando el pincel se seleccione en un controlador de dominio habilitado para ICM. |
| CreatePen       | No se realiza ninguna administración de colores durante la creación del lápiz. Sin embargo, la administración de colores se realizará cuando el pincel se seleccione en un controlador de dominio habilitado para ICM.   |
| ExtCreatePen    | No se realiza ninguna administración de colores durante la creación del lápiz. Sin embargo, la administración de colores se realizará cuando el pincel se seleccione en un controlador de dominio habilitado para ICM.   |
| SelectObject    | Si el objeto que se selecciona es un pincel o un lápiz, se realiza la administración de colores.                                                              |
| SetDCBrushColor | La administración de colores se realiza si WCS está habilitado.                                                                                              |
| SetDCPenColor   | La administración de colores se realiza si WCS está habilitado.                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>Funciones de salida de texto con WCS



|    Función                |   Descripción                                                                                                                                                                                                                              |
|--------------|--------------------------------------------------|
| SetBkColor   | La administración de colores se realiza si WCS está habilitado. |
| SetTextColor | La administración de colores se realiza si WCS está habilitado. |



 

## <a name="bitmap-functions-with-wcs"></a>Funciones de mapa de bits con WCS



|    Función                |   Descripción                                                                                                                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitBlt            | No se realiza ninguna administración de colores cuando se producen rendijas.                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | El parámetro fuUsage especifica que el miembro bmiColors de la estructura BITMAPINFO a la que apunta el parámetro lpbmi sí contiene o no información de color. Si no es así, no se realiza ninguna administración de colores para este mapa de bits. El mapa de bits debe usar la versión 4 o la versión 5 de la estructura BITMAPINFO para habilitar la administración de colores. El contenido del mapa de bits resultante no coincide con el color después de crear el mapa de bits. |
| CreateDIBSection  | Si la estructura BITMAPINFO pasada a través del parámetro pbmi no es la versión 4 o la versión 5, no se realiza ninguna administración de colores. Si es la versión 4 o 5, la administración de colores está habilitada y el espacio de color especificado está asociado al mapa de bits.                                                                                                                                                                                                   |
| MaskBlt           | No se realiza ninguna administración de colores cuando se producen rendijas.                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | Si el objeto es un mapa de bits creado con CreateDIBSection, se realiza la administración de colores. El espacio de colores del mapa de bits se usa como espacio de color de destino.                                                                                                                                                                                                                                                                                       |
| SetDIBits         | Se realiza la administración de colores. Si la estructura BITMAPINFO especificada no es la versión 4 o la versión 5, el perfil de color del controlador de dominio actual se usa como perfil de espacio de color de origen. Si no tiene uno, se usa el espacio sRGB. Si la estructura BITMAPINFO especificada es la versión 4 o la versión 5, el perfil de espacio de colores especificado en el encabezado de mapa de bits se usa como perfil de espacio de color de origen.                                         |
| SetDIBitsToDevice | Se realiza la administración de colores. Si la estructura BITMAPINFO especificada no es la versión 4 o la versión 5, el perfil de color del contexto del dispositivo actual se usa como perfil de espacio de color de origen. Si no tiene uno, se usa el espacio de color sRGB. Si la estructura BITMAPINFO especificada es la versión 4 o la versión 5, el perfil de espacio de color asociado al mapa de bits se usa como espacio de color de origen.                                    |
| SetDIBColorTable  | No se realiza ninguna administración de colores.                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | No se realiza ninguna administración de colores cuando se producen rendijas.                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | Se realiza la administración de colores. Si la estructura BITMAPINFO especificada no es la versión 4 o la versión 5, el perfil de color del controlador de dominio actual se usa como perfil de espacio de color de origen. Si no tiene uno, se usa el espacio sRGB. Si la estructura BITMAPINFO especificada es la versión 4 o la versión 5, el perfil de espacio de colores especificado en el encabezado de mapa de bits se usa como perfil de espacio de color de origen.                                         |



 

 

 




