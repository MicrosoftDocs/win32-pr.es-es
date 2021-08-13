---
title: 'Cfgmgr32.h '
description: Esta sección contiene temas de referencia para el encabezado Cfgmgr32.h.
ms.assetid: 73b4b2ec-ce3d-47c1-9b0e-1052f390ae94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd09a0e905b85d2eae52bb267929d2e1e89e5c6c179a8d6ab4de00320e9f8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541429"
---
# <a name="cfgmgr32h"></a>Cfgmgr32.h 

Esta sección contiene temas de referencia para el encabezado Cfgmgr32.h.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_des"><strong>BUSNUMBER_DES</strong></a><br/></td>
<td>La BUSNUMBER_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso del número de bus para una instancia de dispositivo. Para más información sobre las listas de recursos y las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_range"><strong>BUSNUMBER_RANGE</strong></a><br/></td>
<td>La BUSNUMBER_RANGE especifica una lista de requisitos de recursos que describe el uso del número de bus para una instancia de dispositivo. Para obtener más información sobre las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-busnumber_resource"><strong>BUSNUMBER_RESOURCE</strong></a><br/></td>
<td>La BUSNUMBER_RESOURCE especifica una lista de recursos o una lista de requisitos de recursos que describe el uso del número de bus para una instancia de dispositivo. Para más información sobre las listas de recursos y las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a><br/></td>
<td>La <strong>CM_Add_Empty_Log_Conf</strong> crea una configuración lógica vacía <a href="/windows-hardware/drivers/kernel/hardware-resources">para</a>un tipo de configuración especificado y una instancia de dispositivo especificada, en el equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex"><strong>CM_Add_Empty_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf"><strong>CM_Add_Empty_Log_Conf</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Add_Empty_Log_Conf_Ex</strong> crea una configuración lógica vacía <a href="/windows-hardware/drivers/kernel/hardware-resources">,</a>para un tipo de configuración especificado y una instancia de dispositivo especificada, en el equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a><br/></td>
<td>La <strong>CM_Add_ID</strong> agrega un identificador de dispositivo <a href="/windows-hardware/drivers/install/device-ids">especificado</a> (si aún no está presente) <a href="/windows-hardware/drivers/">a</a> la lista de identificadores de <a href="/windows-hardware/drivers/install/hardware-ids">hardware</a> o a la lista de <a href="/windows-hardware/drivers/install/compatible-ids">identificadores compatibles</a> de una instancia de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_id_exw"><strong>CM_Add_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_idw"><strong>CM_Add_ID</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Add_ID_Ex</strong> agrega un identificador de dispositivo <a href="/windows-hardware/drivers/install/device-ids">(si</a> aún no está presente) a la lista de identificadores de <a href="/windows-hardware/drivers/install/hardware-ids">hardware</a> o a la lista de identificadores <a href="/windows-hardware/drivers/install/compatible-ids">compatibles</a> de una instancia de dispositivo, ya sea en el equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a><br/></td>
<td>La <strong>CM_Add_Res_Des</strong> agrega un <a href="/windows-hardware/drivers/">descriptor de recursos</a> a una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des_ex"><strong>CM_Add_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_add_res_des"><strong>CM_Add_Res_Des</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Add_Res_Des_Ex</strong> agrega un <a href="/windows-hardware/drivers/">descriptor de recursos</a> a una <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica</a>. La configuración lógica puede estar en el equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_connect_machinew"><strong>CM_Connect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012 funcionalidad para acceder a máquinas remotas se ha quitado. No se puede acceder a las máquinas remotas cuando se ejecutan en estas versiones de Windows.
</blockquote>
<br/> La <strong>CM_Connect_Machine</strong> crea una conexión a un equipo remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_class_key"><strong>CM_Delete_Class_Key</strong></a><br/></td>
<td>La <strong>CM_Delete_Class_Key</strong> de dispositivo quita la clase de dispositivo <a href="/windows-hardware/drivers/">instalada especificada</a> del sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a><br/></td>
<td>La <strong>CM_Delete_Device_Interface_Key</strong> elimina la subclave del Registro que usan las aplicaciones y los controladores para almacenar información específica de la interfaz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exa"><strong>CM_Delete_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Delete_Device_Interface_Key_ExA</strong> elimina la subclave del Registro que usan las aplicaciones y los controladores para almacenar información específica de la interfaz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_key_exw"><strong>CM_Delete_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_device_interface_keyw"><strong>CM_Delete_Device_Interface_Key</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Delete_Device_Interface_Key_ExW</strong> elimina la subclave del Registro que usan las aplicaciones y los controladores para almacenar información específica de la interfaz.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_delete_devnode_key"><strong>CM_Delete_DevNode_Key</strong></a><br/></td>
<td>La <strong>CM_Delete_DevNode_Key</strong> elimina las claves del Registro accesibles por el usuario especificadas que están asociadas a un dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disable_devnode"><strong>CM_Disable_DevNode</strong></a><br/></td>
<td>La <strong>CM_Disable_DevNode</strong> deshabilita un dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_disconnect_machine"><strong>CM_Disconnect_Machine</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir de Windows 8 y Windows Server 2012 funcionalidad para acceder a máquinas remotas se ha quitado. No se puede acceder a las máquinas remotas cuando se ejecutan en estas versiones de Windows.
</blockquote>
<br/> La <strong>CM_Disconnect_Machine</strong> elimina una conexión a un equipo remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enable_devnode"><strong>CM_Enable_DevNode</strong></a><br/></td>
<td>La <strong>CM_Enable_DevNode</strong> habilita un dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a><br/></td>
<td>La <strong>CM_Enumerate_Classes,</strong> cuando se llama repetidamente, enumera las clases de <a href="/windows-hardware/drivers/"></a> dispositivo instaladas de la máquina local al proporcionar el GUID de cada clase.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes_ex"><strong>CM_Enumerate_Classes_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_classes"><strong>CM_Enumerate_Classes</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Enumerate_Classes_Ex,</strong> cuando se llama repetidamente, enumera las clases de dispositivo instaladas de una máquina local o <a href="/windows-hardware/drivers/">remota,</a>al proporcionar el GUID de cada clase.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a><br/></td>
<td>La <strong>CM_Enumerate_Enumerators</strong> enumera los enumeradores de dispositivos de la máquina local al proporcionar el nombre de cada enumerador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumerators_exw"><strong>CM_Enumerate_Enumerators_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_enumerate_enumeratorsw"><strong>CM_Enumerate_Enumerators</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Enumerate_Enumerators_Ex</strong> enumera los enumeradores de dispositivos de una máquina local o remota, al proporcionar el nombre de cada enumerador.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a><br/></td>
<td>La <strong>CM_Free_Log_Conf</strong> elimina una configuración lógica <a href="/windows-hardware/drivers/kernel/hardware-resources">y</a> todos los descriptores de <a href="/windows-hardware/drivers/">recursos asociados</a> de la máquina local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_ex"><strong>CM_Free_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf"><strong>CM_Free_Log_Conf</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Free_Log_Conf_Ex</strong> elimina una configuración <a href="/windows-hardware/drivers/kernel/hardware-resources"></a> lógica y todos los descriptores de recursos <a href="/windows-hardware/drivers/">asociados</a> de una máquina local o remota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_log_conf_handle"><strong>CM_Free_Log_Conf_Handle</strong></a><br/></td>
<td>La <strong>CM_Free_Log_Conf_Handle</strong> invalida un identificador de configuración lógico y libera su asignación de memoria asociada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a><br/></td>
<td>La <strong>CM_Free_Res_Des</strong> elimina un <a href="/windows-hardware/drivers/">descriptor de recursos</a> de una configuración <a href="/windows-hardware/drivers/kernel/hardware-resources">lógica</a> en el equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_ex"><strong>CM_Free_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des"><strong>CM_Free_Res_Des</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Free_Res_Des_Ex</strong> quita un <a href="/windows-hardware/drivers/">descriptor de recursos de</a> una configuración <a href="/windows-hardware/drivers/kernel/hardware-resources">lógica</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle"><strong>CM_Free_Res_Des_Handle</strong></a><br/></td>
<td>La <strong>CM_Free_Res_Des_Handle</strong> invalida un identificador de descripción de recursos y libera su asignación de memoria asociada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_free_resource_conflict_handle"><strong>CM_Free_Resource_Conflict_Handle</strong></a><br/></td>
<td>La <strong>CM_Free_Resource_Conflict_Handle</strong> invalida un identificador en una lista de conflictos de recursos y libera la asignación de memoria asociada del identificador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a><br/></td>
<td>La <strong>CM_Get_Child</strong> se usa para recuperar un identificador de instancia de dispositivo en el primer nodo secundario de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en el árbol de dispositivos de la <a href="/windows-hardware/drivers/kernel/device-tree">máquina</a>local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child_ex"><strong>CM_Get_Child_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_child"><strong>CM_Get_Child</strong></a> en su lugar.
</blockquote>
<br/> La <strong>función CM_Get_Child_Ex</strong> se usa para recuperar un identificador de instancia de dispositivo en el primer nodo secundario de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en un árbol de dispositivos local o remoto de <a href="/windows-hardware/drivers/kernel/device-tree">una máquina remota.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a><br/></td>
<td>La <strong>CM_Get_Class_Property</strong> recupera una propiedad de dispositivo establecida para una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz de dispositivo</a> o clase de configuración de <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_exw"><strong>CM_Get_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_propertyw"><strong>CM_Get_Class_Property</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Class_Property_ExW</strong> recupera una propiedad de dispositivo establecida para una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz de dispositivo</a> o una clase de configuración de <a href="/windows-hardware/drivers/install/device-setup-classes">dispositivo</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a><br/></td>
<td>La <strong>CM_Get_Class_Property_Keys</strong> recupera una matriz de las claves de propiedad del dispositivo que representan las propiedades del dispositivo que se establecen para una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz</a> de dispositivo o clase de configuración <a href="/windows-hardware/drivers/install/device-setup-classes">de dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys_ex"><strong>CM_Get_Class_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_property_keys"><strong>CM_Get_Class_Property_Keys</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Class_Property_Keys_Ex</strong> recupera una matriz de las claves de propiedad del dispositivo que representan las propiedades del dispositivo que se establecen para una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz</a> de dispositivo o clase de configuración <a href="/windows-hardware/drivers/install/device-setup-classes">de dispositivo</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_class_registry_propertyw"><strong>CM_Get_Class_Registry_Property</strong></a><br/></td>
<td>La <strong>CM_Get_Class_Registry_Property</strong> recupera una propiedad <a href="/windows-hardware/drivers/install/accessing-device-setup-class-properties">de clase de configuración de dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a><br/></td>
<td>La <strong>CM_Get_Depth</strong> se usa para obtener la profundidad de un nodo de dispositivo especificado<a href="/windows-hardware/drivers/">(devnode</a>) en el árbol de dispositivos <a href="/windows-hardware/drivers/kernel/device-tree">de la máquina local.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth_ex"><strong>CM_Get_Depth_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_depth"><strong>CM_Get_Depth</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Depth_Ex</strong> se usa para obtener la profundidad de un nodo de dispositivo especificado<a href="/windows-hardware/drivers/">(devnode</a>) dentro del árbol de dispositivos de un equipo local <a href="/windows-hardware/drivers/kernel/device-tree">o remoto.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a><br/></td>
<td>La <strong>CM_Get_Device_ID</strong> recupera el identificador de instancia <a href="/windows-hardware/drivers/install/device-instance-ids">de dispositivo</a> para una instancia de dispositivo <a href="/windows-hardware/drivers/">especificada</a> en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_exw"><strong>CM_Get_Device_ID_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_idw"><strong>CM_Get_Device_ID</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Device_ID_Ex</strong> recupera el identificador de instancia de <a href="/windows-hardware/drivers/install/device-instance-ids">dispositivo</a> para una instancia de <a href="/windows-hardware/drivers/">dispositivo</a> especificada en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a><br/></td>
<td>La <strong>CM_Get_Device_ID_List</strong> recupera una lista de los <a href="/windows-hardware/drivers/install/device-instance-ids">IDs</a> de instancia de dispositivo para las instancias de dispositivo <a href="/windows-hardware/drivers/">del equipo local.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_exw"><strong>CM_Get_Device_ID_List_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_lista"><strong>CM_Get_Device_ID_List</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Device_ID_List_Ex</strong> recupera una lista de los <a href="/windows-hardware/drivers/install/device-instance-ids">IDs</a> de instancia de dispositivo para las instancias de dispositivo <a href="/windows-hardware/drivers/">en</a> un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a><br/></td>
<td>La <strong>CM_Get_Device_ID_List_Size</strong> recupera el tamaño de búfer necesario para contener una lista de los <a href="/windows-hardware/drivers/install/device-instance-ids">IDs</a> de instancia de dispositivo para las instancias de dispositivo de <a href="/windows-hardware/drivers/">la máquina local.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_size_exw"><strong>CM_Get_Device_ID_List_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_list_sizea"><strong>CM_Get_Device_ID_List_Size</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Device_ID_List_Size_Ex</strong> recupera el tamaño de búfer necesario para contener una lista de los <a href="/windows-hardware/drivers/install/device-instance-ids">IDs</a> de instancia de dispositivo para las instancias de dispositivo de un equipo local <a href="/windows-hardware/drivers/">o remoto.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a><br/></td>
<td>La <strong>CM_Get_Device_ID_Size</strong> recupera el tamaño de búfer necesario <a href="/windows-hardware/drivers/install/device-instance-ids"></a> para contener un identificador de instancia de dispositivo para una instancia de dispositivo <a href="/windows-hardware/drivers/">en</a> el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size_ex"><strong>CM_Get_Device_ID_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_id_size"><strong>CM_Get_Device_ID_Size</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Device_ID_Size_Ex</strong> recupera el tamaño de búfer necesario <a href="/windows-hardware/drivers/install/device-instance-ids"></a> para contener <a href="/windows-hardware/drivers/"></a> un identificador de instancia de dispositivo para una instancia de dispositivo en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_aliasw"><strong>CM_Get_Device_Interface_Alias</strong></a><br/></td>
<td>La <strong>CM_Get_Device_Interface_Alias</strong> devuelve el alias de la instancia de interfaz de dispositivo especificada, si el alias existe.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a><br/></td>
<td>La <strong>CM_Get_Device_Interface_List</strong> recupera una lista de instancias de interfaz de dispositivo que pertenecen a una clase de <a href="/windows-hardware/drivers/install/device-interface-classes">interfaz de dispositivo especificada.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_list_sizea"><strong>CM_Get_Device_Interface_List_Size</strong></a><br/></td>
<td>La <strong>CM_Get_Device_Interface_List_Size</strong> recupera el tamaño de búfer que se debe pasar a la <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_lista"><strong>CM_Get_Device_Interface_List</strong></a> de almacenamiento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a><br/></td>
<td>La <strong>CM_Get_Device_Interface_Property</strong> recupera una propiedad de dispositivo establecida para una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_exw"><strong>CM_Get_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_propertyw"><strong>CM_Get_Device_Interface_Property</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Device_Interface_Property_ExW</strong> recupera una propiedad de dispositivo establecida para una interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a><br/></td>
<td>La <strong>CM_Get_Device_Interface_Property_Keys</strong> recupera una matriz de claves de propiedad de dispositivo que representan las propiedades del dispositivo que se establecen para una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keys_exw"><strong>CM_Get_Device_Interface_Property_Keys_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_device_interface_property_keysw"><strong>CM_Get_Device_Interface_Property_Keys</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Device_Interface_Property_Keys_ExW</strong> recupera una matriz de claves de propiedad de dispositivo que representan las propiedades del dispositivo que se establecen para una interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a><br/></td>
<td>La <strong>CM_Get_DevNode_Property</strong> recupera una propiedad de instancia de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_exw"><strong>CM_Get_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_propertyw"><strong>CM_Get_DevNode_Property</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_DevNode_Property_ExW</strong> recupera una propiedad de instancia de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a><br/></td>
<td>La <strong>CM_Get_DevNode_Property_Keys</strong> recupera una matriz de las claves de propiedad del dispositivo que representan las propiedades del dispositivo que se establecen para una instancia de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys_ex"><strong>CM_Get_DevNode_Property_Keys_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_property_keys"><strong>CM_Get_DevNode_Property_Keys</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_DevNode_Property_Keys_Ex</strong> recupera una matriz de las claves de propiedad del dispositivo que representan las propiedades del dispositivo que se establecen para una instancia de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_registry_propertyw"><strong>CM_Get_DevNode_Registry_Property</strong></a><br/></td>
<td>La <strong>CM_Get_DevNode_Registry_Property</strong> recupera una propiedad de dispositivo especificada del Registro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a><br/></td>
<td>La <strong>CM_Get_DevNode_Status</strong> obtiene el estado de una instancia de dispositivo de su nodo de dispositivo (<a href="/windows-hardware/drivers/">devnode</a>) en el árbol de dispositivos de <a href="/windows-hardware/drivers/kernel/device-tree">la máquina local.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status_ex"><strong>CM_Get_DevNode_Status_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_devnode_status"><strong>CM_Get_DevNode_Status</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_DevNode_Status_Ex</strong> obtiene el estado de una instancia de dispositivo de su nodo de dispositivo (<a href="/windows-hardware/drivers/">devnode</a>) en un árbol de dispositivos local o <a href="/windows-hardware/drivers/kernel/device-tree">remoto del equipo.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a><br/></td>
<td>La <strong>CM_Get_First_Log_Conf</strong> obtiene la primera configuración lógica <a href="/windows-hardware/drivers/kernel/hardware-resources">,</a>de un tipo de configuración especificado, asociada a una instancia de dispositivo especificada <a href="/windows-hardware/drivers/">en</a> el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex"><strong>CM_Get_First_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf"><strong>CM_Get_First_Log_Conf</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_First_Log_Conf_Ex</strong> obtiene la primera configuración <a href="/windows-hardware/drivers/kernel/hardware-resources">lógica asociada</a> a una instancia de <a href="/windows-hardware/drivers/">dispositivo</a> especificada en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flagsa"><strong>CM_Get_HW_Prof_Flags</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso y no debe usarse.
</blockquote>
<br/> La <strong>CM_Get_HW_Prof_Flags</strong> recupera las marcas de configuración específicas del perfil de <a href="/windows-hardware/drivers/">hardware</a>para una instancia <a href="/windows-hardware/drivers/">de dispositivo</a> en un equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_hw_prof_flags_exa"><strong>CM_Get_HW_Prof_Flags_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función está en desuso y no se debe usar.
</blockquote>
<br/> La <strong>CM_Get_HW_Prof_Flags_Ex</strong> recupera las marcas de configuración específicas del <a href="/windows-hardware/drivers/"></a> perfil de <a href="/windows-hardware/drivers/">hardware</a>para una instancia de dispositivo en un equipo remoto o en un equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a><br/></td>
<td>La <strong>CM_Get_Log_Conf_Priority</strong> obtiene la prioridad de configuración de una configuración <a href="/windows-hardware/drivers/kernel/hardware-resources">lógica especificada</a> en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority_ex"><strong>CM_Get_Log_Conf_Priority_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_log_conf_priority"><strong>CM_Get_Log_Conf_Priority</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Log_Conf_Priority_Ex</strong> obtiene la prioridad de configuración de una configuración <a href="/windows-hardware/drivers/kernel/hardware-resources">lógica especificada</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a><br/></td>
<td>La <strong>CM_Get_Next_Log_Conf</strong> obtiene la siguiente <a href="/windows-hardware/drivers/kernel/hardware-resources">configuración lógica asociada</a> a una instancia de dispositivo <a href="/windows-hardware/drivers/">específica</a> en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex"><strong>CM_Get_Next_Log_Conf_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf"><strong>CM_Get_Next_Log_Conf</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Next_Log_Conf_Ex</strong> obtiene la siguiente configuración <a href="/windows-hardware/drivers/kernel/hardware-resources">lógica</a> asociada a una instancia <a href="/windows-hardware/drivers/">de dispositivo</a> específica en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a><br/></td>
<td>La <strong>CM_Get_Next_Res_Des</strong> obtiene un identificador para el <a href="/windows-hardware/drivers/">siguiente descriptor</a>de recursos , de un tipo de recurso especificado, para una configuración lógica en el equipo local. <a href="/windows-hardware/drivers/kernel/hardware-resources"></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des_ex"><strong>CM_Get_Next_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_next_res_des"><strong>CM_Get_Next_Res_Des</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Next_Res_Des_Ex</strong> obtiene un identificador para el <a href="/windows-hardware/drivers/">siguiente descriptor</a>de recursos , de <a href="/windows-hardware/drivers/kernel/hardware-resources"></a> un tipo de recurso especificado, para una configuración lógica en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a><br/></td>
<td>La <strong>CM_Get_Parent</strong> obtiene un identificador de instancia de dispositivo para el nodo primario de un nodo de dispositivo especificado<a href="/windows-hardware/drivers/">(devnode</a>) en el árbol de dispositivos de la máquina local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent_ex"><strong>CM_Get_Parent_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_parent"><strong>CM_Get_Parent</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Parent_Ex</strong> obtiene un identificador de instancia de dispositivo para el nodo primario de un nodo de dispositivo especificado<a href="/windows-hardware/drivers/">(devnode</a>) en un árbol de dispositivos local o remoto del <a href="/windows-hardware/drivers/kernel/device-tree">equipo.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a><br/></td>
<td>La <strong>CM_Get_Res_Des_Data</strong> recupera la información almacenada en un <a href="/windows-hardware/drivers/">descriptor de recursos</a> en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_ex"><strong>CM_Get_Res_Des_Data_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data"><strong>CM_Get_Res_Des_Data</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Res_Des_Data_Ex</strong> recupera la información almacenada en un <a href="/windows-hardware/drivers/">descriptor de recursos</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a><br/></td>
<td>La <strong>CM_Get_Res_Des_Data_Size</strong> obtiene el tamaño de búfer necesario para contener la información contenida en un descriptor de recursos <a href="/windows-hardware/drivers/">especificado</a> en el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size_ex"><strong>CM_Get_Res_Des_Data_Size_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_res_des_data_size"><strong>CM_Get_Res_Des_Data_Size</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Res_Des_Data_Size_Ex</strong> obtiene el tamaño de búfer necesario para contener la información contenida en un descriptor de recursos <a href="/windows-hardware/drivers/">especificado</a> en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_count"><strong>CM_Get_Resource_Conflict_Count</strong></a><br/></td>
<td>La <strong>CM_Get_Resource_Conflict_Count</strong> de recursos obtiene el número de conflictos contenidos en una lista de conflictos de recursos especificada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a><br/></td>
<td>La <strong>CM_Get_Resource_Conflict_Details</strong> obtiene los detalles sobre uno de los conflictos de recursos de una lista de conflictos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a><br/></td>
<td>La <strong>CM_Get_Sibling</strong> obtiene un identificador de instancia de dispositivo al siguiente nodo relacionado de un nodo de dispositivo especificado (<a href="/windows-hardware/drivers/">devnode</a>) en el árbol de dispositivos de la <a href="/windows-hardware/drivers/kernel/device-tree">máquina</a>local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling_ex"><strong>CM_Get_Sibling_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_sibling"><strong>CM_Get_Sibling</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Get_Sibling_Ex</strong> obtiene un identificador de instancia de dispositivo al siguiente nodo relacionado de un nodo de dispositivo especificado, en un árbol de dispositivos local o <a href="/windows-hardware/drivers/kernel/device-tree">remoto del equipo.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version"><strong>CM_Get_Version</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso y no debe usarse.
</blockquote>
<br/> La <strong>función CM_Get_Version</strong> devuelve la versión 4.0 de Plug and Play (PnP) Administrador de configuración <a href="/windows-hardware/drivers/">DLL</a> (<em>Cfgmgr32.dll</em>) para una máquina local. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_version_ex"><strong>CM_Get_Version_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso y no debe usarse.
</blockquote>
<br/> La <strong>función CM_Get_Version_Ex</strong> devuelve la versión 4.0 del archivo <a href="/windows-hardware/drivers/">DLL</a> de Plug and Play (PnP) Administrador de configuración (<em>Cfgmgr32.dll</em>) para un equipo local o remoto. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a><br/></td>
<td>La <strong>CM_Is_Dock_Station_Present</strong> identifica si una <a href="/windows-hardware/drivers/">estación de acoplamiento</a> está presente en una máquina local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present_ex"><strong>CM_Is_Dock_Station_Present_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_dock_station_present"><strong>CM_Is_Dock_Station_Present</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Is_Dock_Station_Present_Ex</strong> identifica si una estación de <a href="/windows-hardware/drivers/">acoplamiento</a> está presente en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available"><strong>CM_Is_Version_Available</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso y no debe usarse.
</blockquote>
<br/> La <strong>CM_Is_Version_Available</strong> indica si una máquina local admite una versión especificada del archivo <a href="/windows-hardware/drivers/">DLL</a> de Plug and Play (PnP) Administrador de configuración (<em>Cfgmgr32.dll</em>).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_is_version_available_ex"><strong>CM_Is_Version_Available_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso y no debe usarse.
</blockquote>
<br/> La <strong>función CM_Is_Version_Available_Ex</strong> indica si una versión especificada del archivo <a href="/windows-hardware/drivers/">DLL</a> de Plug and Play (PNP) Administrador de configuración (<em>Cfgmgr32.dll</em>) es compatible con una máquina local o remota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a><br/></td>
<td>La <strong>CM_Locate_DevNode</strong> de dispositivo obtiene un identificador de instancia de dispositivo para el nodo de dispositivo que está asociado a un identificador de instancia de dispositivo especificado <a href="/windows-hardware/drivers/install/device-instance-ids">en</a> el equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnode_exw"><strong>CM_Locate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_locate_devnodea"><strong>CM_Locate_DevNode</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Locate_DevNode_Ex</strong> de dispositivo obtiene un identificador de instancia de dispositivo para el nodo de dispositivo que está asociado a un identificador de instancia de dispositivo <a href="/windows-hardware/drivers/install/device-instance-ids">especificado,</a>en un equipo local o en un equipo remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_mapcrtowin32err"><strong>CM_MapCrToWin32Err</strong></a><br/></td>
<td>Convierte un código <strong>CONFIGRET especificado</strong> en su código de error del sistema equivalente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a><br/></td>
<td>La <strong>CM_Modify_Res_Des</strong> modifica un descriptor de recursos especificado en el equipo local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des_ex"><strong>CM_Modify_Res_Des_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_modify_res_des"><strong>CM_Modify_Res_Des</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Modify_Res_Des_Ex</strong> modifica un descriptor de recursos especificado en un equipo local o remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ne-cfgmgr32-cm_notify_action"><strong>CM_NOTIFY_ACTION</strong></a><br/></td>
<td>Esta enumeración identifica Plug and Play de eventos de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_event_data"><strong>CM_NOTIFY_EVENT_DATA</strong></a><br/></td>
<td>Se trata de una estructura de datos de eventos de notificación de dispositivos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/ns-cfgmgr32-cm_notify_filter"><strong>CM_NOTIFY_FILTER</strong></a><br/></td>
<td>Estructura del filtro de notificación de dispositivos<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_class_keyw"><strong>CM_Open_Class_Key</strong></a><br/></td>
<td>La <strong>CM_Open_Class_Key</strong> abre la clave del Registro de la clase de configuración del dispositivo, la clave del Registro de clase de interfaz de dispositivo o una subclave específica de una clase.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a><br/></td>
<td>La <strong>CM_Open_Device_Interface_Key</strong> abre la subclave del Registro que usan las aplicaciones y los controladores para almacenar información específica de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keya"><strong>CM_Open_Device_Interface_Key_ExA</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Open_Device_Interface_Key_ExA</strong> abre la subclave del Registro que usan las aplicaciones y los controladores para almacenar información específica de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_device_interface_key_exw"><strong>CM_Open_Device_Interface_Key_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_open_device_interface_keyw"><strong>CM_Open_Device_Interface_Key</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Open_Device_Interface_Key_ExW</strong> abre la subclave del Registro que usan las aplicaciones y los controladores para almacenar información específica de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_open_devnode_key"><strong>CM_Open_DevNode_Key</strong></a><br/></td>
<td>La <strong>CM_Open_DevNode_Key</strong> abre una clave del Registro para la información de configuración específica del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a><br/></td>
<td>La <strong>CM_Query_And_Remove_SubTree</strong> comprueba si se puede quitar una instancia de dispositivo y sus elementos secundarios y, si es así, los quita.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtree_exw"><strong>CM_Query_And_Remove_SubTree_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_and_remove_subtreew"><strong>CM_Query_And_Remove_SubTree</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Query_And_Remove_SubTree_Ex</strong> comprueba si se puede quitar una instancia de dispositivo y sus elementos secundarios y, si es así, los quita.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_query_resource_conflict_list"><strong>CM_Query_Resource_Conflict_List</strong></a><br/></td>
<td>La <strong>CM_Query_Resource_Conflict_List</strong> identifica las instancias de dispositivo que tienen requisitos de recursos que están en conflicto con la descripción del recurso de una instancia de dispositivo especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a><br/></td>
<td>La <strong>CM_Reenumerate_DevNode</strong> enumera los dispositivos identificados por un nodo de dispositivo especificado y todos sus elementos secundarios.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode_ex"><strong>CM_Reenumerate_DevNode_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_reenumerate_devnode"><strong>CM_Reenumerate_DevNode</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Reenumerate_DevNode_Ex</strong> enumera los dispositivos identificados por un nodo de dispositivo especificado y todos sus elementos secundarios.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a><br/></td>
<td>Use <a href="/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa"><strong>RegisterDeviceNotification en</strong></a> lugar <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>de CM_Register_Notification</strong></a> si el código tiene como destino Windows 7 o versiones anteriores de Windows. Los llamadores del modo kernel deben usar <a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-ioregisterplugplaynotification"><strong>IoRegisterPlugPlayNotification en su</strong></a> lugar.<br/> La <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_register_notification"><strong>CM_Register_Notification</strong></a> registra una rutina de devolución de llamada de aplicación a la que se llamará cuando se produzca un evento PnP del tipo especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a><br/></td>
<td>La <strong>CM_Request_Device_Eject</strong> prepara una instancia de dispositivo local para su eliminación segura, si el dispositivo es extraíble. Si el dispositivo se puede expulsar físicamente, lo será.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_eject_exw"><strong>CM_Request_Device_Eject_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_device_ejectw"><strong>CM_Request_Device_Eject</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Request_Device_Eject_Ex</strong> prepara una instancia de dispositivo local o remota para su eliminación segura, si el dispositivo es extraíble. Si el dispositivo se puede expulsar físicamente, lo será.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a><br/></td>
<td>La <strong>CM_Request_Eject_PC</strong> solicita que se expulse un equipo portátil, que se inserta en una estación <a href="/windows-hardware/drivers/">de</a>acoplamiento local.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc_ex"><strong>CM_Request_Eject_PC_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_request_eject_pc"><strong>CM_Request_Eject_PC</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Request_Eject_PC_Ex</strong> solicita que se expulse un equipo portátil, que <a href="/windows-hardware/drivers/"></a>se inserta en una estación de acoplamiento local o remota.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a><br/></td>
<td>La <strong>CM_Set_Class_Property</strong> establece una propiedad de clase para una clase de configuración de dispositivo o una clase de interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_property_exw"><strong>CM_Set_Class_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_propertyw"><strong>CM_Set_Class_Property</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Set_Class_Property_ExW</strong> establece una propiedad de clase para una clase de configuración de dispositivo o una clase de interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_class_registry_propertyw"><strong>CM_Set_Class_Registry_Property</strong></a><br/></td>
<td>La <strong>CM_Set_Class_Registry_Property</strong> establece o elimina una propiedad de una clase <a href="/windows-hardware/drivers/install/device-setup-classes">de configuración de dispositivo</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a><br/></td>
<td>La <strong>CM_Set_Device_Interface_Property</strong> establece una propiedad de dispositivo de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_property_exw"><strong>CM_Set_Device_Interface_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_device_interface_propertyw"><strong>CM_Set_Device_Interface_Property</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Set_Device_Interface_Property_ExW</strong> establece una propiedad de dispositivo de una interfaz de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a><br/></td>
<td>La <strong>CM_Set_DevNode_Problem</strong> establece un código de problema para un dispositivo que está instalado en un equipo local.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem_ex"><strong>CM_Set_DevNode_Problem_Ex</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_problem"><strong>CM_Set_DevNode_Problem</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Set_DevNode_Problem_Ex</strong> establece un código de problema para un dispositivo que está instalado en un equipo local o remoto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a><br/></td>
<td>La <strong>CM_Set_DevNode_Property</strong> establece una propiedad de instancia de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_property_exw"><strong>CM_Set_DevNode_Property_ExW</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A partir Windows 8 y Windows Server 2012, esta función ha quedado en desuso. Use <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_propertyw"><strong>CM_Set_DevNode_Property</strong></a> en su lugar.
</blockquote>
<br/> La <strong>CM_Set_DevNode_Property_ExW</strong> establece una propiedad de instancia de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_set_devnode_registry_propertyw"><strong>CM_Set_DevNode_Registry_Property</strong></a><br/></td>
<td>La <strong>CM_Set_DevNode_Registry_Property</strong> establece una propiedad de dispositivo especificada en el Registro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_setup_devnode"><strong>CM_Setup_DevNode</strong></a><br/></td>
<td>La <strong>CM_Setup_DevNode</strong> reinicia una instancia de dispositivo que no se está ejecutando porque hay un problema con la configuración del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_uninstall_devnode"><strong>CM_Uninstall_DevNode</strong></a><br/></td>
<td>La <strong>CM_Uninstall_DevNode</strong> elimina todo el estado persistente asociado a una instancia de dispositivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_unregister_notification"><strong>CM_Unregister_Notification</strong></a><br/></td>
<td>Use <a href="/windows/desktop/api/winuser/nf-winuser-unregisterdevicenotification"><strong>UnregisterDeviceNotification en</strong></a> lugar <strong>de CM_Unregister_Notification</strong> si el código tiene como destino Windows 7 o versiones anteriores de Windows.<br/> La <strong>CM_Unregister_Notification</strong> cierre el identificador HCMNOTIFICATION especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_waitnopendinginstallevents"><strong>CMP_WaitNoPendingInstallEvents</strong></a><br/></td>
<td>La <strong>CMP_WaitNoPendingInstallEvents</strong> espera hasta que no haya ninguna actividad de instalación de dispositivo pendiente para que el administrador de PnP realice.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/cfgmgr32/ns-cfgmgr32-conflict_details_a"><strong>CONFLICT_DETAILS</strong></a><br/></td>
<td>La CONFLICT_DETAILS estructura se usa como parámetro para la <a href="/windows/desktop/api/Cfgmgr32/nf-cfgmgr32-cm_get_resource_conflict_detailsw"><strong>CM_Get_Resource_Conflict_Details</strong></a> función.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_des"><strong>CS_DES</strong></a><br/></td>
<td>La CS_DES se usa para especificar una lista de recursos que describe el uso de recursos específicos de la clase de dispositivo para una instancia de dispositivo. Para obtener más información sobre las listas de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-cs_resource"><strong>CS_RESOURCE</strong></a><br/></td>
<td>La CS_RESOURCE se usa para especificar una lista de recursos que describe el uso de recursos específicos de la clase de dispositivo para una instancia de dispositivo. Para obtener más información sobre las listas de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_des"><strong>DMA_DES</strong></a><br/></td>
<td>La DMA_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso del canal de acceso directo a memoria (DMA) para una instancia de dispositivo. Para obtener más información sobre las listas de recursos y las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_range"><strong>DMA_RANGE</strong></a><br/></td>
<td>La DMA_RANGE especifica una lista de requisitos de recursos que describe el uso del canal DMA para una instancia de dispositivo. Para obtener más información sobre las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-dma_resource"><strong>DMA_RESOURCE</strong></a><br/></td>
<td>La DMA_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso del canal DMA para una instancia de dispositivo. Para obtener más información sobre la lista de recursos y las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_des"><strong>IO_DES</strong></a><br/></td>
<td>La IO_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de puertos de E/S para una instancia de dispositivo. Para obtener más información sobre las listas de recursos y las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_range"><strong>IO_RANGE</strong></a><br/></td>
<td>La IO_RANGE especifica una lista de requisitos de recursos que describe el uso de puertos de E/S para una instancia de dispositivo. Para obtener más información sobre las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-io_resource"><strong>IO_RESOURCE</strong></a><br/></td>
<td>La IO_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de puertos de E/S para una instancia de dispositivo. Para obtener más información sobre las listas de recursos y las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_des_64"><strong>IRQ_DES</strong></a><br/></td>
<td>La IRQ_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de la línea IRQ para una instancia de dispositivo. Para obtener más información sobre las listas de recursos y las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_range"><strong>IRQ_RANGE</strong></a><br/></td>
<td>La IRQ_RANGE especifica una lista de requisitos de recursos que describe el uso de la línea IRQ para una instancia de dispositivo. Para obtener más información sobre las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-irq_resource_64"><strong>IRQ_RESOURCE</strong></a><br/></td>
<td>La IRQ_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de la línea IRQ para una instancia de dispositivo. Para obtener más información sobre las listas de recursos y las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_des"><strong>MEM_DES</strong></a><br/></td>
<td>La MEM_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de memoria para una instancia de dispositivo. Para obtener más información sobre las listas de recursos y las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_range"><strong>MEM_RANGE</strong></a><br/></td>
<td>La MEM_RANGE especifica una lista de requisitos de recursos que describe el uso de memoria para una instancia de dispositivo. Para obtener más información sobre las listas de requisitos de recursos, vea <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mem_resource"><strong>MEM_RESOURCE</strong></a><br/></td>
<td>La MEM_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de memoria para una instancia de dispositivo. Para más información sobre las listas de recursos y las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_des"><strong>MFCARD_DES</strong></a><br/></td>
<td>La MFCARD_DES se usa para especificar una lista de recursos o una lista <em></em> de requisitos de recursos que describe el uso de recursos por una de las funciones de hardware proporcionadas por una instancia de un dispositivo multifunción. Para más información sobre las listas de recursos y las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-mfcard_resource"><strong>MFCARD_RESOURCE</strong></a><br/></td>
<td>La MFCARD_RESOURCE se usa para especificar una lista de recursos o una lista <em></em> de requisitos de recursos que describe el uso de recursos por una de las funciones de hardware proporcionadas por una instancia de un dispositivo multifunción. Para más información sobre las listas de recursos y las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_des"><strong>PCCARD_DES</strong></a><br/></td>
<td>La PCCARD_DES se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de recursos por parte de una PC Card recursos. Para más información sobre las listas de recursos y las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/cfgmgr32/ns-cfgmgr32-pccard_resource"><strong>PCCARD_RESOURCE</strong></a><br/></td>
<td>La PCCARD_RESOURCE se usa para especificar una lista de recursos o una lista de requisitos de recursos que describe el uso de recursos por parte de una PC Card recursos. Para más información sobre las listas de recursos y las listas de requisitos de recursos, consulte <a href="/windows-hardware/drivers/kernel/hardware-resources">Recursos de hardware.</a><br/></td>
</tr>
</tbody>
</table>



 

 

 

[Envío de comentarios sobre este tema a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Cfgmgr32.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Envío de comentarios sobre este tema a Microsoft")