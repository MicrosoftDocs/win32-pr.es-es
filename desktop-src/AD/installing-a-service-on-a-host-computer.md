---
title: Instalación de un servicio en un equipo host
description: En el ejemplo de código siguiente se muestran los pasos básicos para instalar un servicio habilitado para directorios en un equipo host.
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0d22098b0a6b823aa5b7db50c20b5a5e2c80c7e540ffdb95e4e2f73c2550fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187393"
---
# <a name="installing-a-service-on-a-host-computer"></a>Instalación de un servicio en un equipo host

En el ejemplo de código siguiente se muestran los pasos básicos para instalar un servicio habilitado para directorios en un equipo host. Realiza las siguientes operaciones:

1.  Llama a [**la función OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) para abrir un identificador para el administrador de control de servicios (SCM) en el equipo local.
2.  Llama a [**la función CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar el servicio en la base de datos de SCM. Esta llamada especifica la cuenta de inicio de sesión y la contraseña del servicio, así como el archivo ejecutable del servicio y otra información sobre el servicio. **CreateService produce un** error si la cuenta de inicio de sesión especificada no es válida. Sin embargo, **CreateService** no comprueba la validez de la contraseña. Tampoco comprueba que la cuenta tenga el inicio de sesión como servicio directamente en el equipo local. Para obtener más información, vea [Conceder inicio de sesión como derecho de servicio en el equipo host](granting-logon-as-service-right-on-the-host-computer.md).
3.  Llama a la subrutina **ScpCreate** del servicio que crea un objeto de punto de conexión de servicio (SCP) en el directorio para publicar la ubicación de esta instancia del servicio. Para obtener más información, vea [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md). Esta rutina también almacena la información de enlace del servicio en el SCP, establece una ACE en el SCP para que el servicio pueda acceder a ella en tiempo de ejecución, almacena en caché el nombre distintivo del SCP en el registro local y devuelve el nombre distintivo del nuevo SCP.
4.  Llama a la subrutina **SpnCompose** del servicio que usa la cadena de clase del servicio y el nombre distintivo del SCP para crear un nombre de entidad de seguridad de servicio (SPN). Para obtener más información, [vea Crear los SPN para un servicio con un SCP.](composing-the-spns-for-a-service-with-an-scp.md) El SPN identifica de forma única esta instancia del servicio.
5.  Llama a la subrutina **SpnRegister** del servicio que registra el SPN en el objeto de cuenta asociado a la cuenta de inicio de sesión del servicio. Para obtener más información, [vea Registrar los SPN para un servicio](registering-the-spns-for-a-service.md). El registro del SPN permite a las aplicaciones cliente autenticar el servicio.

Este ejemplo de código funciona correctamente independientemente de si la cuenta de inicio de sesión es una cuenta de usuario local o de dominio o la cuenta LocalSystem. Para una cuenta de usuario de dominio, el parámetro *szServiceAccountSAM* contiene el nombre de usuario Domain* de la cuenta y el parámetro ***\\**  *szServiceAccountDN* contiene el nombre distintivo del objeto de cuenta de usuario en el directorio. Para la cuenta LocalSystem, *szServiceAccountSAM* y *szPassword* son **NULL** y *szServiceAccountSN* es el nombre distintivo del objeto de cuenta del equipo local en el directorio. Si *szServiceAccountSAM* especifica una cuenta de usuario \\ local (el formato de nombre es ".* UserName*"), el ejemplo de código omite el registro de SPN porque no se admite la autenticación mutua para las cuentas de usuario locales.

Tenga en cuenta que la configuración de seguridad predeterminada solo permite a los administradores de dominio ejecutar este código.

Además, tenga en cuenta que este ejemplo de código, tal como está escrito, debe ejecutarse en el equipo donde se instala el servicio. Por lo tanto, normalmente se encuentra en un ejecutable de instalación independiente del código de instalación del servicio, si existe, que extiende el esquema, extiende la interfaz de usuario o configura la directiva de grupo. Esas operaciones instalan componentes de servicio para todo un bosque, mientras que este código instala el servicio en un único equipo.


```C++
void InstallServiceOnLocalComputer(
            LPTSTR szServiceAccountDN,  // Distinguished name of logon account.
            LPTSTR szServiceAccountSAM, // SAM name of logon account.
            LPTSTR szPassword)          // Password of logon account.
{
SC_HANDLE   schService = NULL;
SC_HANDLE   schSCManager = NULL;
TCHAR szPath[512];
LPTSTR lpFilePart;
TCHAR szDNofSCP[MAX_PATH];
TCHAR szServiceClass[]=TEXT("ADSockAuth");
 
DWORD dwStatus;
TCHAR **pspn=NULL;
ULONG ulSpn=1;
 
// Get the full path of the service's executable.
// The code example assumes that the executable is in the current directory.
dwStatus = GetFullPathName(TEXT("service.exe"), 512, szPath, &lpFilePart);
if (dwStatus == 0) {
    _tprintf(TEXT("Unable to install %s - %s\n"), 
            TEXT(SZSERVICEDISPLAYNAME), GetLastErrorText(szErr, 256));
    return;
}
_tprintf(TEXT("path of service.exe: %s\n"), szPath);
 
// Open the Service Control Manager on the local computer.
schSCManager = OpenSCManager(
                NULL,                   // Computer (NULL == local)
                NULL,                   // Database (NULL == default)
                SC_MANAGER_ALL_ACCESS   // Access required
                );
if (! schSCManager) {
    _tprintf(TEXT("OpenSCManager failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
        
// Install the service in the SCM database.
schService = CreateService(
            schSCManager,               // SCManager database
            TEXT(SZSERVICENAME),        // Name of service
            TEXT(SZSERVICEDISPLAYNAME), // Name to display
            SERVICE_ALL_ACCESS,         // Desired access
            SERVICE_WIN32_OWN_PROCESS,  // Service type
            SERVICE_DEMAND_START,       // Start type
            SERVICE_ERROR_NORMAL,       // Error control type
            szPath,                     // Service binary
            NULL,                       // No load ordering group
            NULL,                       // No tag identifier
            TEXT(SZDEPENDENCIES),       // Dependencies
            szServiceAccountSAM,        // Service account
            szPassword);                // Account password
if (! schService) {
    _tprintf(TEXT("CreateService failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
 
_tprintf(TEXT("%s installed.\n"), TEXT(SZSERVICEDISPLAYNAME) );
 
// Create the service's Service Connection Point (SCP).
dwStatus = ScpCreate(
        2000,                 // Service default port number
        szServiceClass,       // Specifies the service class string
        szServiceAccountSAM,  // SAM name of logon account for ACE
        szDNofSCP             // Buffer returns the DN of the SCP
        );
if (dwStatus != 0) {
    _tprintf(TEXT("ScpCreate failed: %d\n"), dwStatus );
    DeleteService(schService);
    goto cleanup;
}
 
// Compose and register a service principal name for this service.
// This is performed on the install path because this requires elevated
// privileges for updating the directory.
// If a local account of the format ".\user name", skip the SPN.
if ( szServiceAccountSAM[0] == '.' ) 
{
    _tprintf(TEXT("Do not register SPN for a local account.\n"));
    goto cleanup;
}
 
dwStatus = SpnCompose(
        &pspn,            // Receives pointer to the SPN array.
        &ulSpn,           // Receives number of SPNs returned.
        szDNofSCP,        // Input: DN of the SCP.
        szServiceClass);  // Input: the service's class string.
 
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
        szServiceAccountDN,  // Account on which SPNs are registered.
        pspn,                // Array of SPNs to register.
        ulSpn,               // Number of SPNs in array.
        DS_SPN_ADD_SPN_OP);  // Operation code: Add SPNs.
 
if (dwStatus != NO_ERROR) 
{
    _tprintf(TEXT("Failed to compose SPN: Error was %X\n"), 
                  dwStatus);
    DeleteService(schService);
    ScpDelete(szDNofSCP, szServiceClass, szServiceAccountDN);
    goto cleanup;
}
 
cleanup:
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (schService)
    CloseServiceHandle(schService);
DsFreeSpnArray(ulSpn, pspn);
return;
}
```



Para obtener más información sobre el ejemplo de código anterior, vea Crear los [SPN](composing-the-spns-for-a-service-with-an-scp.md) para un servicio con un SCP y Registrar los [SPN para un servicio](registering-the-spns-for-a-service.md).

 

 