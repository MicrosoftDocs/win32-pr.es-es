---
description: MmscUrl
MS-HAID: WWAN\_profile\_v4.element\_MmscUrl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscUrl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24bf6cee6ee20a9906238db851eb72f4dfe47d10
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480271"
---
# <a name="span-idwwan_profile_v4element_mmscurlspanmmscurl"></a><span id="WWAN_profile_v4.element_MmscUrl"></span>MmscUrl

Especifica la dirección URL del servidor MMSC para el dispositivo. Opcional.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscUrl>**

## <a name="syntax"></a>Syntax

``` syntax
<MmscUrl>

  anyURI

</MmscUrl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

Ninguno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios


| Elemento primario | Descripción | 
|----------------|-------------|
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>Información de configuración para El servicio de mensajería multimedia (MMS).</p><p>Además de establecer los elementos de configuración dentro de este elemento, un perfil mms debe tener la siguiente configuración.</p><ul><li>Su <a href="element-name.md"><strong>elemento Name</strong></a> debe contener un nombre único para todo el sistema.</li><li>Su <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> debe establecerse en <strong>UserProvisioned.</strong></li><li>Su <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> debe contener el VALOR DEID DE LA SIM para la que está pensado este perfil.</li><li>Su <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> debe establecerse en <strong>Manual.</strong></li><li>Su <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> debe contener el GUID para el grupo de propósito de MMS.</li><li>Su <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> debe establecerse en <strong>true.</strong></li></ul> | 


 

## <a name="requirements"></a>Requisitos


| | | <p>Espacio de nombres</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
