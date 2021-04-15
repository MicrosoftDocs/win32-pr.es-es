---
title: Cuenta deshabilitada (proveedor de WinNT)
description: Cuando se usa el proveedor de WinNT, se puede habilitar o deshabilitar una cuenta mediante la propiedad IADsUser. AccountDisabled.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Cuenta deshabilitada (proveedor de WinNT)
- Cuenta ADSI deshabilitada, proveedor de Winnt
- Proveedor de WinNT ADSI, ejemplos de administración de usuarios, cuenta deshabilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99b1fe45b71eda14547703f8721b2a13d581b8e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104424303"
---
# <a name="account-disabled-winnt-provider"></a>Cuenta deshabilitada (proveedor de WinNT)

Cuando se usa el proveedor de WinNT, se puede habilitar o deshabilitar una cuenta mediante la propiedad [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) .

## <a name="example-1"></a>Ejemplo 1

En el ejemplo de código siguiente se muestra cómo deshabilitar una cuenta mediante Visual Basic con ADSI.


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a>Ejemplo 2

En el ejemplo de código siguiente se muestra cómo deshabilitar una cuenta mediante C++ con ADSI.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




