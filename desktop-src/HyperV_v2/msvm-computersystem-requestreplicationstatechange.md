---
description: Solicita que el estado de replicación de la máquina virtual se cambie al valor especificado y actúe en la relación de replicación principal de la máquina virtual.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Método RequestReplicationStateChange de la clase Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544734"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a>Método RequestReplicationStateChange de la \_ clase MSVM ComputerSystem

Solicita que el estado de replicación de la máquina virtual se cambie al valor especificado y actúe en la relación de replicación principal de la máquina virtual. Mientras el cambio de estado está en curso, la propiedad **ReplicationState** se cambia al valor del parámetro *RequestedState* . Este método solo se admite para las instancias de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representan una máquina virtual.

> [!Note]  
> A partir de Windows 8.1, se recomienda no usar **RequestReplicationStateChange** ya para solicitar el cambio de estado de replicación. En su lugar, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RequestedState* \[ de\]
</dt> <dd>

Nuevo estado de replicación. Debe ser uno de los valores siguientes.

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Listo para iniciar la replicación inicial** (1)


</dt> <dd>

Listo para iniciar la replicación inicial.

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Esperando para completar la replicación inicial** (2)


</dt> <dd>

Esperando para completar la replicación inicial.

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)


</dt> <dd>

Replicating.

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicación sincronizada completa** (4)


</dt> <dd>

Replicación sincronizada completada.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (7)


</dt> <dd>

Suspende la replicación.

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancelar resincronización** (9)


</dt> <dd>

Cancelar la resincronización.

</dd> </dl> </dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia opcional a un objeto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) que se devuelve si la operación se ejecuta de forma asincrónica. Si está presente, la referencia devuelta se puede usar para supervisar el progreso y obtener el resultado del método.

</dd> <dt>

*TimeoutPeriod* \[ de\]
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                                | Descripción                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl>                    | Correcto<br/>                                                                                                          |
| <dl> <dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt> </dl> | La transición es asincrónica.<br/>                                                                                  |
| <dl> <dt>**Error**</dt> <dt>32768</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**Acceso Denegado**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**No compatible**</dt> <dt>32770</dt> </dl>                          |                                                                                                                             |
| <dl> El <dt>**Estado es desconocido**</dt> <dt>32771</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Tiempo de espera**</dt> <dt>32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**Parámetro no válido**</dt> <dt>32773</dt> </dl>                      | No se admite el valor especificado en uno de los parámetros.<br/>                                                   |
| <dl> El <dt>**sistema está en uso**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**Estado no válido para esta operación**</dt> <dt>32775</dt> </dl>       | El valor especificado en el parámetro *RequestedState* no se admite en el estado o el modo de replicación actual.<br/> |
| <dl> <dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> El <dt>**sistema no está disponible**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**Memoria**</dt> insuficiente <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**No se encontró el archivo**</dt> <dt>32779</dt> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

 




