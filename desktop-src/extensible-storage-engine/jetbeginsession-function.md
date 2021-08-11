---
description: 'Más información sobre: JetBeginSession (Función)'
title: Función JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0852de04f3969e3e30debc7ba7ff4f3aedf7ac4084b17f91feed8984fe4e1467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251619"
---
# <a name="jetbeginsession-function"></a>Función JetBeginSession


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetbeginsession-function"></a>Función JetBeginSession

La **función JetBeginSession** inicia una sesión e inicializa y devuelve un identificador de sesión ese [(JET_SESID](./jet-sesid.md)). Las sesiones controlan todo el acceso a la base de datos y se usan para controlar el ámbito de las transacciones. La sesión se puede usar para iniciar, confirmar o anular transacciones. La sesión también se usa para adjuntar, crear o abrir una base de datos. La sesión se usa como contexto para todas las operaciones DDL y DML. Para aumentar la simultaneidad y el acceso paralelo a la base de datos, se pueden iniciar varias sesiones.

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>Parámetros

*Ejemplo*

Instancia de base de datos que se va a usar para esta llamada.

*psesid*

Puntero a la variable que el identificador de sesión inicializa al devolverse correctamente.

*szUserName*

Este parámetro está reservado.

*szPassword*

Este parámetro está reservado.

### <a name="return-value"></a>Valor devuelto

Esta función permite la devolución de cualquier [JET_ERR](./jet-err.md)que se definen en esta API. Para obtener más información sobre los errores de Jet, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</p>
<p>Este error solo lo devolverán Windows XP y versiones posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los parámetros proporcionados contenía un valor inesperado o un valor que no tenía sentido cuando se combinaba con el valor de otro parámetro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Error en la operación porque no se pudo asignar memoria.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>El número de sesiones que el motor permitirá que el cliente inicie es limitado. Este valor se puede cambiar mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con la JET_paramMaxSessions constante. El número predeterminado de sesiones es 16. Consulte <a href="gg294139(v=exchg.10).md">Parámetros del sistema</a> para obtener más información sobre JET_paramMaxSessions.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</p></td>
</tr>
</tbody>
</table>


Si se ejecuta correctamente, se inicializa el identificador de sesión y se puede usar para las operaciones de base de datos.

En caso de error, no hay sesiones disponibles o no se pudo inicializar una nueva sesión.

#### <a name="remarks"></a>Comentarios

Se debe prestar mucha atención al usar sesiones en distintos subprocesos. Una sesión realiza un seguimiento del subproceso en el que se usó durante [JetBeginTransaction,](./jetbegintransaction-function.md) [JetCommitTransaction](./jetcommittransaction-function.md)o [JetRollback,](./jetrollback-function.md)y producirá un error si se usa en varios subprocesos con una transacción abierta. [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) puede cambiar este comportamiento. Puesto que la sesión sigue siendo un contexto serializado y no se pueden realizar varias operaciones de base de datos en una sola sesión simultáneamente, solo en serie. Sin embargo, puede usar varias sesiones para lograr el acceso simultáneo a la base de datos. Las sesiones se pueden usar dentro de una transacción entre subprocesos estableciendo y restableciendo los contextos de sesión.

El identificador de sesión debe cerrarse [con JetEndSession](./jetendsession-function.md).

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
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Dll</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetBeginSessionW</strong> (Unicode) y <strong>JetBeginSessionA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetDupSession](./jetdupsession-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parámetros del sistema](./extensible-storage-engine-system-parameters.md)
