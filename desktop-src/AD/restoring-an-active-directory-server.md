---
title: Restauración de un servidor de Active Directory
description: Los servidores Active Directory deben restaurarse sin conexión.
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- Restaurar Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273d02fd50d6b3bd68a055a6a783566e4ebddcf7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904471"
---
# <a name="restoring-an-active-directory-server"></a>Restauración de un servidor de Active Directory

Los servidores Active Directory deben restaurarse sin conexión. El sistema debe reiniciarse en el modo de restauración de servicios de directorio. En este modo, el sistema operativo se ejecuta sin Active Directory Domain Services y toda la validación de usuarios se produce a través del administrador de cuentas de seguridad (SAM) en el registro. Para restaurar Active Directory Domain Services, use las credenciales de un administrador local en el controlador de dominio que se restaura.

El autor de la llamada de las funciones restore debe tener el privilegio de acceso de **\_ \_ nombre de restauración se** . Utilice la función [**DsSetAuthIdentity**](dssetauthidentity.md) para establecer el contexto de seguridad en el que se llama a las funciones de copia de seguridad y restauración de directorios.

Tenga en cuenta que al restaurar Active Directory Domain Services, también debe restaurar los demás componentes de estado del sistema.

**Para restaurar Active Directory Domain Services**

1.  Llame a la función [**DsIsNTDSOnline**](dsisntdsonline.md) para determinar si Active Directory Domain Services se están ejecutando.
2.  Si Active Directory Domain Services no se están ejecutando, se llama a la función [**DsRestorePrepare**](dsrestoreprepare.md) para inicializar la operación de restauración y obtener un identificador de contexto de copia de seguridad. Si Active Directory Domain Services se están ejecutando, no se puede restaurar y la aplicación de restauración no debe realizar la operación de restauración. La función **DsRestorePrepare** requiere que el token de expiración se obtenga de la función [**DsBackupPrepare**](dsbackupprepare.md) durante la operación de copia de seguridad.
3.  Llame a la función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) para determinar los directorios en los que se van a restaurar los archivos. Si se produce un error en esta función, restaure los datos de nuevo en el directorio de origen de la copia de seguridad original. es el directorio desde el que se realizó la copia de seguridad de los datos.
4.  Llame a la función [**DsRestoreRegister**](dsrestoreregister.md) para preparar el servidor de Active Directory para la operación de restauración y bloquear los directorios de restauración.
5.  Utilice las funciones estándar de Win32 para restaurar los archivos. En primer lugar, elimine todos los archivos del directorio de destino; a continuación, copie los archivos de copia de seguridad en el directorio de destino.
6.  Llame a la función [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) para indicar que la restauración se ha completado.
7.  Llame a la función [**DsRestoreEnd**](dsrestoreend.md) para liberar todos los recursos asociados al contexto.

Después de una restauración en el modo de restauración de servicios de directorio, el controlador de dominio debe reiniciarse en modo normal. Cuando se inicia el servicio de directorio, el controlador de dominio realizará la comprobación de coherencia normal y el directorio restaurado estará en línea.

Tenga en cuenta que la restauración de un servidor de Active Directory siempre es una operación de dos partes. En primer lugar, restaure la base de datos a una hora en la que se realizó la copia de seguridad. En segundo lugar, replique el directorio, donde el DSA recién restaurado Replica las actualizaciones posteriores a la copia de seguridad de otros DSA en el dominio y el bosque de la empresa.

Un equipo que se ejecuta en Windows 2000 o Windows Server 2003, que contiene una réplica del servicio de directorio, es un controlador de dominio.

La función [**DsRestoreRegister**](dsrestoreregister.md) agrega datos al registro que deben sobrevivir al proceso de restauración del registro para que la restauración funcione correctamente. Para asegurarse de que se conservan los datos del registro, restaure Active Directory Domain Services con las funciones **DsRestore \*** antes de reiniciar el equipo después de llamar a la función [**RegReplaceKey**](/windows/desktop/api/winreg/nf-winreg-regreplacekeya) . Este proceso funciona porque **RegReplaceKey** no reemplaza realmente el subárbol del registro hasta que se reinicia el equipo y los datos del registro agregados por la función **DsRestoreRegister** se excluyen específicamente de la sustitución durante una operación de restauración del registro.

 

 