---
title: Método Modify de la clase MicrosoftDNS_MDType
description: El método Modify actualiza un registro de recursos de agente de correo para el dominio (MD).
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- Modificar DNS de método
- Modificar el método DNS, MicrosoftDNS_MDType clase
- MicrosoftDNS_MDType de clase DNS, Modify (método)
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150258"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a>Método Modify de la \_ clase MicrosoftDNS MDType

El método **Modify** actualiza un registro de recursos de agente de correo para el dominio (MD).

## <a name="syntax"></a>Sintaxis


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TTL* \[ de en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*MDHost* \[ en, opcional\]
</dt> <dd>

Cadena que representa el host de entrega de correo.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Referencia al objeto modificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los parámetros no especificados se dejan sin cambios en el registro modificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MDType**](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





