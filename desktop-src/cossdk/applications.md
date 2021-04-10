---
description: Contiene un objeto para cada aplicación COM+ instalada en el equipo local. Las propiedades expuestas por estos objetos contienen todas las configuraciones realizadas en el nivel de la aplicación.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Colección de aplicaciones
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153273"
---
# <a name="applications-collection"></a>Colección de aplicaciones

Contiene un objeto para cada aplicación COM+ instalada en el equipo local. Las propiedades expuestas por estos objetos contienen todas las configuraciones realizadas en el nivel de la aplicación.

Las propiedades de los componentes de una aplicación se establecen mediante la colección de [**componentes**](components.md) relacionados. Los roles se asignan a una aplicación mediante la colección de [**roles**](roles.md) relacionados.

Para instalar los componentes en una aplicación, use los métodos del objeto [**COMAdminCatalog**](comadmincatalog.md) . Para instalar una aplicación desde un archivo o para apagar o exportar una aplicación, use también métodos en el objeto **COMAdminCatalog** . De lo contrario, para crear una nueva aplicación, puede Agregar un objeto a la colección de **aplicaciones** .

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección de **aplicaciones** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ApplicationInstances**](applicationinstances.md)
-   [**Componentes**](components.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**LegacyComponents**](legacycomponents.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Roles**](roles.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Particiones**](partitions.md)
-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [3GigSupportEnabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [Activación](#recycleactivationlimit)
-   [ApplicationAccessChecksEnabled](#applicationaccesschecksenabled)
-   [ApplicationDirectory](#applicationdirectory)
-   [ApplicationProxy](#applicationproxyservername)
-   [ApplicationProxyServerName](#applicationproxyservername)
-   [AppPartitionID](#apppartitionid)
-   [Autenticación](#authenticationcapability)
-   [AuthenticationCapability](#authenticationcapability)
-   [Sustituir](#changeable)
-   [CommandLine](#commandline)
-   [ConcurrentApps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [CRMEnabled](#crmenabled)
-   [CRMLogFile](#crmlogfile)
-   [Eliminable](#deleteable)
-   [Descripción](#description)
-   [DumpEnabled](#dumpenabled)
-   [DumpOnException](#dumponexception)
-   [DumpOnFailfast](#dumponfailfast)
-   [DumpPath](#dumppath)
-   [EventsEnabled](#eventsenabled)
-   [Id](#applications-collection)
-   [Identidad](#identity)
-   [ImpersonationLevel](#impersonationlevel)
-   [IsEnabled](#isenabled)
-   [IsSystem](#issystem)
-   [MaxDumpCount](#maxdumpcount)
-   [Nombre](#applicationproxyservername)
-   [Contraseña](#password)
-   [QCAuthenticateMsgs](#qcauthenticatemsgs)
-   [QCListenerMaxThreads](#qclistenermaxthreads)
-   [QueueListenerEnabled](#queuelistenerenabled)
-   [QueuingEnabled](#queuingenabled)
-   [RecycleActivationLimit](#recycleactivationlimit)
-   [RecycleCallLimit](#recyclecalllimit)
-   [RecycleExpirationTimeout](#recycleexpirationtimeout)
-   [RecycleLifetimeLimit](#recyclelifetimelimit)
-   [RecycleMemoryLimit](#recyclememorylimit)
-   [Replicable](#replicable)
-   [RunForever](#runforever)
-   [ServiceName](#servicename)
-   [ShutdownAfter](#shutdownafter)
-   [SoapActivated](#soapactivated)
-   [SoapBaseUrl](#soapbaseurl)
-   [SoapMailTo](#soapmailto)
-   [SoapVRoot](#soapvroot)
-   [SRPEnabled](#srpenabled)
-   [SRPTrustLevel](#srptrustlevel)

### <a name="3gigsupportenabled"></a>3GigSupportEnabled



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si la aplicación puede utilizar 3 GB de memoria en su proceso. Si no está habilitado, la aplicación solo puede utilizar 2 GB de memoria. |
| Access         | ReadWrite                                                                                                                                     |
| Tipo           | Bool                                                                                                                                          |
| Valor predeterminado        | False                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si las comprobaciones de acceso se realizan solo en el nivel de proceso o en el nivel de componente y de proceso. Se recomienda usar las constantes en la enumeración y no los valores numéricos. |
| Access         | ReadWrite                                                                                                                                                                                                       |
| Tipo           | Valores posibles largos: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                |
| Valor predeterminado        | COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>Activación



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | La activación local indica que los objetos de la aplicación se ejecutan en un proceso de servidor local dedicado (aplicación de servidor). La activación en proceso indica que los objetos se ejecutan en el proceso de su creador (aplicación de biblioteca). |
| Access         | ReadWrite                                                                                                                                                                                                                           |
| Tipo           | Valores posibles largos: COMAdminActivationInproc (0) COMAdminActivationLocal (1)                                                                                                                                                        |
| Valor predeterminado        | COMAdminActivationLocal (1)                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>ApplicationAccessChecksEnabled



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------|
| Descripción    | Indica si se realizan comprobaciones de acceso para la aplicación cuando los clientes realizan llamadas a ella. |
| Access         | ReadWrite                                                                                          |
| Tipo           | Bool                                                                                               |
| Valor predeterminado        | True                                                                                               |
| Sistema mínimo | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>ApplicationDirectory



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Ruta de acceso completa a la aplicación. Esta información es necesaria cuando se configuran los ensamblados en paralelo (SxS). Los ensamblados en paralelo (SxS) permiten a las aplicaciones ASP especificar qué versión de una DLL del sistema compatible con SxS se va a usar, como MSVCRT, MSXML, COMCTL, GDIPLUS, etc. Por ejemplo, si la aplicación ASP se basa en la versión 2,0 de MSVCRT, puede asegurarse de que la aplicación siga usando la versión 2,0 de MSVCRT incluso después de aplicar los Service Packs al servidor. Cualquier versión nueva de MSVCRT todavía está instalada en el equipo, pero la versión 2,0 permanece y se usa en la aplicación. Los archivos DLL compatibles con SxS se almacenan en% WINDIR% \\ WinSxS. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Predeterminado        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Solo se puede usar una versión de un archivo DLL del sistema en cualquier grupo de aplicaciones, aunque esta característica se pueda configurar en el nivel de la aplicación. Por ejemplo, si la aplicación app1 usa MSVCRT, la versión 2,5 y la aplicación App2 usa MSVCRT, versión 2,4, app1 y App2 no deben estar en el mismo grupo de aplicaciones. Si es así, la aplicación que se carga primero tiene la versión de MSVCRT cargada y la otra aplicación se ve obligada a usarla hasta que se descarguen las aplicaciones.

 

Para obtener más información, vea la sección sobre los ensamblados en paralelo en [cambios en los servicios com+ en IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).

### <a name="applicationproxy"></a>ApplicationProxy



| Entrada | Value |
|----------------|------------------------------------------------------------|
| Descripción    | Indica si la aplicación es un proxy de aplicación. |
| Access         | ReadOnly                                                   |
| Tipo           | Bool                                                       |
| Valor predeterminado        | False                                                      |
| Sistema mínimo | Windows 2000                                               |



 

### <a name="applicationproxyservername"></a>ApplicationProxyServerName



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Un nombre de servidor remoto que se usa al exportar el proxy de aplicación. Es este nombre de servidor al que apunta el proxy de aplicación cuando se instala en un equipo cliente. |
| Access         | ReadWrite                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                 |
| Predeterminado        | ""                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>AppPartitionID



| Entrada | Value |
|----------------|---------------------------------------------------|
| Descripción    | Un GUID que representa el identificador de la partición de aplicación. |
| Access         | ReadOnly                                          |
| Tipo           | String                                            |
| Predeterminado        | <Generated>                                 |
| Sistema mínimo | Windows Server 2003                               |



 

### <a name="authentication"></a>Autenticación



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece el nivel de autenticación de las llamadas, con los valores correspondientes a la configuración de autenticación de llamada a procedimiento remoto (RPC). Cuando se elige COMAdminAuthenticationDefault, se usa el valor de la propiedad DefaultAuthenticationLevel de la colección [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Tipo           | Valores posibles largos: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                              |
| Valor predeterminado        | COMAdminAuthenticationPacket (4)                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> En el caso de las aplicaciones de biblioteca (en proceso), los únicos valores válidos aquí son COMAdminAuthenticationDefault y COMAdminAuthenticationNone. Se recomienda usar las constantes en la enumeración y no los valores numéricos.

 

### <a name="authenticationcapability"></a>AuthenticationCapability



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina qué identidad se presenta cuando se suplantan las llamadas.                                                                                                                                                                      |
| Access         | ReadWrite                                                                                                                                                                                                                               |
| Tipo           | Valores posibles largos: COMAdminAuthenticationCapabilitiesNone (0X0) COMAdminAuthenticationCapabilitiesSecureReference (0X2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) |
| Valor predeterminado        | COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>Sustituir



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si los cambios en la configuración de la aplicación o en sus componentes están permitidos, ya sea mediante programación o a través de la herramienta de administración de servicios de componentes. |
| Access         | ReadWrite                                                                                                                                                                     |
| Tipo           | Bool                                                                                                                                                                          |
| Valor predeterminado        | True                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena de línea de comandos que se va a usar en la depuración. La aplicación puede iniciarse en un depurador con la línea de comandos especificada. |
| Access         | ReadWrite                                                                                                                  |
| Tipo           | String                                                                                                                     |
| Predeterminado        | ""                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>ConcurrentApps



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------|
| Descripción    | Especifica el número máximo de aplicaciones agrupables que pueden ejecutarse simultáneamente. |
| Access         | ReadWrite                                                                        |
| Tipo           | Long (1-1048576)                                                                 |
| Valor predeterminado        | 1                                                                                |
| Sistema mínimo | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| Entrada | Value |
|----------------|---------------------------------------------------------------|
| Descripción    | Cadena informativa para describir quién creó la aplicación. |
| Access         | ReadWrite                                                     |
| Tipo           | String                                                        |
| Predeterminado        | ""                                                            |
| Sistema mínimo | Windows 2000                                                  |



 

### <a name="crmenabled"></a>CRMEnabled



| Entrada | Value |
|----------------|------------------------------------------------------------------|
| Descripción    | Determina si está habilitado el Administrador de recursos de compensación. |
| Access         | ReadWrite                                                        |
| Tipo           | Bool                                                             |
| Valor predeterminado        | False                                                            |
| Sistema mínimo | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>CRMLogFile



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------|
| Descripción    | Nombre y ruta de acceso del archivo para mantener el registro para el administrador de compensación de recursos (CRM). |
| Access         | ReadWrite                                                                              |
| Tipo           | String                                                                                 |
| Predeterminado        | ""                                                                                     |
| Sistema mínimo | Windows 2000                                                                           |



 

### <a name="deleteable"></a>Eliminable



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece si se puede eliminar la aplicación, ya sea mediante programación o a través de la herramienta de administración de servicios de componentes. |
| Access         | ReadWrite                                                                                                                   |
| Tipo           | Bool                                                                                                                        |
| Valor predeterminado        | True                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|----------------------------|
| Descripción    | Describe la aplicación. |
| Access         | ReadWrite                  |
| Tipo           | String                     |
| Predeterminado        | ""                         |
| Sistema mínimo | Windows 2000               |



 

### <a name="dumpenabled"></a>DumpEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------|
| Descripción    | Habilita el volcado del estado de una aplicación COM+ en el momento en que se produjo un error en un directorio designado. |
| Access         | ReadWrite                                                                                             |
| Tipo           | Bool                                                                                                  |
| Valor predeterminado        | False                                                                                                 |
| Sistema mínimo | Windows XP                                                                                            |



 

> [!Note]  
> A partir de Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los archivos de volcado de memoria de COM+.

 

### <a name="dumponexception"></a>DumpOnException



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Habilita el volcado del estado de una aplicación COM+ cuando la aplicación produce una excepción no controlada y finaliza con el tiempo de ejecución de COM+. |
| Access         | ReadWrite                                                                                                                                     |
| Tipo           | Bool                                                                                                                                          |
| Valor predeterminado        | False                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                    |



 

### <a name="dumponfailfast"></a>DumpOnFailfast



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------|
| Descripción    | Habilita el volcado del estado de una aplicación COM+ cuando se produce un error en la aplicación. |
| Access         | ReadWrite                                                                       |
| Tipo           | Bool                                                                            |
| Valor predeterminado        | False                                                                           |
| Sistema mínimo | Windows XP                                                                      |



 

### <a name="dumppath"></a>DumpPath



| Entrada | Value |
|----------------|--------------------------------------------------------------|
| Descripción    | La ruta de acceso del directorio en el que se guardan los archivos de volcado. |
| Access         | ReadWrite                                                    |
| Tipo           | String                                                       |
| Predeterminado        | "% SystemRoot% \\ system32 \\ com \\ DMP"                           |
| Sistema mínimo | Windows XP                                                   |



 

> [!Note]  
> A partir de Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los archivos de volcado de memoria de COM+.

 

### <a name="eventsenabled"></a>EventsEnabled



| Entrada | Value |
|----------------|-----------------------------------------------------------|
| Descripción    | Indica si los eventos están habilitados para la aplicación. |
| Access         | ReadWrite                                                 |
| Tipo           | Bool                                                      |
| Valor predeterminado        | True                                                      |
| Sistema mínimo | Windows 2000                                              |



 

### <a name="id"></a>id



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Un GUID que representa la aplicación. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                            |
| Tipo           | String                                                                                                                                                               |
| Predeterminado        | <Generated>                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>Identidad



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece la identidad de proceso de servidor para la aplicación. Especifique una cuenta de usuario válida o un "usuario interactivo" para que la aplicación asuma la identidad del usuario que ha iniciado la sesión actual. También puede especificar las cadenas ' NT Authority \\ LocalService ', ' NT Authority \\ NetworkService ' y ' NT Authority \\ System '. La contraseña predeterminada para estas tres cuentas es "" (cadena vacía). |
| Access         |                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipo           |                                                                                                                                                                                                                                                                                                                                                                                    |
| Valor predeterminado        |                                                                                                                                                                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

La propiedad de identidad no está habilitada para las aplicaciones de biblioteca, que se ejecutan en el proceso del cliente.

La propiedad de contraseña debe establecerse al mismo tiempo que la identidad, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque la contraseña y la identidad se validan antes de guardarse. Si la contraseña y la identidad no se sincronizan, la aplicación no se puede iniciar hasta que un administrador la restablezca.

### <a name="impersonationlevel"></a>ImpersonationLevel



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece el nivel de suplantación usado para las llamadas realizadas a otras aplicaciones.                                                                                           |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Valores posibles largos: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4) |
| Valor predeterminado        | COMAdminImpersonationImpersonate (3)                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Si el componente o la aplicación COM+ está deshabilitado, IsEnabled es false. Si el componente o la aplicación COM+ está habilitado, IsEnabled es true. |
| Access         | ReadWrite                                                                                                                                 |
| Tipo           | Bool                                                                                                                                      |
| Valor predeterminado        | True                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                |



 

### <a name="issystem"></a>IsSystem



| Entrada | Value |
|----------------|--------------------------------------|
| Descripción    | Identifica las aplicaciones del sistema COM+. |
| Access         | ReadOnly                             |
| Tipo           | Bool                                 |
| Valor predeterminado        | False                                |
| Sistema mínimo | Windows 2000                         |



 

### <a name="maxdumpcount"></a>MaxDumpCount



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de archivos que se van a generar antes de que se produzca la sobrescritura. |
| Access         | ReadWrite                                                                        |
| Tipo           | Long (1-200)                                                                     |
| Predeterminado        | 5                                                                                |
| Sistema mínimo | Windows XP                                                                       |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la aplicación. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadWrite                                                                                                                                                                                                                            |
| Tipo           | String                                                                                                                                                                                                                               |
| Predeterminado        | "Nueva aplicación"                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> Deben elegirse nombres únicos para las aplicaciones. Si se crean varias aplicaciones con el mismo nombre, puede interferir con la referencia de las aplicaciones por nombre, lo que resulta en un comportamiento impredecible.

 

### <a name="password"></a>Contraseña



| Entrada | Value |
|----------------|----------------------------------------------------------------------------|
| Descripción    | Establece la contraseña utilizada por el proceso de servidor para iniciar sesión con la identidad. |
| Access         | WriteOnly                                                                  |
| Tipo           | String                                                                     |
| Predeterminado        | ""                                                                         |
| Sistema mínimo | Windows 2000                                                               |



 

La contraseña debe establecerse al mismo tiempo que la identidad, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque la contraseña y la identidad se validan antes de guardarse. Si la contraseña y la identidad no se sincronizan, la aplicación no se puede iniciar hasta que un administrador la restablezca.

### <a name="qcauthenticatemsgs"></a>QCAuthenticateMsgs



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica en qué circunstancias se autentican las solicitudes en cola a una aplicación.                                                 |
| Access         | ReadWrite                                                                                                                               |
| Tipo           | Valores posibles largos: COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2) |
| Valor predeterminado        | COMAdminQCMessageAuthenticateSecureApps (0)                                                                                             |
| Sistema mínimo | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QCListenerMaxThreads



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de subprocesos de agente de escucha simultáneos. El intervalo válido para esta propiedad es de 0 a 1000. En el caso de una aplicación recién creada, el valor se deriva del algoritmo que se usa actualmente para determinar el número predeterminado de subprocesos del agente de escucha: 16 veces el número de CPU del servidor. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                 |
| Tipo           | Long (0-1000)                                                                                                                                                                                                                                                                                             |
| Valor predeterminado        | 0                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Esta propiedad también está disponible con la capacidad de lectura y escritura de la pestaña **puesta en cola** de la herramienta administrativa Servicios de componentes.

 

### <a name="queuelistenerenabled"></a>QueueListenerEnabled



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si el agente de escucha de componentes en cola está habilitado para la aplicación. Si está habilitada, el agente de escucha se inicia cuando se inicia la aplicación. Esta propiedad solo surte efecto si QueuingEnabled está establecido en true. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                 |
| Valor predeterminado        | False                                                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------|
| Descripción    | Indica si el servicio de componentes en cola COM+ está habilitado para la aplicación. |
| Access         | ReadWrite                                                                            |
| Tipo           | Bool                                                                                 |
| Valor predeterminado        | False                                                                                |
| Sistema mínimo | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>RecycleActivationLimit



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de activaciones de los objetos configurados en la aplicación que se aceptan antes de reciclar el proceso. El número predeterminado de activaciones es 0. |
| Access         | ReadWrite                                                                                                                                                            |
| Tipo           | Long (0-1048576)                                                                                                                                                     |
| Valor predeterminado        | 0                                                                                                                                                                    |
| Sistema mínimo | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de llamadas para permitir que los objetos configurados en la aplicación acepten antes de reciclar el proceso. El número predeterminado de llamadas es 0. |
| Access         | ReadWrite                                                                                                                                                      |
| Tipo           | Long (0-1048576)                                                                                                                                               |
| Valor predeterminado        | 0                                                                                                                                                              |
| Sistema mínimo | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>RecycleExpirationTimeout



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica la cantidad de tiempo (en minutos) que se permite la ejecución de un proceso reciclado antes de cerrarlo. La cuenta atrás comienza inmediatamente después de que se recicle el proceso. El tiempo de espera de expiración máximo es de 1440 minutos (24 horas) y el valor predeterminado es 15 minutos. |
| Access         | ReadWrite                                                                                                                                                                                                                                                        |
| Tipo           | Long (1-1440)                                                                                                                                                                                                                                                    |
| Valor predeterminado        | 15                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>RecycleLifetimeLimit



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de minutos que se permite que un proceso se ejecute antes de reciclarlo. El límite de duración máximo es de 30240 minutos (21 días) y el valor predeterminado es 0 minutos. |
| Access         | ReadWrite                                                                                                                                                                   |
| Tipo           | Long (0-30240)                                                                                                                                                              |
| Valor predeterminado        | 0                                                                                                                                                                           |
| Sistema mínimo | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>RecycleMemoryLimit



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica la cantidad máxima de uso de memoria (en kilobytes) permitida para un proceso antes de que se recicle. Si el uso de memoria del proceso supera el número especificado durante un período superior a un minuto, el proceso se recicla. La cantidad predeterminada de uso de memoria es de 0 KB. |
| Access         | ReadWrite                                                                                                                                                                                                                                                              |
| Tipo           | Long (0-1048576)                                                                                                                                                                                                                                                       |
| Valor predeterminado        | 0                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a>Replicable



| Entrada | Value |
|----------------|------------------------------------------------------|
| Descripción    | Indica si la aplicación se puede replicar. |
| Access         | ReadWrite                                            |
| Tipo           | Bool                                                 |
| Valor predeterminado        | True                                                 |
| Sistema mínimo | Windows XP                                           |



 

### <a name="runforever"></a>RunForever



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Permite que un proceso de servidor continúe si una aplicación está inactiva. Si se establece en true, el proceso de servidor no se apaga cuando se deja inactivo. Si se establece en false, el proceso se cierra según el valor establecido por la propiedad ShutdownAfter. RunForever no está habilitado para las aplicaciones de biblioteca (en proceso). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                     |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>ServiceName



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El nombre de servicio correspondiente a la aplicación configurada para ejecutarse como una aplicación de servicio. Si este valor es **null**, la aplicación no está configurada para ejecutarse como un servicio. De lo contrario, la información de configuración para el servicio se puede encontrar mediante el nombre del servicio. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                         |
| Tipo           | String                                                                                                                                                                                                                                                                           |
| Predeterminado        | ""                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>ShutdownAfter



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece el retraso antes de cerrar un proceso de servidor después de que se vuelva inactivo. La latencia de cierre oscila entre 0 y 1440 minutos (24 horas). Si RunForever se establece en true, esta propiedad se omite. ShutdownAfter no está habilitado para las aplicaciones de biblioteca (en proceso). |
| Access         | ReadWrite                                                                                                                                                                                                                                                          |
| Tipo           | Long (0-1440)                                                                                                                                                                                                                                                      |
| Valor predeterminado        | 3                                                                                                                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>SoapActivated



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------|
| Descripción    | Indica si esta aplicación se expone para su consumo a través del protocolo SOAP. |
| Access         | ReadWrite                                                                            |
| Tipo           | Bool                                                                                 |
| Valor predeterminado        | False                                                                                |
| Sistema mínimo | Windows Server 2003                                                                  |



 

### <a name="soapbaseurl"></a>SoapBaseUrl



| Entrada | Value |
|----------------|------------------------------------------------------------------------------|
| Descripción    | Punto de conexión de la dirección URL en el que esta aplicación se expone a través del protocolo SOAP. |
| Access         | ReadWrite                                                                    |
| Tipo           | String                                                                       |
| Predeterminado        | ""                                                                           |
| Sistema mínimo | Windows Server 2003                                                          |



 

### <a name="soapmailto"></a>SoapMailTo



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------|
| Descripción    | La dirección de correo electrónico en la que se expone esta aplicación a través del protocolo SOAP. |
| Access         | ReadWrite                                                                     |
| Tipo           | String                                                                        |
| Predeterminado        | ""                                                                            |
| Sistema mínimo | Windows Server 2003                                                           |



 

### <a name="soapvroot"></a>SoapVRoot



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Descripción    | El directorio raíz virtual de IIS en el que residen los scripts de acceso que exponen la aplicación a través del protocolo SOAP. |
| Access         | ReadWrite                                                                                                            |
| Tipo           | String                                                                                                               |
| Predeterminado        | ""                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>SRPEnabled



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina la Directiva de restricción de software (SRP) de la aplicación. Si se establece en true, se utiliza la propiedad SRPTrustLevel de la aplicación. Si se establece en false, se usan las directivas de restricción de software de la configuración de seguridad local. La configuración de seguridad local se controla mediante el complemento Directiva de seguridad local de Microsoft Management Console. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el nivel de confianza de la Directiva de restricción de software (SRP) de la aplicación. Esta propiedad solo se usa si la propiedad SRPEnabled está establecida en true. El nivel de confianza de SRP hace referencia al nivel de confianza que desea dar a una aplicación. Un nivel de confianza SRP sin restricciones se corresponde con \_ el \_ valor de enumeración LEVELID FULLYTRUSTED más seguro, mientras que un nivel de confianza SRP no permitido corresponde al \_ valor de enumeración de LEVELID no \_ permitido. La enumeración para los niveles de confianza se define en Winsafer. h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipo           | Valores posibles largos: LEVELID de seguridad no \_ \_ permitido (0X0) Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Valor predeterminado        | Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Una aplicación en la que esté dispuesto a confiar con acceso sin restricciones debe tener la seguridad más estricta asociada. Las aplicaciones que no están restringidas pueden cargar solo componentes no restringidos, mientras que las aplicaciones no permitidas no podrán ejecutarse y, por lo tanto, no podrán cargar ningún componente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
