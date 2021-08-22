---
description: Método virtual puro que invalidan las clases derivadas.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Método CBaseControlVideo.GetStaticImage (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69496754c8a1f80be341c475f422229aba6108dbc0e73cd1db9506a301690ffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660835"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a>Método CBaseControlVideo.GetStaticImage

Método virtual puro que invalidan las clases derivadas.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Puntero al tamaño del búfer de salida.

</dd> <dt>

*pDIBImage* 
</dt> <dd>

Puntero al búfer de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

A través de la interfaz [**IBasicVideo,**](/windows/desktop/api/Control/nn-control-ibasicvideo) una aplicación puede solicitar que se le de una copia de la imagen actual en un búfer de memoria (algunos representadores pueden devolver E NOTIMPL a esto si no la \_ admiten). La clase derivada determina cómo recuperar la imagen. Cuando la aplicación llama **a CBaseControlVideo::GetStaticImage**, llama a este método virtual puro que la clase derivada debe invalidar para implementarlo. También lo llama la función miembro [**CBaseControlVideo::GetCurrentImage.**](cbasecontrolvideo-getcurrentimage.md)

La clase proporciona una función miembro del asistente, [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md), a la que se puede proporcionar un ejemplo que contiene una imagen, y la función miembro copiará la sección correspondiente de ella (en función del rectángulo de origen actual) en el búfer de salida proporcionado por la aplicación.

En el ejemplo siguiente se muestra una implementación de esta función miembro en una clase derivada. En este ejemplo, m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md).


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




