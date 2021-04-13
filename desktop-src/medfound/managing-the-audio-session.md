---
description: En este tema se describe cómo controlar el volumen de audio cuando se usa MFPlay para la reproducción de audio y vídeo.
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: Administrar la sesión de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5231ca02603279675fabaaac4b96a1cd001906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360130"
---
# <a name="managing-the-audio-session"></a>Administrar la sesión de audio

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo controlar el volumen de audio cuando se usa MFPlay para la reproducción de audio y vídeo.

MFPlay proporciona los siguientes métodos para controlar el volumen de audio durante la reproducción.



| Método                                                            | Descripción                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [**IMFPMediaPlayer::SetBalance**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | Establece el equilibrio entre los canales izquierdo y derecho. |
| [**IMFPMediaPlayer::SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | Silencia o desactiva el audio.                           |
| [**IMFPMediaPlayer::SetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | Establece el nivel de volumen.                                |



 

Para comprender el comportamiento de estos métodos, debe conocer la terminología de la API de sesión de audio de Windows (WASAPI), que implementa la funcionalidad de audio de bajo nivel que usa MFPlay.

En WASAPI, cada secuencia de audio pertenece a exactamente una *sesión de audio*, que es un grupo de secuencias de audio relacionadas. Normalmente, una aplicación mantiene una única sesión de audio, aunque las aplicaciones pueden crear más de una sesión. El programa de control de volumen del sistema (Sndvol) muestra un control de volumen para cada sesión de audio. A través de Sndvol, un usuario puede ajustar el volumen de una sesión de audio desde fuera de la aplicación. En la imagen siguiente se ilustra este proceso.

![diagrama que muestra secuencias de audio que pasan a través del control de volumen a los oradores; sndvol de aplicación y de punto a control de volumen](images/audio-session.gif)

En MFPlay, un elemento multimedia puede tener una o varias secuencias de audio activas (normalmente solo una). Internamente, MFPlay usa el [representador de audio de streaming](streaming-audio-renderer.md) (SAR) para representar las secuencias de audio. A menos que lo configure de otro modo, el SAR se une a la sesión de audio predeterminada de la aplicación.

Los métodos de audio MFPlay controlan solo las secuencias que pertenecen al elemento multimedia actual. No afectan al volumen de ningún otro flujo que pertenezca a la misma sesión de audio. En términos de WASAPI, los métodos de MFPlay controlan los niveles de volumen *por canal* , no el nivel de volumen maestro. En la imagen siguiente se ilustra este proceso.

![diagrama similar al anterior, pero el segundo flujo comienza en el elemento multimedia, y la aplicación apunta a la segunda secuencia y al control de volumen.](images/audio-session02.gif)

Es importante comprender algunas implicaciones de esta característica de MFPlay. En primer lugar, una aplicación puede ajustar el volumen de reproducción sin que afecte a otras secuencias de audio. Puede usar esta característica si MFPlay para implementar el fundido cruzado de audio, creando dos instancias del objeto MFPlay y ajustando el volumen por separado.

Si usa métodos de MFPlay para cambiar el estado de volumen o silenciar, los cambios no aparecen en Sndvol. Por ejemplo, puede llamar a [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) para silenciar el audio, pero Sndvol no mostrará la sesión como silenciada. Por el contrario, si se usa SndVol para ajustar el volumen de sesión, los cambios no se reflejan en los valores devueltos por [**IMFPMediaPlayer:: GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) o [**IMFPMediaPlayer:: GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).

Para cada instancia del objeto MFPlay Player, el nivel de volumen efectivo es igual a *fPlayerVolume* × *FSessionVolume*, donde *fPlayerVolume* es el valor devuelto por [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume)y *fSessionVolume* es el volumen principal de la sesión.

En el caso de escenarios de reproducción sencillos, podría ser preferible usar WASAPI para controlar el volumen de audio para toda la sesión, en lugar de usar los métodos MFPlay.

## <a name="example-code"></a>Código de ejemplo

A continuación se muestra una clase de C++ que controla las tareas básicas de WASAPI:

-   Controlar el volumen y silenciar el estado de la sesión.
-   Recibir notificaciones cada vez que cambie el estado del volumen o silenciar.

### <a name="class-declaration"></a>Declaración de clase

La `CAudioSessionVolume` declaración de clase implementa la interfaz [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , que es la interfaz de devolución de llamada para los eventos de la sesión de audio.


```C++
class CAudioSessionVolume : public IAudioSessionEvents
{
public:
    // Static method to create an instance of the object.
    static HRESULT CreateInstance(
        UINT uNotificationMessage,
        HWND hwndNotification,
        CAudioSessionVolume **ppAudioSessionVolume
    );

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IAudioSessionEvents methods.

    STDMETHODIMP OnSimpleVolumeChanged(
        float NewVolume,
        BOOL NewMute,
        LPCGUID EventContext
        );

    // The remaining audio session events do not require any action.
    STDMETHODIMP OnDisplayNameChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnIconPathChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnChannelVolumeChanged(DWORD,float[],DWORD,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnGroupingParamChanged(LPCGUID,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnStateChanged(AudioSessionState)
    {
        return S_OK;
    }

    STDMETHODIMP OnSessionDisconnected(AudioSessionDisconnectReason)
    {
        return S_OK;
    }

    // Other methods
    HRESULT EnableNotifications(BOOL bEnable);
    HRESULT GetVolume(float *pflVolume);
    HRESULT SetVolume(float flVolume);
    HRESULT GetMute(BOOL *pbMute);
    HRESULT SetMute(BOOL bMute);
    HRESULT SetDisplayName(const WCHAR *wszName);

protected:
    CAudioSessionVolume(UINT uNotificationMessage, HWND hwndNotification);
    ~CAudioSessionVolume();

    HRESULT Initialize();

protected:
    LONG m_cRef;                        // Reference count.
    UINT m_uNotificationMessage;        // Window message to send when an audio event occurs.
    HWND m_hwndNotification;            // Window to receives messages.
    BOOL m_bNotificationsEnabled;       // Are audio notifications enabled?

    IAudioSessionControl    *m_pAudioSession;
    ISimpleAudioVolume      *m_pSimpleAudioVolume;
};
```



Cuando el `CAudioSessionVolume` objeto recibe un evento de sesión de audio, envía un mensaje de ventana privada a la aplicación. El identificador de ventana y el mensaje de ventana se proporcionan como parámetros para el `CAudioSessionVolume::CreateInstance` método estático.

### <a name="getting-the-wasapi-interface-pointers"></a>Obtener los punteros de la interfaz WASAPI

`CAudioSessionVolume` usa dos interfaces WASAPI principales:

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) administra la sesión de audio.
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controla el nivel de volumen y el estado de silencio de la sesión.

Para obtener estas interfaces, debe enumerar el extremo de audio que utiliza el SAR. Un *punto de conexión de audio* es un dispositivo de hardware que captura o usa datos de audio. Para la reproducción de audio, un punto de conexión es simplemente un altavoz u otra salida de audio. De forma predeterminada, el SAR usa el punto de conexión predeterminado para el rol de dispositivo **eConsole** . Un *rol de dispositivo* es un rol asignado para un punto de conexión. Los roles de dispositivo se especifican mediante la enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , que está documentada en las [API de audio Core](../coreaudio/core-audio-apis-in-windows-vista.md).

En el código siguiente se muestra cómo enumerar el punto de conexión y obtener las interfaces de WASAPI.


```C++
HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}
```



### <a name="controlling-the-volume"></a>Control del volumen

Los `CAudioSessionVolume` métodos que controlan el volumen de audio llaman a los métodos [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) equivalentes. Por ejemplo, `CAudioSessionVolume::SetVolume` llama a [**ISimpleAudioVolume:: SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), tal y como se muestra en el código siguiente.


```C++
HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}
```



## <a name="complete-caudiosessionvolume-code"></a>Código de CAudioSessionVolume completo

Esta es la lista completa de los métodos de la `CAudioSessionVolume` clase.


```C++
static const GUID AudioSessionVolumeCtx =
{ 0x2715279f, 0x4139, 0x4ba0, { 0x9c, 0xb1, 0xb3, 0x51, 0xf1, 0xb5, 0x8a, 0x4a } };


CAudioSessionVolume::CAudioSessionVolume(
    UINT uNotificationMessage,
    HWND hwndNotification
    )
    : m_cRef(1),
      m_uNotificationMessage(uNotificationMessage),
      m_hwndNotification(hwndNotification),
      m_bNotificationsEnabled(FALSE),
      m_pAudioSession(NULL),
      m_pSimpleAudioVolume(NULL)
{
}

CAudioSessionVolume::~CAudioSessionVolume()
{
    EnableNotifications(FALSE);

    SafeRelease(&m_pAudioSession);
    SafeRelease(&m_pSimpleAudioVolume);
};


//  Creates an instance of the CAudioSessionVolume object.

/* static */
HRESULT CAudioSessionVolume::CreateInstance(
    UINT uNotificationMessage,
    HWND hwndNotification,
    CAudioSessionVolume **ppAudioSessionVolume
    )
{

    CAudioSessionVolume *pAudioSessionVolume = new (std::nothrow)
        CAudioSessionVolume(uNotificationMessage, hwndNotification);

    if (pAudioSessionVolume == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pAudioSessionVolume->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppAudioSessionVolume = pAudioSessionVolume;
    }
    else
    {
        pAudioSessionVolume->Release();
    }

    return hr;
}


//  Initializes the CAudioSessionVolume object.

HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}

STDMETHODIMP CAudioSessionVolume::QueryInterface(REFIID riid, void **ppv)
{
    static const QITAB qit[] =
    {
        QITABENT(CAudioSessionVolume, IAudioSessionEvents),
        { 0 },
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::Release()
{
    LONG cRef = InterlockedDecrement( &m_cRef );
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}


// Enables or disables notifications from the audio session. For example, the
// application is notified if the user mutes the audio through the system
// volume-control program (Sndvol).

HRESULT CAudioSessionVolume::EnableNotifications(BOOL bEnable)
{
    HRESULT hr = S_OK;

    if (m_hwndNotification == NULL || m_pAudioSession == NULL)
    {
        return E_FAIL;
    }

    if (m_bNotificationsEnabled == bEnable)
    {
        // No change.
        return S_OK;
    }

    if (bEnable)
    {
        hr = m_pAudioSession->RegisterAudioSessionNotification(this);
    }
    else
    {
        hr = m_pAudioSession->UnregisterAudioSessionNotification(this);
    }

    if (SUCCEEDED(hr))
    {
        m_bNotificationsEnabled = bEnable;
    }

    return hr;
}


// Gets the session volume level.

HRESULT CAudioSessionVolume::GetVolume(float *pflVolume)
{
    if ( m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMasterVolume(pflVolume);
    }
}

//  Sets the session volume level.
//
//  flVolume: Ranges from 0 (silent) to 1 (full volume)

HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}


//  Gets the muting state of the session.

HRESULT CAudioSessionVolume::GetMute(BOOL *pbMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMute(pbMute);
    }
}

//  Mutes or unmutes the session audio.

HRESULT CAudioSessionVolume::SetMute(BOOL bMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMute(
            bMute,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}

//  Sets the display name for the session audio.

HRESULT CAudioSessionVolume::SetDisplayName(const WCHAR *wszName)
{
    if (m_pAudioSession == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pAudioSession->SetDisplayName(wszName, NULL);
    }
}


//  Called when the session volume level or muting state changes.
//  (Implements IAudioSessionEvents::OnSimpleVolumeChanged.)

HRESULT CAudioSessionVolume::OnSimpleVolumeChanged(
    float NewVolume,
    BOOL NewMute,
    LPCGUID EventContext
    )
{
    // Check if we should post a message to the application.

    if ( m_bNotificationsEnabled &&
        (*EventContext != AudioSessionVolumeCtx) &&
        (m_hwndNotification != NULL)
        )
    {
        // Notifications are enabled, AND
        // We did not trigger the event ourselves, AND
        // We have a valid window handle.

        // Post the message.
        ::PostMessage(
            m_hwndNotification,
            m_uNotificationMessage,
            *((WPARAM*)(&NewVolume)),  // Coerce the float.
            (LPARAM)NewMute
            );
    }
    return S_OK;
}
```



## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
