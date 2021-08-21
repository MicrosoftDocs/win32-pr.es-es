---
description: 'Más información sobre: Miembros systemParameters'
title: Miembros SystemParameters
TOCTitle: SystemParameters members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.SystemParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters_members(v=EXCHG.10)
ms:contentKeyID: 55104101
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d2ad43871c768955f98c0e372adde37cd731f8f4689bcb05b21f7e169bed715c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071002"
---
# <a name="systemparameters-members"></a>Miembros SystemParameters

Incluir miembros protegidos  
Incluir miembros heredados  

Constantes para la API de ESENT. Estos no tienen que buscarse a través de parámetros del sistema. Esta clase proporciona propiedades estáticas para establecer y obtener parámetros globales del sistema ESENT. Esta clase proporciona propiedades estáticas para establecer y obtener parámetros globales del sistema ESENT.

El [tipo SystemParameters](./systemparameters-class.md) expone los miembros siguientes.

## <a name="properties"></a>Propiedades

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351215(v=exchg.10).md">BookmarkMost</a></td>
<td>Obtiene el tamaño máximo de un marcador. <a href="dn292149(v=exchg.10).md">JetGetBookmark(JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351214(v=exchg.10).md">CacheSize</a></td>
<td>Obtiene o establece el tamaño de la caché de base de datos en páginas. De forma predeterminada, la memoria caché de la base de datos ajustará automáticamente su tamaño, al establecer esta propiedad en un valor distinto de cero, la memoria caché se ajustará al tamaño de destino.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351149(v=exchg.10).md">CacheSizeMax</a></td>
<td>Obtiene o establece el tamaño máximo de la caché de páginas de la base de datos. El tamaño está en páginas de base de datos. Si este parámetro se deja en su valor predeterminado, el tamaño máximo de la memoria caché se establecerá en el tamaño de la memoria física cuando se llame a JetInit.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351216(v=exchg.10).md">CacheSizeMin</a></td>
<td>Obtiene o establece el tamaño mínimo de la caché de páginas de base de datos, en páginas de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351151(v=exchg.10).md">ColumnsKeyMost</a></td>
<td>Obtiene el número máximo de componentes de una clave de ordenación o índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351218(v=exchg.10).md">Configuración</a></td>
<td>Obtiene o establece un valor que especifica los valores predeterminados para todo el conjunto de parámetros del sistema. Cuando este parámetro se establece en una configuración específica, todos los valores de parámetro del sistema se restablecen a sus valores predeterminados para esa configuración. Si la configuración se establece para una instancia específica, los parámetros globales del sistema no se restablecerán a sus valores predeterminados. Configuración pequeña (0): el motor de base de datos está optimizado para su uso en memoria. Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales. Compatible con Windows Vista y versiones 2. Se omite en Windows XP y Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351153(v=exchg.10).md">DatabasePageSize</a></td>
<td>Obtiene o establece el tamaño de las páginas de la base de datos, en bytes.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351221(v=exchg.10).md">EnableAdvanced</a></td>
<td>Obtiene o establece un valor que indica si el motor de base de datos acepta o rechaza los cambios en un subconjunto de los parámetros del sistema. Este parámetro se usa junto con <a href="dn351218(v=exchg.10).md">Configuration</a> para evitar que algunos parámetros del sistema se establezcan fuera de los valores predeterminados de la configuración seleccionada. Compatible con Windows Vista y versiones 2. Se omite en Windows XP y Windows Server 2003.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351152(v=exchg.10).md">EnableFileCache</a></td>
<td>Obtiene o establece un valor que indica si el motor de base de datos debe usar la caché de archivos del sistema operativo para todos los archivos administrados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351220(v=exchg.10).md">EnableViewCache</a></td>
<td>Obtiene o establece un valor que indica si el motor de base de datos debe usar E/S de archivos asignados a memoria para los archivos de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351223(v=exchg.10).md">EventLoggingLevel</a></td>
<td>Obtiene o establece el nivel de detalle de los mensajes del registro de eventos que el motor de base de datos emite al registro de eventos. Los números más altos darán como resultado mensajes de registro de eventos más detallados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351154(v=exchg.10).md">ExceptionAction</a></td>
<td>Obtiene o establece el valor que codifica qué hacer con las excepciones generadas en JET.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351227(v=exchg.10).md">HungIOActions</a></td>
<td>Obtiene o establece el conjunto de acciones que se realizarán en las E/S que aparecen como no ejecutadas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351155(v=exchg.10).md">HungIOThreshold</a></td>
<td>Obtiene o establece el umbral para lo que se considera una E/S fija sobre la que se debe actuar.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351156(v=exchg.10).md">KeyMost</a></td>
<td>Obtiene el tamaño máximo de la clave. Esto depende del tamaño de página de la base de datos y la versión de Esent.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351229(v=exchg.10).md">LegacyFileNames</a></td>
<td>Obtiene o establece la compatibilidad con versiones anteriores con las convenciones de nomenclatura de archivos de versiones anteriores del motor de base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351157(v=exchg.10).md">LVChunkSizeMost</a></td>
<td>Obtiene el tamaño de los fragmentos lv. Esto depende del tamaño de página de la base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351230(v=exchg.10).md">MaxInstances</a></td>
<td>Obtiene o establece el número máximo de instancias que se pueden crear.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351160(v=exchg.10).md">MinDataForXpress</a></td>
<td>Obtiene o establece la menor cantidad de datos que se deben comprimir con compresión xpress.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351159(v=exchg.10).md">OutstandingIOMax</a></td>
<td>Este parámetro controla cuántas E/S de archivos de base de datos se pueden poner en cola por disco en el sistema operativo host a la vez. Un valor mayor para este parámetro puede ayudar significativamente al rendimiento de una aplicación de base de datos grande.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351158(v=exchg.10).md">ProcessFriendlyName</a></td>
<td>Obtiene o establece el nombre descriptivo de esta instancia del proceso.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351161(v=exchg.10).md">StartFlushThreshold</a></td>
<td>Obtiene o establece el umbral en el que la caché de páginas de la base de datos comienza a expulsar páginas de la memoria caché para hacer espacio para las páginas que no están almacenadas en caché. Cuando el número de búferes de página de la memoria caché cae por debajo de este umbral, se inicia un proceso en segundo plano para reponer ese grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de caché establecido por JET_paramCacheSizeMax. Este umbral también debe ser siempre menor que el umbral de detección establecido por JET_paramStopFlushThreshold. El alto de distancia del umbral de inicio determinará el tiempo de respuesta que debe tener la caché de páginas de la base de datos para generar búferes disponibles antes de que la aplicación los necesite. Un umbral de inicio alto dará al proceso en segundo plano más tiempo para reaccionar. Sin embargo, un umbral de inicio alto implica un umbral de detección más alto y eso reducirá el tamaño efectivo de la caché de páginas de la base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351231(v=exchg.10).md">StopFlushThreshold</a></td>
<td>Obtiene o establece el umbral en el que la caché de páginas de la base de datos termina expulsando páginas de la memoria caché para dar espacio a las páginas que no están almacenadas en caché. Cuando el número de búferes de página de la memoria caché supera este umbral, se detiene el proceso en segundo plano que se inició para reponer ese grupo de búferes disponibles. Este umbral siempre es relativo al tamaño máximo de caché establecido por JET_paramCacheSizeMax. Este umbral también debe ser siempre mayor que el umbral inicial establecido por JET_paramStartFlushThreshold. La distancia entre el umbral inicial y el umbral de detección afecta a la eficacia con la que el proceso en segundo plano vacía las páginas de la base de datos. Una brecha mayor hará que sea más probable que se combinen las escrituras en páginas vecinos. Sin embargo, un umbral de detección alto reducirá el tamaño efectivo de la caché de páginas de la base de datos.</td>
</tr>
</tbody>
</table>


Superior

## <a name="fields"></a>Campos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351208(v=exchg.10).md">BaseNameLength</a></td>
<td>Longitud del prefijo utilizado para dar nombre a los archivos utilizados por el motor de base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351146(v=exchg.10).md">ColumnMost</a></td>
<td>Tamaño máximo de las columnas que no se JET_coltyp. LongBinary o JET_coltyp. LongText.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351210(v=exchg.10).md">ColumnsFixedMost</a></td>
<td>Número máximo de columnas fijas permitidas en una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351140(v=exchg.10).md">ColumnsMost</a></td>
<td>Número máximo de columnas permitidas en una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351148(v=exchg.10).md">ColumnsTaggedMost</a></td>
<td>Número máximo de columnas etiquetadas permitidas en una tabla.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351212(v=exchg.10).md">ColumnsVarMost</a></td>
<td>Número máximo de columnas de longitud variable permitidas en una tabla.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351141(v=exchg.10).md">LocaleNameMaxLength</a></td>
<td>Longitud máxima de un nombre de configuración regional (LOCALE_NAME_MAX_LENGTH de winnt.h).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351213(v=exchg.10).md">NameMost</a></td>
<td>Tamaño máximo de un nombre de tabla, columna o índice.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a></td>
<td>Número de páginas que proporciona la base de datos temporal más pequeña posible.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[SystemParameters (clase)](./systemparameters-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
