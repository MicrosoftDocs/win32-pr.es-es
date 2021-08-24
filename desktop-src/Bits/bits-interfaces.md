---
title: Interfaces bits
description: Use las siguientes interfaces Servicio de transferencia inteligente en segundo plano (BITS) para transferir archivos y supervisar trabajos dentro de la cola de transferencia.
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: 0edd4229e76a85767689427cfccd6cb38aa11c0e54345053ce10d1a99fc1fde8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529075"
---
# <a name="bits-interfaces"></a>Interfaces bits

Use las siguientes interfaces Servicio de transferencia inteligente en segundo plano (BITS) para transferir archivos y [supervisar trabajos](using-bits.md) dentro de la cola de transferencia.

| Interfaz | Descripción |
|-|-|
| [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | Los clientes implementan [**la interfaz IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) para recibir la notificación de que un trabajo se ha completado, se ha modificado o está en error. |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | Los clientes implementan la [**interfaz IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) para recibir la notificación de que un archivo ha completado la descarga. |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | Los clientes implementan [**la interfaz IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) para recibir la notificación de que los intervalos de un archivo han finalizado la descarga. |
| [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | Recupera los detalles de un error de trabajo. |
| [**IBackgroundCopyFile**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | Recupera los nombres de archivo locales y remotos de una solicitud de transferencia de archivos en el trabajo y su progreso. |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | Especifica un nuevo nombre remoto para el archivo y recupera la lista de intervalos que se van a descargar. |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | Valida el archivo para que los usuarios del mismo nivel puedan solicitar su contenido y recupere el nombre del archivo temporal. |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | Recupera las estadísticas de descarga de los servidores del mismo nivel y de origen. |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | Proporciona métodos genéricos get y set para las propiedades BackgroundCopyFile. |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | Obtiene o establece las propiedades genéricas de las transferencias de archivos BITS. |
| [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | Agrega archivos al trabajo, establece el nivel de prioridad del trabajo, determina el estado del trabajo, inicia y detiene el trabajo. |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | Recupera los datos de respuesta de un trabajo de carga, determina el progreso de la transferencia de datos de respuesta al cliente, solicita la ejecución de la línea de comandos y proporciona credenciales para un servidor proxy y remoto. |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | Descarga los intervalos de un archivo, cambia el prefijo de un nombre de archivo remoto y mantiene la información del propietario y la ACL con el archivo. |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | Habilita el almacenamiento en caché del mismo nivel, restringe el tiempo de descarga e inspecciona las características del token de usuario. |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | Consulta o establece varios comportamientos opcionales de un trabajo. |
| [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | Especifica certificados de cliente para la autenticación de cliente basada en certificados y encabezados personalizados para las solicitudes HTTP. |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | Use esta interfaz para recuperar o invalidar el método HTTP usado para una transferencia de BITS. |
| [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | Crea trabajos de transferencia, recupera un objeto enumerador de trabajos de la cola y recupera trabajos individuales de la cola. |
| [**IBitsPeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | Obtiene información sobre un usuario del mismo nivel en el vecino. |
| [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | Administre el grupo de pares desde el que puede descargar contenido. |
| [**IBitsPeerCacheRecord**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | Obtiene información sobre un archivo en la memoria caché. |
| [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | Asocia y administra un par de tokens de seguridad para un Servicio de transferencia inteligente en segundo plano de transferencia de datos (BITS). |
| [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | Enumera los archivos del trabajo. |
| [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | Enumera los trabajos de la cola de transferencia. |
| [**IEnumBitsPeerCacheRecords**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | Enumera los registros de la memoria caché. |
| [**IEnumBitsPeers**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | Enumera la lista de elementos del mismo nivel que BITS ha detectado. |



 

 

 




