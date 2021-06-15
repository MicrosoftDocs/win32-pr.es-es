---
description: Para convertir archivos multimedia al formato ASF, puede usar codificadores de Windows Media. Obtenga información sobre cómo crear un codificador mediante CoCreateInstance.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Creación de un codificador mediante CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c4cdf7b72bbfee97031088502113d085738981
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068471"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Creación de un codificador mediante CoCreateInstance

Para convertir archivos multimedia al formato ASF, puede usar codificadores de Windows Media. Para usar estos codificadores, deben estar registrados en el sistema. Los codificadores se implementan [como Media Foundation](media-foundation-transforms.md) transformaciones (MTA) y deben exponer la interfaz DETRANSFORMTransform. En este tema se describe cómo una aplicación puede obtener un puntero a la interfaz DETRANSFORMTransform del codificador MFT necesaria y crear instancias de ella para su uso.

Para obtener información sobre el registro del codificador, vea [Creación de instancias de Un codificador MFT.](instantiating-the-encoder-mft.md)

-   [Usar la interfaz DETRANSFORM de un codificador](#creating-an-encoder-by-using-cocreateinstance)
    -   [Ejemplo de creación del codificador](#encoder-creation-example)
-   [Temas relacionados](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Usar la interfaz DETRANSFORM de un codificador

Tras el registro correcto de codificadores de Windows Media con el sistema, una aplicación puede enumerar los codificadores mediante una llamada a [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum). Para buscar el codificador adecuado, debe especificar lo siguiente:

-   GUID que representa la categoría , que es **MFT \_ CATEGORY AUDIO \_ \_ ENCODER** o **MFT CATEGORY VIDEO \_ \_ \_ ENCODER**.

-   Formato que se debe coincidir. Esto se establece en la estructura [**\_ MFT REGISTER \_ TYPE \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) que especifica el tipo principal y el subtipo del tipo de medio en el que el codificador generará ejemplos. Esta estructura se pasa en el *parámetro pOutputType.* Para obtener información sobre los tipos admitidos, vea [GUID de tipo multimedia.](media-type-guids.md)

    > [!Note]  
    > No se requiere la información del tipo de entrada en el parámetro *pInputType.* Esto se debe a que la aplicación conoce el tipo de entrada y el codificador espera que el flujo de entrada esté en un formato sin comprimir.

     

[**MFTEnum devuelve**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) una matriz de punteros [**MFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para los MFT del codificador que coinciden con los criterios de búsqueda. Puede crear instancias de un codificador llamando a la función COM **CoCreateInstance** y pasando el CLSID del codificador que desea usar. Esta función devuelve un puntero a la **interfaz DETRANSFORMTransform** que representa el codificador. Para obtener más información sobre esta llamada de función, vea la documentación Windows SDK del modelo de objetos componentes (COM).

### <a name="encoder-creation-example"></a>Ejemplo de creación del codificador

En el ejemplo de código siguiente se muestra cómo crear un codificador de audio o vídeo.


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de instancias de un MFT de codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de Windows Media](windows-media-encoders.md)
</dt> </dl>

 

 



