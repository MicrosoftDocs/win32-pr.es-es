---
description: Nombre de ModemDMConfigProfile \/ (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_Name
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Nombre (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5db3565-db0a-4e6d-a0c5-7e9b3d006d5d
api_name:
- Name
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 40fc710649d5e1cb87f69d8358ba5706492b6c5f
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388771"
---
# <a name="span-idwwan_profile_v4element_1_namespanmodemdmconfigprofilename-v4"></a><span data-ttu-id="7e11c-103"><span id="WWAN_profile_v4.element_1_Name"></span>Nombre de ModemDMConfigProfile \/ (v4)</span><span class="sxs-lookup"><span data-stu-id="7e11c-103"><span id="WWAN_profile_v4.element_1_Name"></span>ModemDMConfigProfile\/Name (v4)</span></span>

<span data-ttu-id="7e11c-104">Nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="7e11c-104">The name of the profile.</span></span> <span data-ttu-id="7e11c-105">Para obtener más información, vea la documentación del elemento de [**nombre**](./schema-name-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="7e11c-105">For more information, see the documentation for the v1 [**Name**](./schema-name-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="7e11c-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="7e11c-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Name\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Name\>**

## <a name="syntax"></a><span data-ttu-id="7e11c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e11c-107">Syntax</span></span>

``` syntax
<Name>

  nameType

</Name>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="7e11c-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7e11c-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="7e11c-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="7e11c-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="7e11c-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7e11c-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="7e11c-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e11c-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="7e11c-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7e11c-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="7e11c-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7e11c-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e11c-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="7e11c-114">Parent Element</span></span></th>
<th><span data-ttu-id="7e11c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e11c-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e11c-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="7e11c-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="7e11c-117">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="7e11c-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="7e11c-118">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="7e11c-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="7e11c-119">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="7e11c-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="7e11c-120">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="7e11c-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e11c-121"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="7e11c-121"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="7e11c-122">Perfil de configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="7e11c-122">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="7e11c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e11c-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e11c-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e11c-124">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
