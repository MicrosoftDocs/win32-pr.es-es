---
description: Marcas de funcionalidad de coordenada de textura del controlador.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da9ca23ebc4dd121527721a9d10a2db55a4d555
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995262"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Marcas de funcionalidad de coordenada de textura del controlador.



| \#Definir                                 | Value       | Descripción                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTSS \_ TCI \_ PASSTHRU                    | 0x00000000L | Use las coordenadas de textura especificadas contenidas en el formato de vértice. Este valor se resuelve en cero.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Use el vértice normal, transformado en espacio de la cámara, como coordenadas de textura de entrada para la transformación de textura de esta fase.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Use la posición del vértice, transformada en espacio de la cámara, como coordenadas de textura de entrada para la transformación de textura de esta fase.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Use el vector de reflexión, transformado en espacio de la cámara, como coordenada de textura de entrada para la transformación de textura de esta fase. El vector de reflexión se calcula a partir de la posición del vértice de entrada y el vector normal. |
| MAPA DE ESFERA \_ DE TCI de D3DTSS \_                   | 0x00040000L | Use las coordenadas de textura especificadas para la asignación de esferas.                                                                                                                                                            |



 

D3DTSS \_ TEXCOORDINDEX usa estas constantes.

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



