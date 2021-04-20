---
title: Elemento Interval (repetitionType)
description: Especifica la cantidad de tiempo entre cada reinicio de la tarea.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Intervalo de elementos Programador de tareas
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734200"
---
# <a name="interval-repetitiontype-element"></a>Elemento Interval (repetitionType)

Especifica la cantidad de tiempo entre cada reinicio de la tarea. El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, "PT5M" es 5 minutos, "PT1H" es 1 hora y "PT20M" es 20 minutos). El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es de 1 minuto.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el [**tipo complejo repetitionType.**](taskschedulerschema-repetitiontype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                      | Derivado de                                                             | Description                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Repetición**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, el intervalo del patrón de repetición se especifica mediante la [**propiedad RepetitionPattern.Interval.**](repetitionpattern-interval.md)

Para el desarrollo de C++, el intervalo del patrón de repetición se especifica mediante la [**propiedad IRepetitionPattern::Interval.**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML para una tarea que usa un intervalo de repetición, vea [Ejemplo de desencadenador diario (XML).](daily-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





