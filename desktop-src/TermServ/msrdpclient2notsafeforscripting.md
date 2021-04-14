---
title: Clase MsRdpClient2NotSafeForScripting
description: Control de cliente RDP de Microsoft-versión 3.
ms.assetid: F4584E14-6389-49F0-808D-E95858986BCD
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la clase MsRdpClient2NotSafeForScripting
- Servicios de Escritorio remoto de la clase MsRdpClient2NotSafeForScripting, descrito
topic_type:
- apiref
api_name:
- MsRdpClient2NotSafeForScripting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d64b25909a9d9c7bfa6b2fbf88531333b53951
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422320"
---
# <a name="msrdpclient2notsafeforscripting-class"></a>Clase MsRdpClient2NotSafeForScripting

Control de cliente de Microsoft RDP-versión 3

Esta clase implementa las interfaces siguientes.

-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)

**MsRdpClient2NotSafeForScripting** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MsRdpClient2NotSafeForScripting** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](imstscax-connect.md)                                                         | Inicia una conexión utilizando las propiedades establecidas actualmente en el control.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crea un objeto de canal virtual del lado cliente para cada nombre de canal virtual especificado.<br/>                                                                                                                                                                                              |
| [**Desconectar**](imstscax-disconnect.md)                                                   | Desconecta la conexión activa.<br/>                                                                                                                                                                                                                                                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Recupera las opciones establecidas para un canal virtual.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Notifica al módulo de redireccionamiento de dispositivos del Escritorio remoto control ActiveX que se ha producido un cambio de dispositivo en el sistema. Este método pasa las notificaciones de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) al control.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Se llama después de que un control ActiveX muestre un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo error de certificado).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Se llama antes de que un control ActiveX muestre un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo error de certificado).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Se llama cuando el control de cliente se vuelve a conectar automáticamente a una sesión remota.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con un servidor host de sesión de escritorio remoto.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con un servidor host de sesión de escritorio remoto.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Se llama cuando el cliente recibe datos en un canal virtual que admite scripts.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Se llama cuando el cliente llama al método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) .<br/>                                                                                                                                                                           |
| [**Conectado**](imstscaxevents-onconnected.md)                                           | Se llama cuando el control de cliente está en proceso de establecer una conexión con un servidor host de sesión de escritorio remoto.<br/>                                                                                                                                                                       |
| [**Conectar**](imstscaxevents-onconnecting.md)                                         | Se llama cuando el control de cliente comienza a conectarse a un servidor en respuesta a una llamada a [**IMsTscAx:: Connect**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Se llama cuando el usuario ha arrastrado hacia abajo en la barra de conexión.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Se le llama cuando se ha presionado el botón dispositivos en la barra de conexión.<br/>                                                                                                                                                                                                             |
| [**OnDisconnection**](imstscaxevents-ondisconnected.md)                                     | Se llama cuando el control de cliente se ha desconectado del servidor host de sesión de escritorio remoto.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Se llama cuando el cliente entra en el modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de [teclas de método abreviado](terminal-services-shortcut-keys.md) del modo de pantalla completa (Ctrl + Alt + inter).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Se llama cuando el control de cliente encuentra un error irrecuperable.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Se le llama cuando se presiona la combinación de teclas de foco de versión. Por ejemplo, se llama a este evento cuando el usuario presiona las teclas CTRL + ALT + Flecha izquierda o CTRL + ALT + Flecha derecha.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Se llama cuando el usuario no ha realizado ninguna entrada del mouse o del teclado durante el período de tiempo establecido por el método [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Se llama cuando el cliente deja el modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de [teclas de método abreviado](terminal-services-shortcut-keys.md) del modo de pantalla completa (Ctrl + Alt + inter).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Se llama cuando el control de cliente ha iniciado sesión correctamente en un servidor host de sesión de escritorio remoto, después de mostrar el cuadro de diálogo Inicio de sesión de Windows.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Se le llama cuando se produce un error de inicio de sesión u otro evento de inicio de sesión.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Se le llama cuando cambia el modo de entrada del mouse.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Se llama cuando el estado de la red ha cambiado.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Se llama durante la secuencia de conexión cuando el cliente recupera la clave pública del servidor. Solo se llama a este evento si la propiedad **NotifyTSPublicKey** es **Variant \_ true**.<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Se llama para indicar que el tamaño del control de cliente en el escritorio remoto ha cambiado en respuesta a una operación de control de cliente.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Se le llama cuando se muestra un programa RemoteApp.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Se llama cuando un programa RemoteApp devuelve un resultado al control de cliente.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Se le llama cuando se muestra una ventana de RemoteApp.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Se llama cuando el usuario presiona el botón **minimizar** en la barra de conexión en el modo de pantalla completa. La activación de este evento es una solicitud que la aplicación contenedora se minimiza por sí misma.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Se llama cuando el cliente solicita cambiar al modo de pantalla completa y se llama al método [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) para establecer la propiedad **ContainerHandledFullScreen** en un valor distinto de cero.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Se llama cuando el cliente solicita dejar el modo de pantalla completa y la propiedad [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) se ha establecido en un valor distinto de cero.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Se llama cuando el cliente recibe un mensaje del sistema.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Se llama cuando el control ha adquirido el nombre de usuario.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Se llama cuando el control de cliente encuentra una condición de error que no es grave.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Solicita un cierre estable del control de cliente.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Restablece todos los Estados de contraseña en el control.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envía una serie de pulsaciones de teclas al control. Las pulsaciones de teclas están en formato de código de examen, que son los datos de teclado de las claves físicas reales.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envía datos al servidor host de sesión de escritorio remoto a través de un canal virtual que se creó anteriormente mediante el método [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md) .<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Establece las opciones de canal virtual para el control de cliente.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Propiedades

La clase **MsRdpClient2NotSafeForScripting** tiene estas propiedades.



| Propiedad                                                                             | Tipo de acceso           | Descripción                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Solo lectura<br/>  | Puntero a la interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .<br/>                                                                       |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Solo lectura<br/>  | Puntero a la interfaz [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) , que se usa para establecer la configuración avanzada del control de cliente.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Solo lectura<br/>  | Puntero a la interfaz [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) , que se usa para establecer la configuración avanzada del control de cliente.<br/>         |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>              | Lectura/escritura<br/> | Esta propiedad no es compatible.<br/>                                                                                                                                |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                      | Lectura/escritura<br/> | Esta propiedad no es compatible.<br/>                                                                                                                                |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Solo lectura<br/>  | Intensidad máxima de cifrado del control actual.<br/>                                                                                                        |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>        | Solo escritura<br/> | La contraseña del control ActiveX Escritorio remoto, en formato de texto no cifrado.<br/>                                                                                              |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lectura/escritura<br/> | Profundidad de color del control actual.<br/>                                                                                                                            |
| [**Conectado**](imstscax-connected.md)<br/>                                   | Solo lectura<br/>  | Estado de conexión del control actual.<br/>                                                                                                                   |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lectura/escritura<br/> | Texto que se muestra en el área cliente del control mientras el control está en estado conectado.<br/>                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | Lectura/escritura<br/> | Texto que aparece centrado en el control mientras el control se está conectando.<br/>                                                                                 |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lectura/escritura<br/> | Alto del control actual, en píxeles, en el escritorio remoto inicial.<br/>                                                                                        |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lectura/escritura<br/> | El ancho del control actual, en píxeles, en el escritorio remoto inicial.<br/>                                                                                         |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Lectura/escritura<br/> | El texto que aparece centrado en el control antes de que se termine una conexión.<br/>                                                                               |
| [**Domain**](imstscax-domain.md)<br/>                                         | Lectura/escritura<br/> | Dominio en el que el usuario actual inicia sesión.<br/>                                                                                                                  |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Solo lectura<br/>  | Información ampliada sobre el motivo del control de cliente para la desconexión.<br/>                                                                                      |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lectura/escritura<br/> | Indica si el control está en modo de pantalla completa.<br/>                                                                                                          |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Solo escritura<br/> | El título de la ventana que se muestra cuando el control está en modo de pantalla completa.<br/>                                                                                            |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Solo lectura<br/>  | Indica si el control ha mostrado una barra de desplazamiento horizontal.<br/>                                                                                           |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>          | Lectura/escritura<br/> | Esta propiedad no es compatible.<br/>                                                                                                                                |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>                  | Lectura/escritura<br/> | Esta propiedad no es compatible.<br/>                                                                                                                                |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | Solo lectura<br/>  | Puntero A la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .<br/>                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Solo lectura<br/>  | Puntero a la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , que se usa para establecer la configuración segura para el control de cliente.<br/>    |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Solo lectura<br/>  | Indica si la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponible.<br/>                                                 |
| [**Server**](imstscax-server.md)<br/>                                         | Lectura/escritura<br/> | Nombre del servidor al que está conectado el control actual.<br/>                                                                                              |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Lectura/escritura<br/> | Indica si el control establecerá la conexión del servidor host de sesión de escritorio remoto inmediatamente después del inicio.<br/>                                                   |
| [**Nombre**](imstscax-username.md)<br/>                                     | Lectura/escritura<br/> | La credencial de inicio de sesión del nombre de usuario.<br/>                                                                                                                                |
| [**Versión**](imstscax-version.md)<br/>                                       | Solo lectura<br/>  | Número de versión del control actual.<br/>                                                                                                                     |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Solo lectura<br/>  | Indica si el control muestra una barra de desplazamiento vertical.<br/>                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| CLSID<br/>                    | CLSID \_ MsRdpClient2NotSafeForScripting se define como 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de controles ActiveX Escritorio remoto](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

