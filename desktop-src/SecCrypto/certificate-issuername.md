---
description: Recupera una cadena que contiene el nombre del emisor del certificado.
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Propiedad Certificate.IssuerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f4404a105748a79ef942f37c088a5436fc3eeea0784bb6ff814dd0782262dcf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771589"
---
# <a name="certificateissuername-property"></a>Propiedad Certificate.IssuerName

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad IssuerName** recupera una cadena que contiene el nombre del emisor del certificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a>Valor de propiedad

Cadena que contiene el nombre del emisor del certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
