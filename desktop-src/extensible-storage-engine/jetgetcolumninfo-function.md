---
description: 'Más información acerca de: JetGetColumnInfo (función)'
title: Función JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716512"
---
# <a name="jetgetcolumninfo-function"></a>Función JetGetColumnInfo


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetcolumninfo-function"></a>Función JetGetColumnInfo

La función **JetGetColumnInfo** recupera información acerca de una columna.

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para la llamada API.

*DBID*

Identifica, junto con *szTableName*, la tabla que contiene la columna de la que se recupera la información.

*szTableName*

Identifica, junto con *DBID*, la tabla que contiene la columna de la que se recupera la información.

*szColumnName*

Nombre de la columna para la que se captura la información.

*pvResult*

Puntero a un búfer que recibirá la información. El tipo de búfer depende de *InfoLevel*. El autor de la llamada debe estar configurado para alinear el búfer adecuadamente.

*cbMax*

Tamaño, en bytes, del búfer que se pasa en *pvResult*.

*InfoLevel*

Tipo de información que se va a recuperar para la columna especificada por *szColumnName*. El formato de los datos almacenados en *pvResult* depende de este parámetro. Para obtener el esquema de la tabla temporal, vea [JET_COLUMNLIST](./jet-columnlist-structure.md).

Estos *InfoLevels* se diferencian en lo siguiente:

  - JET_ColInfoListSortColumnid ordenará la tabla temporal por *columnid*.

  - JET_ColInfoListCompact compactará la salida. Para obtener más información sobre la salida de Compact, consulte [JET_COLUMNLIST](./jet-columnlist-structure.md).

Las siguientes opciones están disponibles para su uso con este parámetro.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ColInfo</p></td>
<td><p>JET_ColInfo y JET_ColInfoByColid recuperan la misma información. <em>pvResult</em> se interpreta como un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>y los campos de la estructura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> se rellenan de forma adecuada.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Esto es similar a una estructura de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Si esta función se ejecuta correctamente, la estructura se rellena con los valores adecuados. Si se produce un error en esta función, la estructura contiene datos sin definir.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p>Como JET_ColInfo, <em>pvResult</em> se interpreta como un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, con la excepción de que <em>InfoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a una <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>pvResult</em> se interpreta como una estructura de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Si esta función se ejecuta correctamente, la estructura se rellena con los valores adecuados. Se abre una tabla temporal que se identifica mediante el miembro <strong>TABLEID</strong> de la estructura <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . La tabla debe cerrarse con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Si se produce un error en esta función, la estructura contiene datos sin definir.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p>Igual que JET_ColInfoList.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>Igual que JET_ColInfoList; sin embargo, la tabla resultante se ordena por columnid, en lugar de por nombre de columna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor está en desuso y el uso de él devolverá JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>Como JET_ColInfoBase, <em>pvResult</em> se interpreta como un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, con la excepción de que <em>InfoLevel</em> indica que la columna solicitada (<em>szColumName</em>) no es el nombre de la columna de cadena, sino un puntero a una <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p>
<p><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>Devolver solo columnas no derivadas (si la tabla se deriva de una plantilla).</p>
<p>Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>Devuelva solo el nombre de columna y el columnid de cada columna.</p>
<p>Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>Orden devuelto de la lista de columnas por columnid (el valor predeterminado es ordenar la lista por nombre de columna).</p>
<p>Este valor puede ser lógicamente o debe encontrarse en el <em>InfoLevel</em>, cuando el <em>InfoLevel</em> base está JET_ColInfoList.</p>
<p><strong>Windows Vista:  </strong> Este valor se introduce en Windows Vista.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>No se encontró la columna denominada <em>szColumnName</em> en la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Se ha especificado un <em>InfoLevel</em> incorrecto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Este error se puede devolver si:</p>
<ul>
<li><p>Se proporcionó un nombre incorrecto para <em>szTableName</em> .</p></li>
<li><p>Se proporcionó un nombre incorrecto para <em>szColumnName</em> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Este error se puede devolver si:</p>
<ul>
<li><p>Se ha especificado un <em>InfoLevel</em> incorrecto.</p></li>
<li><p>Se pasó un valor de <em>szTableName</em> nulo.</p></li>
<li><p>El búfer es demasiado pequeño.</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) y **JetGetColumnInfo** recuperan información sobre una columna. La diferencia entre ellos es cómo se identifica la tabla:

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifica una tabla mediante *TABLEID*.

  - **JetGetColumnInfo** identifica una tabla por la combinación de *DBID* y *szTableName* .

Al recuperar datos con JET_ColInfoList, JET_ColInfoListSortColumnid o JET_ColInfoListCompact, se abrirá una tabla temporal. La tabla temporal contiene datos y la estructura [JET_COLUMNLIST](./jet-columnlist-structure.md) contiene información suficiente para atravesar la tabla temporal. La tabla temporal debe cerrarse con [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetGetColumnInfoW</strong> (Unicode) y <strong>JetGetColumnInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[Parámetros de control de errores](./error-handling-parameters.md)  
[Errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
