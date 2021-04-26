---
description: Estas opciones identifican los tipos de recursos de consulta.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eac450ed722da26fe4885d41707483adf401f89
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994112"
---
# <a name="d3dusage_query"></a>CONSULTA D3DUSAGE \_

Estas opciones identifican los tipos de recursos de consulta.



| \#Definir                                   | Descripción                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILTRO DE CONSULTA D3DUSAGE \_ \_                    | Consulte el formato de recurso para ver si admite tipos de filtro de textura distintos de D3DTEXF \_ POINT (que siempre se admite).                                                                                                                                                                                                                         |
| D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP             | Consulte el recurso sobre un mapa de protuberancia heredado.                                                                                                                                                                                                                                                                                                         |
| MEZCLA DE \_ POSTPIXELSHADER DE CONSULTAS D3DUSAGE \_ \_ | Consulte el recurso para comprobar la compatibilidad con la compatibilidad posterior con la combinación de sombreadores de píxeles. Si [**CheckDeviceFormat produce**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) un error con D3DUSAGE \_ QUERY \_ POSTPIXELSHADER BLENDING, no se admiten las operaciones de combinación de píxeles \_ posteriores. Entre ellas se incluyen la prueba alfa, píxeles de píxeles, combinación de destino de representación, habilitación de escritura de color y dithering. |
| D3DUSAGE \_ QUERY \_ SRGBREAD                  | Consulte el recurso para comprobar si una textura admite la corrección gamma durante una operación de lectura.                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ QUERY \_ SRGBWRITE                 | Consulte el recurso para comprobar si una textura admite la corrección gamma durante una operación de escritura.                                                                                                                                                                                                                                                       |
| VÉRTICE DE CONSULTA D3DUSAGETEXTURE \_ \_             | Consulte el recurso para comprobar la compatibilidad con el muestreo de textura del sombreador de vértices.                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ QUERY \_ WRAPANDMIP                | Consulte el recurso para comprobar la compatibilidad con el ajuste de texturas y la asignación de mip.                                                                                                                                                                                                                                                                          |



 

Use [**CheckDeviceFormat para**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) consultar la compatibilidad de hardware para estos usos y otros usos enumerados en [D3DUSAGE](d3dusage.md).

## <a name="constant-information"></a>Información constante



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3d9types.h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
