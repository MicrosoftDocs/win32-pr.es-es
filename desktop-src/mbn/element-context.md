---
description: Contexto de MBNProfileExt \/ (v4)
MS-HAID: WWAN\_profile\_v4.element\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Context
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eff61884-1d37-4e1a-85f0-2fadf14227ac
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8ec231b5d7e2769d86262864e0b9a53621c36a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720357"
---
# <a name="span-idwwan_profile_v4element_contextspanmbnprofileextcontext-v4"></a><span id="WWAN_profile_v4.element_Context"></span>Contexto de MBNProfileExt \/ (v4)

Especifica los parámetros necesarios para establecer una conexión de datos.

## <a name="element-hierarchy"></a>Jerarquía de elemento

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a>Sintaxis

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a>Clave

`?`   opcional (cero o uno)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Ninguno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento secundario</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-accessstring.md">AccessString</a></td>
<td><p>Identifica el APN o la cadena de marcado que se va a utilizar para establecer una conexión de datos.</p>
<p>Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-authprotocol.md">AuthProtocol</a></td>
<td><p>>Especifica el protocolo de autenticación que se va a utilizar para activar un contexto del Protocolo de datos de paquetes (PDP).</p>
<p>Tenga en cuenta que en V4, hay un nuevo valor de enumeración disponible para este elemento. <strong>La selección activa</strong> significa que un protocolo de autenticación se va a seleccionar por las capas inferiores.</p>
<p>Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-compression.md">Compresión</a></td>
<td><p>Especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos.</p>
<p>Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-iptype.md">IPType</a></td>
<td><p>Especifica el tipo de IP que se va a usar en esta conexión de datos.</p>
<p>Este elemento es nuevo en V4 del esquema. El elemento puede tener uno de los valores siguientes.</p>
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor predeterminado</td>
<td>El tipo de IP se va a seleccionar por las capas inferiores</td>
</tr>
<tr class="even">
<td>IPv4</td>
<td>Usar IPv4</td>
</tr>
<tr class="odd">
<td>IPv6</td>
<td>Usar IPv6</td>
</tr>
<tr class="even">
<td>IPv4v6</td>
<td>Usar IPv4 y/o IPv6, como están disponibles.</td>
</tr>
<tr class="odd">
<td>XLAT</td>
<td>Usar 464XLAT para canalizar redes IPv4 a través de IPv6</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><a href="element-userlogoncred.md">UserLogonCred</a></td>
<td><p>Credenciales de inicio de sesión para una conexión.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento primario</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior. Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</p>
<p>Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento. Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</p></td>
</tr>
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Perfil de configuración de DM de módem.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Espacio de nombres</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



