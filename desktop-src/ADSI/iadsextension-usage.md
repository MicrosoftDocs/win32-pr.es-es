---
title: Uso de IADsExtension
description: Este tema contiene ejemplos de código de C++ para usar la interfaz IADsExtension.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbab6813a87701fe2d7e130a03540476412c9e13b9d5d3ca96bdd0e63b2dad54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023493"
---
# <a name="iadsextension-usage"></a>Uso de IADsExtension

[**IADsExtension es una**](/windows/desktop/api/Iads/nn-iads-iadsextension) interfaz opcional implementada por el escritor de extensiones cuando se cumple al menos una de las condiciones siguientes:

-   El componente de extensión requiere una notificación de inicialización tal como se define en **ADSI \_ EXT \_ *dwCode*** en el [**método Operate.**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate)
-   La extensión admite una interfaz dual o de distribución.

Si un componente de extensión admite la [**interfaz IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) por primera vez, los [**métodos IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**IADsExtension::P rivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) pueden devolver **E \_ NOTIMPL**. Como alternativa, si un componente de extensión admite una interfaz dual o de distribución , el [**método Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) puede omitir los datos y devolver un **valor HRESULT** de **E \_ NOTIMPL**.

El código siguiente muestra una extensión que implementa [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).


```C++
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
    HRESULT hr = S_OK;
    switch (dwCode) 
    {
    case ADS_EXT_INIT:
         // Prompt for a credential.
         // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);
          break;
    default:
          hr = E_FAIL;
          break;
    }        
    return hr;        
}
 
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{        
      if (rgdispid == NULL)
      {
        return E_POINTER;
      }    
    return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
 
STDMETHOD(PrivateInvoke)(DISPID dispidMember, REFIID riid, LCID lcid, WORD wFlags, DISPPARAMS * pdispparams, VARIANT * pvarResult, EXCEPINFO * pexcepinfo, UINT * puArgErr)
{
 return DispInvoke( (IHelloWorld*)this, 
           m_pTypeInfo,
        dispidMember, 
        wFlags, 
        pdispparams, 
        pvarResult, 
        pexcepinfo, 
        puArgErr );
}
```



 

 




