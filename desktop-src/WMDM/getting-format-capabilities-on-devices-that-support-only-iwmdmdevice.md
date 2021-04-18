---
title: Obtener capacidades de formato a través de IWMDMDevice
description: Obtener capacidades de formato en dispositivos que solo admiten IWMDMDevice
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Media Administrador de dispositivos, funcionalidades de dispositivo
- Administrador de dispositivos, funcionalidades del dispositivo
- Guía de programación, funcionalidades del dispositivo
- aplicaciones de escritorio, funcionalidades de dispositivo
- creación de aplicaciones de Windows Media Administrador de dispositivos, funcionalidades de dispositivo
- escribir archivos en dispositivos, funcionalidades del dispositivo
- Método IWMDMDevice
- Administrador de dispositivos de Windows Media, método IWMDMDevice
- Administrador de dispositivos, método IWMDMDevice
- Guía de programación, método IWMDMDevice
- aplicaciones de escritorio, método IWMDMDevice
- crear aplicaciones de Windows Media Administrador de dispositivos, método IWMDMDevice
- escribir archivos en dispositivos, método IWMDMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "104358542"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a><span data-ttu-id="b6d86-116">Obtener capacidades de formato a través de IWMDMDevice</span><span class="sxs-lookup"><span data-stu-id="b6d86-116">Getting format capabilities through IWMDMDevice</span></span>

<span data-ttu-id="b6d86-117">El método recomendado para consultar un dispositivo para sus capacidades de reproducción es [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="b6d86-117">The recommended method for querying a device for its playback capabilities is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="b6d86-118">Sin embargo, si un dispositivo no admite este método, en su lugar, la aplicación puede llamar a [**IWMDMDevice:: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) para recuperar una matriz de formatos de audio compatibles como estructuras de [**\_ WAVEFORMATEX**](-waveformatex.md) y formatos MIME como cadenas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6d86-118">However, if a device does not support this method, the application instead can call [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) to retrieve an array of supported audio formats as [**\_WAVEFORMATEX**](-waveformatex.md) structures and MIME formats as strings from the device.</span></span>

<span data-ttu-id="b6d86-119">En los pasos siguientes se muestra cómo una aplicación puede usar este método para consultar los formatos admitidos en un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="b6d86-119">The following steps show how an application can use this method to query a device for supported formats:</span></span>

1.  <span data-ttu-id="b6d86-120">Llame a **GetFormatSupport** para recuperar matrices de formatos de audio y MIME.</span><span class="sxs-lookup"><span data-stu-id="b6d86-120">Call **GetFormatSupport** to retrieve arrays of both audio and mime formats.</span></span>
2.  <span data-ttu-id="b6d86-121">Recorra los formatos de audio recuperados y examine cada estructura [**\_ WAVEFORMATEX**](-waveformatex.md) para intentar encontrar un formato de audio aceptable</span><span class="sxs-lookup"><span data-stu-id="b6d86-121">Loop through the retrieved audio formats and examine each [**\_WAVEFORMATEX**](-waveformatex.md) structure to try to find an acceptable audio format</span></span>
3.  <span data-ttu-id="b6d86-122">Recorra las cadenas de formato MIME recuperadas (si lo desea) para buscar un tipo de archivo aceptable.</span><span class="sxs-lookup"><span data-stu-id="b6d86-122">Loop through the retrieved MIME format strings (if desired) to find an acceptable file type.</span></span> <span data-ttu-id="b6d86-123">El SDK no define las constantes para los formatos MIME; debe usar valores estándar del sector (que se pueden encontrar en el sitio web de iana.org).</span><span class="sxs-lookup"><span data-stu-id="b6d86-123">The SDK does not define constants for MIME formats; you should use industry standard values (which can be found at the iana.org Web site).</span></span> <span data-ttu-id="b6d86-124">Un dispositivo debe enumerar los tipos MIME específicos que admite.</span><span class="sxs-lookup"><span data-stu-id="b6d86-124">A device should list the specific MIME types that it supports.</span></span>

<span data-ttu-id="b6d86-125">En el código de C++ siguiente se muestra cómo recuperar funciones de formato desde un dispositivo, mediante **GetFormatSupport**.</span><span class="sxs-lookup"><span data-stu-id="b6d86-125">The following C++ code demonstrates retrieving format capabilities from a device, using **GetFormatSupport**.</span></span>


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="b6d86-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6d86-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6d86-127">**Detección de capacidades de formato de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="b6d86-127">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> <dt>

[<span data-ttu-id="b6d86-128">**Obtener capacidades de formato en los dispositivos que admiten IWMDMDevice3**</span><span class="sxs-lookup"><span data-stu-id="b6d86-128">**Getting Format Capabilities on Devices That Support IWMDMDevice3**</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




