---
description: Recupera un valor booleano que indica si el certificado es para una entidad de certificación (CA).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: BasicConstraints.IsCertificateAuthority, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 90d616f4a7a0fe8522118848826bee88523ad45c34cb8a3fff23c722e68f2495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879765"
---
# <a name="basicconstraintsiscertificateauthority-property"></a>BasicConstraints.IsCertificateAuthority, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use la clase [**X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

La **propiedad IsCertificateAuthority** recupera un valor booleano que indica si el certificado es para una entidad [*de certificación*](../secgloss/c-gly.md) (CA).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es True**, el certificado solo lo usará una entidad de certificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
