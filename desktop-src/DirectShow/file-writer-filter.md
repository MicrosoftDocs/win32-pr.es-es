---
description: Filtro de escritor de archivos
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro de escritor de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274777"
---
# <a name="file-writer-filter"></a>Filtro de escritor de archivos

El filtro del escritor de archivos se puede usar para escribir archivos en el disco independientemente del formato. El filtro simplemente escribe en el disco lo que reciba en su PIN de entrada, por lo que se debe conectar al nivel superior a un multiplexor que pueda dar formato al archivo correctamente. Puede crear un nuevo archivo de salida con el escritor de archivos o especificar un archivo existente. Si el archivo ya existe, se sobrescribirá por completo con los nuevos datos.

El filtro del escritor de archivos utiliza las marcas de tiempo del flujo de entrada como desplazamientos de archivo y proporciona acceso aleatorio al archivo. Admite **IStream** para permitir la lectura y escritura del encabezado de archivo después de que el gráfico se detenga. Para mejorar el rendimiento, también admite escrituras superpuestas no almacenadas en búfer y controla la negociación de búfer correspondiente.

> [!Note]  
> Para escribir archivos ASF, use el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) .

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream** |
| Tipos de medios de anclaje de entrada                    | \_Secuencia MEDIATYPE, MEDIASUBTYPE \_ null                                                                                                                                                              |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**                                                                                |
| Tipos de medios de anclaje de salida                   | No aplicable                                                                                                                                                                                     |
| Interfaces de clavija de salida                    | No aplicable                                                                                                                                                                                     |
| Identificador CLSID                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                   |
| Executable                               | qcap.dll                                                                                                                                                                                           |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



