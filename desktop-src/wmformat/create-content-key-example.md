---
title: Ejemplo de creación de una clave de contenido
description: Ejemplo de creación de una clave de contenido
ms.assetid: 8e75bac3-d1fb-4a72-8088-fe5ff0899ac2
keywords:
- SDK de Windows Media Format, claves de contenido
- SDK de Windows Media Format, código de ejemplo
- SDK de Windows Media Format, ejemplos de código
- Administración de derechos digitales (DRM), claves de contenido
- DRM (administración de derechos digitales), claves de contenido
- Administración de derechos digitales (DRM), código de ejemplo
- DRM (administración de derechos digitales), código de ejemplo
- Administración de derechos digitales (DRM), ejemplos de código
- DRM (administración de derechos digitales), ejemplos de código
- API extendidas del cliente DRM, claves de contenido
- API extendidas del cliente, claves de contenido
- API extendidas del cliente DRM, código de ejemplo
- API extendidas de cliente, código de ejemplo
- API extendidas del cliente DRM, ejemplos de código
- API extendidas de cliente, ejemplos de código
- claves de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881dfd0d318d7d699b44ca9c3f77f22f9acfc689
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076344"
---
# <a name="create-content-key-example"></a><span data-ttu-id="c7771-119">Ejemplo de creación de una clave de contenido</span><span class="sxs-lookup"><span data-stu-id="c7771-119">Create Content Key Example</span></span>

<span data-ttu-id="c7771-120">La clave de contenido se usa para cifrar los ejemplos de medios para la importación de DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c7771-120">The content key is used to encrypt media samples for Windows Media DRM Import.</span></span> <span data-ttu-id="c7771-121">En el ejemplo de código siguiente se muestra cómo crear e inicializar una estructura de clave de contenido.</span><span class="sxs-lookup"><span data-stu-id="c7771-121">The following code example demonstrates how to create and initialize a content key structure.</span></span>


```C++
HRESULT CreateContentKey( WMDRM_IMPORT_CONTENT_KEY **ppContentKey, DWORD *pcbContentKey)
{
    // TODO: Set this value to the desired number of bytes for the content key data. 
    const DWORD IV_DATA_SIZE = 16;
    HRESULT hr = S_OK;
    WMDRM_IMPORT_CONTENT_KEY *pContentKey = NULL;

    // The content key.
    const BYTE rgbContentKey[] = {
        0x67, 0x39, 0x83, 0xb9,
        0x52, 0xa8, 0xe3
    };        
    const DWORD CONTENT_KEY_DATA_SIZE = sizeof(rgbContentKey);

    // Compute the total size of the content key structure
    DWORD cbContentKey = sizeof( WMDRM_IMPORT_CONTENT_KEY ) +
      IV_DATA_SIZE + CONTENT_KEY_DATA_SIZE;

    // Make sure we have a valid 
    if( NULL == ppContentKey )
    {
        hr = E_POINTER;
        goto EXIT;
    }

    // Allocate the content key, locally first
    pContentKey = (WMDRM_IMPORT_CONTENT_KEY *)new BYTE[ cbContentKey ];
    
    // Check the allocation was successful 
    if( NULL == pContentKey )
    {
        hr = E_OUTOFMEMORY;
        goto EXIT;
    }

    // Ininitalize the key
    ZeroMemory( pContentKey, cbContentKey );
    pContentKey->dwVersion = 0;
    pContentKey->cbStructSize = cbContentKey;

    // Set the initialization vector key type 
    pContentKey->dwIVKeyType = WMDRM_KEYTYPE_RC4;
    pContentKey->cbIVKey = IV_DATA_SIZE;
    
    // Generate a random initialization vector. Note that this random number
    //  generator is not very good. It is only intended to be demonstrative
    //  and it is not recommended for use in commercial strength code.
    srand((unsigned int)time(NULL));
    BYTE* pKeyData = pContentKey->rgbKeyData;
    for (size_t i = 0; i < IV_DATA_SIZE; ++i)
    {
        *pKeyData++ = (BYTE)(rand() & 0xFF); 
    }   
    
    // Set the content key type.
    pContentKey->dwContentKeyType = WMDRM_KEYTYPE_COCKTAIL;
    pContentKey->cbContentKey = CONTENT_KEY_DATA_SIZE;

    // Fill out the content key. 
    for (size_t i = 0; i < CONTENT_KEY_DATA_SIZE; ++i)
    {
        *pKeyData++ = rgbContentKey[i]; 
    }   
    

    // If all has been successful, set the parameters
    *ppContentKey = pContentKey;
    pContentKey = NULL;
    *pcbContentKey = cbContentKey;

EXIT:
    SAFE_ARRAY_DELETE( pContentKey );
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c7771-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7771-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7771-123">**Ejemplos de importación de DRM**</span><span class="sxs-lookup"><span data-stu-id="c7771-123">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




