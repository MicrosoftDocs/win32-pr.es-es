---
description: La propiedad estado recupera el código de Estado HTTP de la última respuesta.
ms.assetid: 80b05e69-7f00-455d-94c3-a06eaa997cae
title: 'IWinHttpRequest:: status (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Status
- IWinHttpRequest.get_Status
- WinHttpRequest.Status
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ea7569867336547bba4639e36cf65f7b5a08ae6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913614"
---
# <a name="iwinhttprequeststatus-property"></a><span data-ttu-id="c7fc3-103">IWinHttpRequest:: status (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c7fc3-103">IWinHttpRequest::Status property</span></span>

<span data-ttu-id="c7fc3-104">La propiedad **Estado** recupera el código de estado http de la última respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-104">The **Status** property retrieves the HTTP status code from the last response.</span></span>

<span data-ttu-id="c7fc3-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fc3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7fc3-106">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] long *Status
);
```


```JScript

Status = WinHttpRequest.Status
```





## <a name="property-value"></a><span data-ttu-id="c7fc3-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c7fc3-107">Property value</span></span>

<span data-ttu-id="c7fc3-108">Un valor de tipo **Long** que recibe el código de estado devuelto.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-108">A value of type **long** that receives the returned status code.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c7fc3-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c7fc3-109">Error codes</span></span>

<span data-ttu-id="c7fc3-110">El valor devuelto es correcto si se ejecuta correctamente o un valor de error en caso contrario. **\_**</span><span class="sxs-lookup"><span data-stu-id="c7fc3-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7fc3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7fc3-111">Remarks</span></span>

<span data-ttu-id="c7fc3-112">Los resultados de esta propiedad solo son válidos después de que el método [**send**](iwinhttprequest-send.md) se haya completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-112">The results of this property are valid only after the [**Send**](iwinhttprequest-send.md) method has successfully completed.</span></span> <span data-ttu-id="c7fc3-113">Para obtener una lista de códigos de estado, consulte [**códigos de estado http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c7fc3-113">For a list of status codes see [**HTTP Status Codes**](http-status-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="c7fc3-114">En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c7fc3-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c7fc3-115">Examples</span></span>

<span data-ttu-id="c7fc3-116">En el ejemplo siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP, mostrar el **Estado** y [**statusText**](iwinhttprequest-statustext.md)y leer los encabezados de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-116">The following example shows how to open an HTTP connection, send an HTTP request, display the **Status** and [**StatusText**](iwinhttprequest-statustext.md), and read the response headers.</span></span> <span data-ttu-id="c7fc3-117">Este ejemplo debe ejecutarse desde un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-117">This example must be run from a command prompt.</span></span>


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
    // variable for return value
    HRESULT    hr;

    // initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    LONG            lStatus = 0;
    BSTR            bstrStatusText = NULL;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->get_Status(&lStatus);
        hr = pIWinHttpRequest->get_StatusText(&bstrStatusText);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%s\n\n", bstrResponse);
        wprintf(L"%u - %s\n\n", lStatus, bstrStatusText);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrStatusText)
        SysFreeString(bstrStatusText);
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="c7fc3-118">En el ejemplo de scripting siguiente se muestra cómo abrir una conexión HTTP, enviar una solicitud HTTP, mostrar el **Estado** y [**statusText**](iwinhttprequest-statustext.md)y leer el texto de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, display the **Status** and [**StatusText**](iwinhttprequest-statustext.md), and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the status.
WScript.Echo( WinHttpReq.Status + " - " + WinHttpReq.StatusText);

// Display the date header.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="c7fc3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7fc3-119">Requirements</span></span>



| <span data-ttu-id="c7fc3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7fc3-120">Requirement</span></span> | <span data-ttu-id="c7fc3-121">Value</span><span class="sxs-lookup"><span data-stu-id="c7fc3-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fc3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7fc3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fc3-123">Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]</span><span class="sxs-lookup"><span data-stu-id="c7fc3-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c7fc3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7fc3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fc3-125">Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]</span><span class="sxs-lookup"><span data-stu-id="c7fc3-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c7fc3-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c7fc3-126">Redistributable</span></span><br/>          | <span data-ttu-id="c7fc3-127">WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c7fc3-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c7fc3-128">IDL</span><span class="sxs-lookup"><span data-stu-id="c7fc3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7fc3-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc3-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7fc3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7fc3-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7fc3-131"><dt>Winhttp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc3-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="c7fc3-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7fc3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7fc3-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7fc3-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c7fc3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7fc3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fc3-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c7fc3-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="c7fc3-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c7fc3-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="c7fc3-137">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="c7fc3-137">**StatusText**</span></span>](iwinhttprequest-statustext.md)
</dt> <dt>

[<span data-ttu-id="c7fc3-138">Versiones de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c7fc3-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




