---
description: Contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: profileList (WLANPolicy), elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678305"
---
# <a name="profilelist-wlanpolicy-element"></a>profileList (WLANPolicy), elemento

El elemento profileList (WLANPolicy) contiene una lista de perfiles que se van a aplicar en el nivel de dominio o de equipo. Este elemento es opcional. Si este elemento está presente, debe contener al menos un perfil.

Los perfiles deben basarse en [el \_ esquema de Perfil de WLAN](wlan-profileschema-schema.md), con un elemento raíz de [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento **profileList** se define mediante el elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




