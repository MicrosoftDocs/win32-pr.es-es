---
description: 'Más información acerca de: JetGetBookmark (función)'
title: JetGetBookmark función)
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156808"
---
# <a name="jetgetbookmark-function"></a>JetGetBookmark función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgetbookmark-function"></a>JetGetBookmark función)

La función **JetGetBookmark** recupera el marcador para el registro que está asociado a la entrada de índice en la posición actual de un cursor. Este marcador se puede usar para volver a colocar el cursor en el mismo registro mediante [JetGoToBookmark](./jetgotobookmark-function.md).

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Sesión que se va a usar para esta llamada.

*TABLEID*

Cursor que se va a usar para esta llamada.

*pvBookmark*

Búfer de salida que recibe el marcador.

*cbMax*

Tamaño máximo, en bytes, del búfer de salida.

*pcbActual*

Tamaño real, en bytes, del marcador.

Si este parámetro es **null** , no se devolverá el tamaño real del marcador.

Si el búfer de salida es demasiado pequeño, se seguirá devolviendo el tamaño real del marcador. Esto significa que este número será mayor que el tamaño del búfer de salida.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir todo el marcador. El búfer de salida se ha rellenado con tanta parte del marcador como quepa. También se ha devuelto el tamaño real del marcador, si se solicita.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p><strong>Windows XP:  </strong> Estos valores devueltos se introdujeron en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>El cursor no está situado en un registro. Esto puede ocurrir por diversos motivos. Por ejemplo, esto ocurrirá si el cursor se coloca después del último registro en el índice actual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</p>
<p><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si esta función se ejecuta correctamente, el marcador del registro asociado a la entrada de índice en la posición actual de un cursor se devolverá en el búfer de salida. No se producirá ningún cambio en el estado de la base de datos.

Si se produce un error en esta función, el estado del búfer de salida y del tamaño real del marcador será undefined, a menos que se devuelva JET_errBufferTooSmall. En caso de que se devuelva JET_errBufferTooSmall, el búfer de salida contendrá tantos del marcador como quepan en el espacio proporcionado y el tamaño real del marcador será preciso. No se producirá ningún cambio en el estado de la base de datos.

#### <a name="remarks"></a>Observaciones

Por lo general, los marcadores se deben tratar como fragmentos opacos de datos. No se realiza ningún intento de aprovechar la estructura interna de estos datos. Sin embargo, se cumplen las siguientes condiciones de todos los marcadores ESENT:

  - Un marcador identifica de forma única un registro en una tabla determinada.

  - El marcador de un registro no cambiará durante el período de duración de dicho registro.

  - El marcador de un registro es igual que la clave de ese registro en el índice principal de la tabla que contiene ese registro. Si no se define ningún índice principal sobre esa tabla, el motor de base de datos creará su propio marcador para el registro.

  - Los marcadores se pueden comparar entre sí mediante la función [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su orden relativo en el índice principal sobre la tabla de los registros de origen. Si no se define ningún índice principal sobre esa tabla, no es significativo usar el orden relativo de los marcadores de esa tabla.

  - No tiene sentido comparar los marcadores de los registros de diferentes tablas entre sí.

  - Un marcador siempre es menor o igual que JET_cbBookmarkMost (256) bytes de longitud, antes de Windows Vista.
    
**Windows Vista:** En Windows Vista y versiones posteriores, los marcadores pueden ser mayores que JET_cbBookmarkMost (256) bytes. El tamaño máximo de un marcador es igual al valor actual de JET_paramKeyMost + 1.

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
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
