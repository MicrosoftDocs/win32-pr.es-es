---
description: En el ejemplo siguiente se reinicia el sistema local mediante la función InitiateSystemShutdown.
ms.assetid: 928c2d48-daa5-4c27-816b-766adedba7eb
title: Mostrar el cuadro de diálogo de apagado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedfee9e96fa1e6183cbe1d9322a603b65ae4b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667182"
---
# <a name="displaying-the-shutdown-dialog-box"></a>Mostrar el cuadro de diálogo de apagado

En el ejemplo siguiente se reinicia el sistema local mediante la función [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) . El sistema muestra un cuadro de diálogo con un mensaje personalizado y un mensaje al usuario para cerrar las aplicaciones en el intervalo de tiempo de espera especificado (30 segundos). Una vez transcurrido el intervalo de tiempo de espera, se reinicia el sistema.

La aplicación debe habilitar el privilegio de nombre de cierre de SE \_ antes de \_ llamar a [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna). Para obtener más información, vea [privilegios](../secauthz/privileges.md).


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL MySystemShutdown( LPTSTR lpMsg )
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   BOOL fResult;               // system shutdown flag 
 
   // Get the current process token handle so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
      (PTOKEN_PRIVILEGES) NULL, 0); 
 
   // Cannot test the return value of AdjustTokenPrivileges. 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Display the shutdown dialog box and start the countdown. 
 
   fResult = InitiateSystemShutdown( 
      NULL,    // shut down local computer 
      lpMsg,   // message for user
      30,      // time-out period, in seconds 
      FALSE,   // ask user to close apps 
      TRUE);   // reboot after shutdown 
 
   if (!fResult) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE; 
}
```



Si la función [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) se ejecuta en el período de tiempo de espera especificado por [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), el sistema no se apaga. Por ejemplo, si se llama a PreventSystemShutdown después de MySystemShutdown, el sistema cierra el cuadro de diálogo y no reinicia el sistema.


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL PreventSystemShutdown()
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   // Get the current process token handle  so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
         TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
         &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Prevent the system from shutting down. 
 
   if ( !AbortSystemShutdown(NULL) ) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
       (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE;
}
```



 

 
