---
description: En este tema se proporciona información sobre el códec PNG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Información general sobre el formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3d74282f8c14fd94b3661430402a808b04ceb9cf0a061a1648f7a912af5636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086759"
---
# <a name="png-format-overview"></a>Información general sobre el formato PNG

En este tema se proporciona información sobre el códec PNG nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



|     Componente          | Descripción                     |
|------------------------|---------------------------------|
| Nombres formales         | Formato PNG (Portable Network Graphics) |
| Extensiones de nombre de archivo | png                             |
| Tipo de MIME              | image/png                       |
| Compatibilidad con especificaciones  | Especificación PNG 1.2           |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec PNG nativos.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatPng | 1b7cfaf4-713f-473c-qued6137425faeaf |
| Descodificador          | CLSID \_ WICPngDecoder     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Codificador          | CLSID \_ WICPngEncoder     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 y versiones posteriores

A partir de Windows 8 WIC proporciona un descodificador PNG adicional

## <a name="encoding"></a>Encoding

La API de codificación wic está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre codificación.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las funcionalidades de un codificador de imagen y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones del codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la **interfaz IPropertyBag2** para la codificación WIC , vea Información general [sobre codificación](-wic-creating-encoder.md).

El códec PNG usa opciones básicas del codificador WIC. En la tabla siguiente se enumeran las opciones del codificador WIC compatibles con el códec PNG nativo.



| Nombre de la propiedad   | VARTYPE  | Intervalo de valores                                                 | Valor predeterminado                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | VT \_ BOOL | **TRUE** / **FALSE**                                          | **FALSE**                                                        |
| FilterOption    | VT \_ UI1  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Si hay una opción de codificador en la [**lista de opciones IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.

### <a name="interlaceoption"></a>InterlaceOption

Especifica si se codifican los datos de la imagen como entrelazados.

El valor predeterminado es **FALSE**.

### <a name="filteroption"></a>FilterOption

Especifica la opción de filtro que se usará para la compresión de imágenes.

El valor predeterminado es [**WICPngFilterUnspecified.**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)

## <a name="decoding"></a>Descodificación

La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

El códec PNG nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en lacodización de fotogramas y agrega opciones avanzadas para la decodización de un flujo de imagen. Para obtener más información sobre estas opciones avanzadas, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

 

 
