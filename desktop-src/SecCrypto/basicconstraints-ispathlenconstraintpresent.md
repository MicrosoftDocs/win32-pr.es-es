---
description: Recupera un valor booleano que indica si la restricción de longitud de ruta de acceso está presente.
ms.assetid: 25840a62-13d1-4b54-9b09-64f77a465e06
title: Propiedad BasicConstraints. IsPathLenConstraintPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPathLenConstraintPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9809b6747bac548b14b37384719dbe2660188582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670790"
---
# <a name="basicconstraintsispathlenconstraintpresent-property"></a>Propiedad BasicConstraints. IsPathLenConstraintPresent

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]

La propiedad **IsPathLenConstraintPresent** recupera un valor booleano que indica si la restricción de longitud de ruta de acceso está presente.

## <a name="syntax"></a>Sintaxis


```VB
BasicConstraints.IsPathLenConstraintPresent As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si es **true**, la restricción de longitud de ruta de acceso está presente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
