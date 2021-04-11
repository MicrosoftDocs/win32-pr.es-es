---
description: Enumerar el contenido del servicio
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Enumerar el contenido del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adb949fdec9a0001583b1481ccd50ada1ef1df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275345"
---
# <a name="enumerating-service-content"></a>Enumerar el contenido del servicio

Una vez que la aplicación abre un servicio, puede comenzar a realizar operaciones relacionadas con el servicio. En el caso de la aplicación WpdServicesApiSample, una de estas operaciones es la enumeración de contenido de un servicio de contactos determinado. En la tabla siguiente se describen las interfaces utilizadas.



|                                                                      |                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Interfaz                                                            | Descripción                                                                                      |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Se usa para recuperar la interfaz IPortableDeviceContent2 para tener acceso al contenido del servicio.         |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Se usa para recuperar la interfaz IEnumPortableDeviceObjectIDs para enumerar los objetos en el servicio. |
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | Se utiliza para enumerar objetos en el servicio.                                                        |



 

El código de enumeración de contenido se encuentra en el módulo ContentEnumeration. cpp. Este código reside en los métodos **EnumerateAllContent** y **RecursiveEnumerate** . El método anterior llama a la última.

El método **EnumerateContent** toma un puntero a un objeto [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) como su parámetro. Este objeto corresponde a un servicio que la aplicación abrió anteriormente cuando llamó al método [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) .

El método **EnumerateContent** crea un objeto [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) y pasa este objeto al método [**IPortableDeviceService:: Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) . Este método, a su vez, recupera el contenido en el nivel raíz del servicio y, a continuación, comienza de forma recursiva para recuperar el contenido que se encuentra debajo de la raíz.

El código siguiente corresponde al método **EnumerateContent** .


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



El código siguiente corresponde al método **RecursiveEnumerate** . El método RecursiveEnumerate crea una instancia de una interfaz **IEnumPortableDeviceObjectIDs** para el objeto primario proporcionado y llama a **IEnumPortableDeviceObjectIDs:: Next**, y recupera un lote de objetos secundarios inmediatos. Para cada objeto secundario, se llama de nuevo a RecursiveEnumerate para devolver sus objetos secundarios descendientes, etc.


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Interfaz IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**Interfaz IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[Apertura de un servicio](opening-a-service.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



