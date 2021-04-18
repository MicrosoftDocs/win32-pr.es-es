---
title: Interfaz IVMVirtualMachine (VPCCOMInterfaces. h)
description: Define la interfaz para una máquina virtual.
ms.assetid: c1c243f2-0fb7-4249-8dc9-f0b70059e78f
keywords:
- Interfaz IVMVirtualMachine Virtual PC
- Interfaz IVMVirtualMachine Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006fe414a662c3d6d556aba68712aa0b428d9b5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695856"
---
# <a name="ivmvirtualmachine-interface"></a>Interfaz IVMVirtualMachine

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define la interfaz para una máquina virtual. **IVMVirtualMachine** puede notificar a los clientes sobre eventos mediante la interfaz de salida de [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md) . Los objetos **IVMVirtualMachine** se devuelven desde métodos [**IVMVirtualPC**](ivmvirtualpc.md) como [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md), [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)y [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md). También puede recuperar un objeto **IVMVirtualMachine** del objeto [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md) devuelto desde la propiedad [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Miembros

La interfaz **IVMVirtualMachine** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachine** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMVirtualMachine** tiene estos métodos.



| Método                                                                           | Descripción                                                                                                |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md)                       | Agrega una nueva unidad de CD o DVD a la máquina virtual.<br/>                                              |
| [**AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)         | Agrega una nueva conexión de disco duro a la máquina virtual.<br/>                                         |
| [**AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md)                 | Agrega una interfaz de red a la máquina virtual.<br/>                                                |
| [**AttachUSBDevice**](ivmvirtualmachine-attachusbdevice.md)                     | Conecta un dispositivo USB a una máquina virtual.<br/>                                                     |
| [**DetachUSBDevice**](ivmvirtualmachine-detachusbdevice.md)                     | Libera un dispositivo USB de una máquina virtual.<br/>                                                   |
| [**DiscardSavedState**](ivmvirtualmachine-discardsavedstate.md)                 | Descarta cualquier información de estado guardada para una máquina virtual guardada.<br/>                               |
| [**DiscardUndoDisks**](ivmvirtualmachine-discardundodisks.md)                   | Descarta los discos para deshacer.<br/>                                                                |
| [**GetActivationValue**](ivmvirtualmachine-getactivationvalue.md)               | Recupera el valor de la configuración de activación especificada para esta máquina virtual.<br/>               |
| [**GetConfigurationValue**](ivmvirtualmachine-getconfigurationvalue.md)         | Recupera el valor de la configuración especificada para esta máquina virtual.<br/>            |
| [**MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)                       | Combina los discos para deshacer virtuales.<br/>                                                                  |
| [**Pausar**](ivmvirtualmachine-pause.md)                                         | Pausa la máquina virtual.<br/>                                                                     |
| [**RemoveActivationValue**](ivmvirtualmachine-removeactivationvalue.md)         | Quita el valor de la configuración de activación especificada para esta máquina virtual.<br/>                 |
| [**RemoveConfigurationValue**](ivmvirtualmachine-removeconfigurationvalue.md)   | Quita el valor de la configuración especificada para esta máquina virtual.<br/>              |
| [**RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md)                 | Quita la unidad de CD o DVD especificada de la máquina virtual.<br/>                                 |
| [**RemoveHardDiskConnection**](ivmvirtualmachine-removeharddiskconnection.md)   | Quita la conexión de disco duro especificada de la máquina virtual.<br/>                            |
| [**RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)           | Quita una interfaz de red de la máquina virtual.<br/>                                           |
| [**Reset**](ivmvirtualmachine-reset.md)                                         | Restablece la máquina virtual.<br/>                                                                     |
| [**Reanudar**](ivmvirtualmachine-resume.md)                                       | Reanuda la máquina virtual.<br/>                                                                    |
| [**Guardar**](ivmvirtualmachine-save.md)                                           | Guarda el estado de la máquina virtual.<br/>                                                                |
| [**SetActivationValue**](ivmvirtualmachine-setactivationvalue.md)               | Establece el valor de la configuración de activación especificada para esta máquina virtual.<br/>                    |
| [**SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)         | Establece el valor de la configuración especificada para esta máquina virtual.<br/>                 |
| [**StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md) | Configura un canal de comunicación entre el host y el invitado.<br/>                                         |
| [**Inicio**](ivmvirtualmachine-startup.md)                                     | Inicia la máquina virtual desde el estado no inicializado o guardado.<br/>                        |
| [**Startup2**](ivmvirtualmachine-startup2.md)                                   | Inicia la máquina virtual desde el estado no inicializado o guardado, con opciones avanzadas.<br/> |
| [**TurnOff**](ivmvirtualmachine-turnoff.md)                                     | Desactiva la máquina virtual.<br/>                                                                  |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMVirtualMachine** tiene estas propiedades.



| Propiedad                                                                            | Tipo de acceso           | Descripción                                                                                                                                    |
|:------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Contable**](ivmvirtualmachine-accountant.md)<br/>                       | Solo lectura<br/>  | Un contable para esta máquina virtual.<br/>                                                                                             |
| [**AttachedDriveTypes**](ivmvirtualmachine-attacheddrivetypes.md)<br/>       | Solo lectura<br/>  | Una matriz que indica el tipo de unidad conectado a cada ubicación de la máquina virtual.<br/>                                             |
| [**BaseBoardSerialNumber**](ivmvirtualmachine-baseboardserialnumber.md)<br/> | Lectura/escritura<br/> | Número de serie de la placa base.<br/>                                                                                                       |
| [**BIOSGUID**](ivmvirtualmachine-biosguid.md)<br/>                           | Lectura/escritura<br/> | GUID del BIOS.<br/>                                                                                                                      |
| [**BIOSSerialNumber**](ivmvirtualmachine-biosserialnumber.md)<br/>           | Lectura/escritura<br/> | Número de serie del BIOS.<br/>                                                                                                             |
| [**ChassisAssetTag**](ivmvirtualmachine-chassisassettag.md)<br/>             | Lectura/escritura<br/> | La etiqueta del activo del chasis.<br/>                                                                                                              |
| [**ChassisSerialNumber**](ivmvirtualmachine-chassisserialnumber.md)<br/>     | Lectura/escritura<br/> | Número de serie del chasis.<br/>                                                                                                          |
| [**ConfigID**](ivmvirtualmachine-configid.md)<br/>                           | Solo lectura<br/>  | Identificador único de la máquina virtual.<br/>                                                                                      |
| [**Muestra**](ivmvirtualmachine-display.md)<br/>                             | Solo lectura<br/>  | La pantalla de vídeo de la máquina virtual.<br/>                                                                                          |
| [**DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md)<br/>                   | Solo lectura<br/>  | Colección enumerable de unidades de CD y DVD conectadas a la máquina virtual.<br/>                                                      |
| [**Archivo**](ivmvirtualmachine-file.md)<br/>                                   | Solo lectura<br/>  | Ruta de acceso completa del archivo. VMC para la configuración de la máquina virtual.<br/>                                                    |
| [**FloppyDrives**](ivmvirtualmachine-floppydrives.md)<br/>                   | Solo lectura<br/>  | Colección enumerable de unidades de disquete conectadas a la máquina virtual.<br/>                                                          |
| [**Invitados**](ivmvirtualmachine-guestos.md)<br/>                             | Solo lectura<br/>  | El sistema operativo invitado de esta máquina virtual.<br/>                                                                                |
| [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)<br/>     | Solo lectura<br/>  | Colección enumerable de conexiones del disco duro.<br/>                                                                                  |
| [**Has3DNow**](ivmvirtualmachine-has3dnow.md)<br/>                           | Solo lectura<br/>  | Indica si el procesador admite el conjunto de instrucciones 3DNow.<br/>                                                                 |
| [**HasMMX**](ivmvirtualmachine-hasmmx.md)<br/>                               | Solo lectura<br/>  | Indica si el procesador admite el conjunto de instrucciones MMX.<br/>                                                                   |
| [**HasSSE**](ivmvirtualmachine-hassse.md)<br/>                               | Solo lectura<br/>  | Indica si el procesador admite el conjunto de instrucciones SSE.<br/>                                                                   |
| [**HasSSE2**](ivmvirtualmachine-hassse2.md)<br/>                             | Solo lectura<br/>  | Indica si el procesador admite el conjunto de instrucciones SSE2.<br/>                                                                  |
| [**Teclado**](ivmvirtualmachine-keyboard.md)<br/>                           | Solo lectura<br/>  | El dispositivo de teclado para la máquina virtual.<br/>                                                                                        |
| [**Memory**](ivmvirtualmachine-memory.md)<br/>                               | Lectura/escritura<br/> | La cantidad de memoria física en la máquina virtual, en megabytes.<br/>                                                                 |
| [**Mouse**](ivmvirtualmachine-mouse.md)<br/>                                 | Solo lectura<br/>  | El dispositivo de mouse de la máquina virtual.<br/>                                                                                           |
| [**Name**](ivmvirtualmachine-name.md)<br/>                                   | Lectura/escritura<br/> | El nombre de la configuración de la máquina virtual.<br/>                                                                                      |
| [**Adaptadores**](ivmvirtualmachine-networkadapters.md)<br/>             | Solo lectura<br/>  | Colección enumerable de NIC conectada a la máquina virtual.<br/>                                                                   |
| [**Notas**](ivmvirtualmachine-notes.md)<br/>                                 | Lectura/escritura<br/> | Notas de la máquina virtual.<br/>                                                                                                  |
| [**ParallelPorts**](ivmvirtualmachine-parallelports.md)<br/>                 | Solo lectura<br/>  | Colección enumerable de puertos paralelos.<br/>                                                                                         |
| [**Velocidaddeprocesador**](ivmvirtualmachine-processorspeed.md)<br/>               | Solo lectura<br/>  | La velocidad del procesador, en megahercios (MHz).<br/>                                                                                     |
| [**RdpPipeName**](ivmvirtualmachine-rdppipename.md)<br/>                     | Solo lectura<br/>  | Nombre de la canalización con nombre de la conexión RDP utilizada para el vídeo y la entrada.<br/>                                                                     |
| [**SavedStateFilePath**](ivmvirtualmachine-savedstatefilepath.md)<br/>       | Solo lectura<br/>  | Ruta de acceso completa al archivo de estado guardado.<br/>                                                                                              |
| [**SerialPorts**](ivmvirtualmachine-serialports.md)<br/>                     | Solo lectura<br/>  | Colección enumerable de puertos serie.<br/>                                                                                           |
| [**ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)<br/>   | Lectura/escritura<br/> | La acción que se realizará en esta máquina virtual si se ejecuta cuando se cierra Windows Virtual PC.<br/>                                |
| [**State**](ivmvirtualmachine-state.md)<br/>                                 | Solo lectura<br/>  | Estado actual de la máquina virtual.<br/>                                                                                           |
| [**Puede deshacer**](ivmvirtualmachine-undoable.md)<br/>                           | Lectura/escritura<br/> | Indica si las unidades de deshacer están habilitadas para los discos duros conectados a la máquina virtual.<br/>                                      |
| [**UndoAction**](ivmvirtualmachine-undoaction.md)<br/>                       | Lectura/escritura<br/> | La acción predeterminada que debe realizarse en todas las unidades de deshacer cuando se apaga la máquina virtual desde el sistema operativo invitado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



 

