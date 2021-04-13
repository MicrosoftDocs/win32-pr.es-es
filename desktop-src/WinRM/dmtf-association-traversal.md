---
title: Detección de perfiles DMTF a través de cruce seguro de asociaciones
description: Un componente clave de la infraestructura de Instrumental de administración de Windows (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421519"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Detección de perfiles DMTF a través de cruce seguro de asociaciones

Un componente clave de la infraestructura de Instrumental de administración de Windows (WMI) es un modelo orientado a objetos de las entidades administrables de un sistema. El modelo se ajusta a un estándar mantenido por el equipo de tareas de administración de escritorio ([DMTF](https://www.dmtf.org/standards/wsman)) y se conoce como modelo de información común (CIM). Algunas clases del modelo, como archivo de [ \_ archivos CIM](../cimwin32prov/cim-datafile.md) o [ \_ proceso de Win32](../cimwin32prov/win32-process.md), se corresponden directamente con entidades administrables. Otras clases del modelo, como SystemServices de [Win32 \_ ](../cimwin32prov/win32-systemservices.md), representan las relaciones entre las entidades administrables. Estas clases de modelado de relaciones se conocen como clases de asociación.

Mediante el lenguaje de consulta específico de WMI, WQL, puede recuperar instancias de clases que representan entidades administrables o instancias de clases de asociación. Pero WQL es específico de la implementación. Solo funciona con la implementación de Windows del estándar DMTF (WMI). Además, la sintaxis de WQL para recuperar clases de asociación es bastante complicada.

La infraestructura de Administración remota de Windows (WinRM) proporciona una manera excelente de aprovechar la funcionalidad de WMI. Las primeras versiones de WinRM tenían que usar WQL para recuperar instancias de clases de asociación. WinRM 2,0 incluye una nueva característica conocida como detección de perfiles de DMTF a través de cruce seguro de asociaciones. El cruce seguro de asociaciones permite que un usuario de WinRM recupere instancias de clases de asociación mediante un mecanismo de filtrado estándar, el dialecto AssociationFilter, definido en la especificación de enlace CIM de DMTF. Para obtener más información sobre el recorrido de asociación, vea el WS-Management especificación de enlace de CIM ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

La utilidad WinRM proporciona un mecanismo sencillo para atravesar la Asociación adecuada y recuperar un perfil de dispositivo.

## <a name="configuration-implementation-details"></a>Detalles de la implementación de configuración

La utilidad WinRM admite ahora un dialecto para la solicitud de asociación. Se puede especificar el URI o el alias mediante la utilidad WinRM.



| Alias       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| correlación | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Recuperar instancias de una clase de asociación mediante el dialecto AssociationFilter

La utilidad WinRM puede recuperar instancias de clase de asociación WMI de una instancia de origen determinada. El siguiente comando muestra cómo usar la utilidad WinRM para recuperar instancias de clases de Asociación de [ \_ servicio Win32](../cimwin32prov/win32-service.md) . El modificador "-Associations" se debe usar para devolver clases de asociación.

**WinRM Enumerate wmicimv2/ \* -Dialect: Association-Associations-Filter: {Object = \_ servicio Win32? Name = WinRM; resultclassname = Win32 \_ dependentservice; role = dependent}**

El siguiente fragmento de código basado en texto es la salida del comando anterior:

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Recuperar instancias de una clase asociada mediante el dialecto AssociationFilter

La utilidad WinRM puede recuperar instancias de clase WMI asociadas a una instancia de origen determinada. El siguiente comando muestra cómo usar la utilidad WinRM para recuperar instancias de las clases asociadas del [ \_ servicio Win32](../cimwin32prov/win32-service.md) .

**WinRM Enumerate wmicimv2/ \* -Dialect: Association-Filter: {Object = \_ servicio Win32? Name = WinRM; associationclassname = Win32 \_ dependentservice; resultclassname = Win32 \_ Service; resultrole = antecedente; role = dependent}**

El siguiente fragmento de código basado en texto es la salida del comando anterior:

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 