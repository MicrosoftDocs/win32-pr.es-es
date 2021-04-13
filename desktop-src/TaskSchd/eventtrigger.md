---
title: Objeto EventTrigger (Windows. UI. Xaml. h)
description: Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce un evento del sistema.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- desencadenador de evento Programador de tareas, objeto
- Objeto EventTrigger Programador de tareas
- Objeto EventTrigger Programador de tareas, descrito
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534990"
---
# <a name="eventtrigger-object"></a>EventTrigger (objeto)

Objeto de scripting que representa un desencadenador que inicia una tarea cuando se produce un evento del sistema.

## <a name="members"></a>Miembros

El objeto **EventTrigger** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **EventTrigger** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](eventtrigger-delay.md)<br/>                      | Lectura/escritura<br/> | Obtiene o establece un valor que indica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.<br/>                                                                                                                                                                                                                                                            |
| [**habilitado**](trigger-enabled.md)<br/>                       | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece un valor booleano que indica si el desencadenador está habilitado.<br/>                                                                                                                                                                                                                                             |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/>                                                                                                                                                                                              |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la cantidad máxima de tiempo que se permite la ejecución de la tarea iniciada por este desencadenador.<br/>                                                                                                                                                                                                                       |
| [**Sesión**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece el identificador del desencadenador.<br/>                                                                                                                                                                                                                                                                            |
| [**Repetición**](trigger-repetition.md)<br/>                 | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>                                                                                                                                                                                                       |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lectura/escritura<br/> | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene o establece la fecha y hora en que se activa el desencadenador.<br/>                                                                                                                                                                                                                                                           |
| [**Subscription**](eventtrigger-subscription.md)<br/>        | Lectura/escritura<br/> | Obtiene o establece la cadena de consulta XPath que identifica el evento que activa el desencadenador.<br/>                                                                                                                                                                                                                                                                                         |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Solo lectura<br/>  | Heredado del objeto [**desencadenador**](trigger.md) . Obtiene el tipo del desencadenador.<br/>                                                                                                                                                                                                                                                                                           |
| [**ValueQueries**](eventtrigger-valuequeries.md)<br/>        | Lectura/escritura<br/> | Obtiene o establece una colección de consultas XPath con nombre. Cada consulta de la colección se aplica al último XML de evento coincidente que se devuelve de la consulta de suscripción especificada en la propiedad de [**suscripción**](eventtrigger-subscription.md) . El nombre de la consulta se puede usar como una variable en el mensaje de una acción [**ShowMessageAction**](showmessageaction.md) .<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede crear un máximo de 500 tareas con suscripciones de eventos. Una suscripción de eventos que consulta diversos eventos se puede usar para desencadenar una tarea que utiliza la misma acción en respuesta a los eventos que se registran.

Al leer o escribir su propio XML para una tarea, se especifica un desencadenador de eventos mediante el elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) del esquema de programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y un ejemplo de código para este objeto de scripting, vea [ejemplo de desencadenador de eventos (scripting)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Windows. UI. Xaml. h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Activado**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

