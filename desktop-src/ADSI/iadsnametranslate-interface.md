---
title: Interfaz IADsNameTranslate
description: La interfaz IADsNameTranslate se usa para traducir nombres distintivos entre distintos formatos. Las traducciones de nombres se realizan en el servidor de directorio y esta interfaz solo está disponible para los objetos de Active Directory.
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- Interfaz IADsNameTranslate ADSI
- IADsTranslate ADSI, usar
- ADSI ADSI, código de ejemplo C/C++, uso de IADsTranslate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ff5b44288289f118c41463a22e619aa815ecb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903050"
---
# <a name="iadsnametranslate-interface"></a>Interfaz IADsNameTranslate

La interfaz [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) se usa para traducir nombres distintivos entre distintos formatos. Las traducciones de nombres se realizan en el servidor de directorio y esta interfaz solo está disponible para los objetos de Active Directory.

En el siguiente ejemplo de código se convierte un nombre de cuenta del formato de Windows al formato LDAP.


```C++
HRESULT TranslateNTNameToLDAPName( BSTR * pNTName, BSTR * pLDAPName )
{
    IADsNameTranslate *pTrans;
    HRESULT hr = S_OK;
 
    hr = CoCreateInstance(CLSID_NameTranslate, 
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsNameTranslate,
                          (void**) &pTrans );
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Init(ADS_NAME_INITTYPE_DOMAIN, 
                      CComBSTR("Fabrikam.com"));
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Set(ADS_NAME_TYPE_NT4, *pNTName);
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Get(ADS_NAME_TYPE_1779, pLDAPName);
    pTrans->Release();
    return hr;
}
```



 

 




