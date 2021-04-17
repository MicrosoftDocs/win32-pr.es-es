---
description: Establece la información del servidor proxy.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'IWinHttpRequest:: SetProxy (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717211"
---
# <a name="iwinhttprequestsetproxy-method"></a>IWinHttpRequest:: SetProxy (método)

El método **SetProxy** establece la información del servidor proxy.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProxySetting* \[ de\]
</dt> <dd>

Marcas que controlan este método. Puede ser uno de los valores siguientes.



| Value                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ predeterminado</dt> </dl>   | Configuración de proxy predeterminada. Equivalente a **HTTPREQUEST \_ PROXYSETTING \_ Preconfig**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>preconfiguración de \_ PROXYSETTING HTTPREQUEST \_</dt> </dl> | Indica que la configuración del proxy debe obtenerse del registro. Se supone que se ha ejecutado [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) . Si Proxycfg.exe no se ha ejecutado y se ha especificado la **\_ \_ preconfiguración de HttpRequest PROXYSETTING** , el comportamiento es equivalente a **HttpRequest \_ PROXYSETTING \_ Direct**.<br/> |
| <dl> <dt>PROXYSETTING de HTTPREQUEST \_ \_ directo</dt> </dl>    | Indica que se debe tener acceso directamente a todos los servidores HTTP y HTTPS. Use este comando si no hay ningún servidor proxy.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>\_proxy PROXYSETTING \_ HTTPREQUEST</dt> </dl>     | Cuando se especifica el **\_ \_ proxy HTTPREQUEST PROXYSETTING** , *varProxyServer* se debe establecer en una cadena de servidor proxy y *varBypassList* debe establecerse en una cadena de lista de omisión de dominio. Esta configuración de proxy solo se aplica a la instancia actual del objeto [**WinHttpRequest**](winhttprequest.md) .<br/>                                    |



 

</dd> <dt>

*ProxyServer* \[ en, opcional\]
</dt> <dd>

Se establece en una cadena de servidor proxy cuando *ProxySetting* es igual a **HTTPREQUEST \_ ProxySetting \_ proxy**.

</dd> <dt>

*BypassList* \[ en, opcional\]
</dt> <dd>

Se establece en una cadena de lista de omisión de dominio cuando *ProxySetting* es igual a **HTTPREQUEST \_ ProxySetting \_ proxy**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**

## <a name="remarks"></a>Observaciones

Permite a la aplicación que realiza la llamada especificar el uso de la información de proxy predeterminada (configurada por la herramienta de configuración de proxy) o invalidar [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md). Se debe llamar a este método antes de llamar al método [**send**](iwinhttprequest-send.md) . Si se llama a este método después del método [**send**](iwinhttprequest-send.md) , no tiene ningún efecto.

[**IWinHttpRequest**](iwinhttprequest-interface.md) pasa estos parámetros a los servicios http de Microsoft Windows (WinHTTP).

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer la configuración de proxy para un servidor proxy determinado, abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta. Este ejemplo debe ejecutarse desde un símbolo del sistema. Esta configuración de proxy solo funciona si tiene un servidor proxy denominado " \_ servidor proxy" que usa el puerto 80 y el equipo puede omitir el servidor proxy cuando el nombre de host termina con ". Microsoft.com".


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
        }
    if (SUCCEEDED(hr))
    {   // Open WinHttpRequest.
            BSTR bstrMethod  = SysAllocString(L"GET");
                BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
                SysFreeString(bstrMethod);
                SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
                hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



En el ejemplo de scripting siguiente se muestra cómo establecer la configuración de proxy para un servidor proxy determinado, abrir una conexión HTTP, enviar una solicitud HTTP y leer el texto de la respuesta. Esta configuración de proxy solo funciona si tiene un servidor proxy denominado " \_ servidor proxy" que usa el puerto 80 y el equipo puede omitir el servidor proxy cuando el nombre de host termina con ". Microsoft.com".


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp. lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




