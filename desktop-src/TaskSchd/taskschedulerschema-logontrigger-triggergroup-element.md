---
title: Elemento LogonTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- desencadenador Logon, elemento XML
- Programador de tareas del elemento LogonTrigger
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359707"
---
# <a name="logontrigger-triggergroup-element"></a>Elemento LogonTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

El elemento **LogonTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                        | Tipo                                                                     | Descripción                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Retraso (logonTriggerType)**](taskschedulerschema-delay-logontriggertype-element.md)                         | duration                                                                 | Cantidad de tiempo entre el momento en el que el usuario inicia sesión y el momento en que se inicia la tarea.<br/>                                              |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica la fecha y hora de desactivación del desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.<br/>                                   |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**UserId (logonTriggerType)**](taskschedulerschema-userid-logontriggertype-element.md)                       | string                                                                   | Identificador del usuario. La tarea se inicia cuando este usuario inicia sesión en el equipo.<br/>                                      |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, se especifica un desencadenador Logon mediante el objeto [**LogonTrigger**](logontrigger.md) .

En el desarrollo de C++, se especifica un desencadenador Logon mediante la interfaz [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .

Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) y [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) . Estos elementos se deben agregar en la secuencia que se muestra a continuación.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**UserId (logonTriggerType)**](taskschedulerschema-userid-logontriggertype-element.md)
-   [**Retraso (logonTriggerType)**](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a>Atributos

El atributo que se muestra a continuación está definido por los tipos de elementos complejos de [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

-   ID: identificador del desencadenador.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que utiliza un desencadenador Logon, vea [ejemplo de desencadenador de inicio de sesión (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





