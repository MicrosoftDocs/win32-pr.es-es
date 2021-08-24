---
title: Método CreateInstanceFromPropertyData de la MicrosoftDNS_ATMAType clase
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos atma (Atma) de dirección DE ATM.
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- Dns del método CreateInstanceFromPropertyData
- Método DNS CreateInstanceFromPropertyData , MicrosoftDNS_ATMAType clase
- MicrosoftDNS_ATMAType clase DNS , método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44edf3428087da73f5ba89c32232af0ae589bc0d865642ec04953c62e16404e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539325"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a>Método CreateInstanceFromPropertyData de la clase MICROSOFTDNS \_ ATMAType

El **método CreateInstanceFromPropertyData** crea una instancia de un registro de recursos atma (ATMA) de una dirección ATM.

## <a name="syntax"></a>Sintaxis


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DnsServerName* \[ En\]
</dt> <dd>

FQDN o dirección IP del servidor DNS que contiene este RR.

</dd> <dt>

*ContainerName* \[ En\]
</dt> <dd>

Nombre del contenedor de la instancia de Zone, Cache o RootHints que contiene este RR.

</dd> <dt>

*OwnerName* \[ En\]
</dt> <dd>

Nombre del propietario del RR.

</dd> <dt>

*RecordClass* \[ en, opcional\]
</dt> <dd>

Clase del RR. El valor predeterminado es 1. Los valores siguientes son válidos.



| Value                                                                                                | Significado                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ en, opcional\]
</dt> <dd>

Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Formato de dirección ATM. Dos valores posibles para FORMAT son: 0 que indica el formato de dirección del sistema de finalización de ATM (AESA) y 1 que indica el formato E.164.

</dd> <dt>

*ATMAddress* \[ En\]
</dt> <dd>

Cadena de longitud variable de octetos que contiene la dirección ATM del nodo o propietario al que pertenece este RR. Los cuatro primeros bytes de la matriz se usan para almacenar el tamaño de la cadena de octeto. El byte más significativo se almacena en byte 0.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Referencia al nuevo objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**Método Modify de la clase ATMAType de MicrosoftDNS \_**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





