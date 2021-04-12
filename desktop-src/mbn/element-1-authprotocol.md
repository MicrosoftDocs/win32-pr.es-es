---
description: ModemDMConfigProfile \/ ... \/ AuthProtocol (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_AuthProtocol
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AuthProtocol
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5e6c5a25-fe9e-4d0a-8b5b-4ff585f562af
api_name:
- AuthProtocol
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7a935d7367589a3043fdd9d064935d0c0dd64b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541427"
---
# <a name="span-idwwan_profile_v4element_1_authprotocolspanmodemdmconfigprofileauthprotocol-v4"></a><span data-ttu-id="a3359-103"><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>ModemDMConfigProfile \/ ... \/ AuthProtocol (v4)</span><span class="sxs-lookup"><span data-stu-id="a3359-103"><span id="WWAN_profile_v4.element_1_AuthProtocol"></span>ModemDMConfigProfile\/...\/AuthProtocol (v4)</span></span>

><span data-ttu-id="a3359-104">Especifica el protocolo de autenticación que se va a utilizar para activar un contexto del Protocolo de datos de paquetes (PDP).</span><span class="sxs-lookup"><span data-stu-id="a3359-104">Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="a3359-105">Tenga en cuenta que en V4, hay un nuevo valor de enumeración disponible para este elemento.</span><span class="sxs-lookup"><span data-stu-id="a3359-105">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="a3359-106">**La selección activa** significa que un protocolo de autenticación se va a seleccionar por las capas inferiores.</span><span class="sxs-lookup"><span data-stu-id="a3359-106">**AutoSelection** means that an auth protocol is to be picked by lower layer(s).</span></span>

<span data-ttu-id="a3359-107">Para obtener más información, consulte la documentación del elemento [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="a3359-107">For further information, see the documentation for the v1 [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a3359-108">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="a3359-108">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

## <a name="syntax"></a><span data-ttu-id="a3359-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3359-109">Syntax</span></span>

``` syntax
<AuthProtocol>

  "NONE" | "PAP" | "CHAP" | "MsCHAPv2" | "AutoSelection"

</AuthProtocol>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a3359-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a3359-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a3359-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="a3359-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a3359-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a3359-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a3359-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a3359-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="a3359-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a3359-114">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a3359-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a3359-115"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3359-116">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a3359-116">Parent Element</span></span></th>
<th><span data-ttu-id="a3359-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3359-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3359-118"><a href="element-1-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="a3359-118"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="a3359-119">Especifica los parámetros necesarios para establecer una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="a3359-119">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="a3359-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3359-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3359-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3359-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
