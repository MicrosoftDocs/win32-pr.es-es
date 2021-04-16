---
description: MBNProfileExt \/ ... \/ IPType (v4)
MS-HAID: WWAN\_profile\_v4.element\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918355cdfc90863539da5f29aff542654a95f5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542195"
---
# <a name="span-idwwan_profile_v4element_iptypespanmbnprofileextiptype-v4"></a><span data-ttu-id="99536-103"><span id="WWAN_profile_v4.element_IPType"></span>MBNProfileExt \/ ... \/ IPType (v4)</span><span class="sxs-lookup"><span data-stu-id="99536-103"><span id="WWAN_profile_v4.element_IPType"></span>MBNProfileExt\/...\/IPType (v4)</span></span>

<span data-ttu-id="99536-104">Especifica el tipo de IP que se va a usar en esta conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="99536-104">Specifies the IP type to be used on this data connection.</span></span>

<span data-ttu-id="99536-105">Este elemento es nuevo en V4 del esquema.</span><span class="sxs-lookup"><span data-stu-id="99536-105">This element is new in v4 of the schema.</span></span> <span data-ttu-id="99536-106">El elemento puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="99536-106">The element can have one of the following values.</span></span>

| <span data-ttu-id="99536-107">Value</span><span class="sxs-lookup"><span data-stu-id="99536-107">Value</span></span>   | <span data-ttu-id="99536-108">Significado</span><span class="sxs-lookup"><span data-stu-id="99536-108">Meaning</span></span>                                       |
|---------|-----------------------------------------------|
| <span data-ttu-id="99536-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="99536-109">Default</span></span> | <span data-ttu-id="99536-110">El tipo de IP se va a seleccionar por las capas inferiores</span><span class="sxs-lookup"><span data-stu-id="99536-110">IP type is to be picked by lower layer(s)</span></span>     |
| <span data-ttu-id="99536-111">IPv4</span><span class="sxs-lookup"><span data-stu-id="99536-111">IPv4</span></span>    | <span data-ttu-id="99536-112">Usar IPv4</span><span class="sxs-lookup"><span data-stu-id="99536-112">Use IPv4</span></span>                                      |
| <span data-ttu-id="99536-113">IPv6</span><span class="sxs-lookup"><span data-stu-id="99536-113">IPv6</span></span>    | <span data-ttu-id="99536-114">Usar IPv6</span><span class="sxs-lookup"><span data-stu-id="99536-114">Use IPv6</span></span>                                      |
| <span data-ttu-id="99536-115">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="99536-115">IPv4v6</span></span>  | <span data-ttu-id="99536-116">Usar IPv4 y/o IPv6, como están disponibles.</span><span class="sxs-lookup"><span data-stu-id="99536-116">Use IPv4 and/or IPv6, as available.</span></span>           |
| <span data-ttu-id="99536-117">XLAT</span><span class="sxs-lookup"><span data-stu-id="99536-117">XLAT</span></span>    | <span data-ttu-id="99536-118">Usar 464XLAT para canalizar redes IPv4 a través de IPv6</span><span class="sxs-lookup"><span data-stu-id="99536-118">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="99536-119">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="99536-119">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a><span data-ttu-id="99536-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99536-120">Syntax</span></span>

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="99536-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="99536-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="99536-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="99536-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="99536-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="99536-123">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="99536-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="99536-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="99536-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="99536-125">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="99536-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="99536-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="99536-127">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="99536-127">Parent Element</span></span></th>
<th><span data-ttu-id="99536-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="99536-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="99536-129"><a href="element-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="99536-129"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="99536-130">Especifica los parámetros necesarios para establecer una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="99536-130">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="99536-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99536-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="99536-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99536-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



