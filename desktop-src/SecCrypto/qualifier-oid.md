---
description: Recupera el identificador de objeto del calificador.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Propiedad Qualifier. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690506"
---
# <a name="qualifieroid-property"></a>Propiedad Qualifier. OID

\[La propiedad **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]

La propiedad **OID** recupera el ID. de objeto del calificador. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**OID**](oid.md) que identifica el calificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Qualifier**](qualifier.md)
</dt> </dl>

 

 
