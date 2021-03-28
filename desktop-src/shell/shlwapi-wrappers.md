---
description: Las tablas de este documento enumeran las funciones de contenedor desde Shlwapi.dll que proporcionan una funcionalidad de Unicode limitada a Windows 95, Windows 98 y Windows Millennium Edition (Windows me).
title: Funciones de encapsulador SHLWAPI
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3c428c89-b650-48c1-9f91-b94f9f8e10e2
api_name:
- SHLWAPI Wrapper Functions
- AppendMenuWrapW
- CallWindowProcWrapW
- CharLowerWrapW
- CharUpperBufWrapW
- CharUpperWrapW
- CompareStringWrapW
- CopyFileWrapW
- CreateEventWrapW
- CreateFileWrapW
- CreateWindowExWrapW
- DefWindowProcWrapW
- DeleteFileWrapW
- DialogBoxParamWrapW
- DispatchMessageWrapW
- DragQueryFileWrapW
- DrawTextExWrapW
- DrawTextWrapW
- ExtTextOutWrapW
- FormatMessageWrapW
- GetClassInfoWrapW
- GetDateFormatW
- GetDateFormatWrapW
- GetDlgItemTextWrapW
- GetFileAttributesWrapW
- GetLocaleInfoWrapW
- GetMenuItemInfoWrapW
- GetModuleFileNameWrapW
- GetModuleHandleWrapW
- GetObjectWrapW
- GetOpenFileNameWrapW
- GetSaveFileNameWrapW
- GetSystemDirectoryWrapW
- GetTimeFormatWrapW
- GetWindowLongWrapW
- GetWindowsDirectoryWrapW
- GetWindowTextLengthWrapW
- GetWindowTextWrapW
- InsertMenuItemWrapW
- IsCharAlphaNumericWrapW
- IsCharAlphaWrapW
- IsCharUpperWrapW
- LoadLibraryWrapW
- LoadStringWrapW
- MessageBoxWrapW
- MLGetUILanguage
- MoveFileWrapW
- OutputDebugStringWrapW
- PeekMessageWrapW
- PostMessageWrapW
- RegCreateKeyExWrapW
- RegisterClassWrapW
- RegOpenKeyExWrapW
- RegQueryValueExW
- RegQueryValueExWrapW
- RegQueryValueWrapW
- RegSetValueExWrapW
- SendMessageWrapW
- SetDlgItemTextWrapW
- SetWindowLongWrapW
- SetWindowTextWrapW
- SHCancelTimerQueueTimer
- SHDeleteTimerQueue
- ShellExecuteExWrapW
- ShellMessageBoxWrapW
- SHGetFileInfoWrapW
- SHGetPathFromIDListWrapW
- SHInterlockedCompareExchange
- SHQueueUserWorkItem
- SHSetTimerQueueTimer
- TranslateAcceleratorWrapW
- UnregisterClassWrapW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 52e3a5b60a331a74ced1888d5a196348497c5ff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815315"
---
# <a name="shlwapi-wrapper-functions"></a>Funciones de encapsulador SHLWAPI

\[Estas funciones están disponibles a través de Windows XP Service Pack 2 (SP2) y Windows Server 2003. Podrían modificarse o no estar disponibles en versiones posteriores de Windows.\]

Las tablas de este documento enumeran las funciones de contenedor desde Shlwapi.dll que proporcionan una funcionalidad de Unicode limitada a Windows 95, Windows 98 y Windows Millennium Edition (Windows me).

Windows 95, Windows 98 y Windows Millennium Edition (Windows me) se conocen aquí como "plataformas ANSI nativas". En las plataformas ANSI nativas, estas funciones contenedoras convierten los parámetros de cadena de entrada Unicode a ANSI y llaman a versiones ANSI de funciones de la columna reenviar **a** . Por ejemplo, **AppendMenuWrapW** llama a **AppendMenuA**, que es la versión ANSI de [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Las demás funciones siguen el mismo patrón. Las cadenas devueltas por la función ANSI se convierten a Unicode y se devuelven a la aplicación que realiza la llamada. Aparte de las excepciones indicadas en la columna **comentarios** , la función contenedora tiene la misma sintaxis y proporciona la misma funcionalidad que la función de la columna reenviar **a** . Debe hacer referencia a esa página de referencia para obtener información detallada sobre el uso.

**Advertencia de seguridad:** Varias cadenas Unicode se pueden convertir en la misma cadena ANSI. Colisiones inesperadas después de la conversión podrían provocar un comportamiento inesperado. Por ejemplo, si se usa **CreateEventWrapW** para crear dos eventos con un nombre diferente cuyos nombres coincidan después de la conversión de Unicode a ANSI, la segunda llamada devolverá un identificador al mismo evento que la primera llamada, aunque las cadenas Unicode originales eran diferentes.

Los sistemas operativos Microsoft Windows NT, Windows 2000, Windows XP, Windows Server 2003 y versiones posteriores se conocen aquí como "plataformas Unicode nativas". En su mayor parte, en las plataformas Unicode nativas, estas funciones contenedoras simplemente reenvían los parámetros de la cadena de entrada a la versión Unicode de la función en la columna reenviar **a** . Por ejemplo, **AppendMenuWrapW** reenvía a **AppendMenuW**, que es la versión Unicode de [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Las demás funciones siguen el mismo patrón. Cualquier cadena devuelta por la función Unicode se devuelve a la aplicación que realiza la llamada. Aparte de las excepciones indicadas en la columna **comentarios** , la función contenedora tiene la misma sintaxis y proporciona la misma funcionalidad que la función de la columna reenviar **a** . Debe hacer referencia a esa página de referencia para obtener información detallada sobre el uso.

**Advertencia de seguridad:** Los problemas de seguridad indicados para las funciones de la columna reenviar **a** también se aplican a las funciones de contenedor correspondientes. Para obtener más información, consulte la documentación de referencia de la función en la columna reenviar **a** .

Las funciones contenedoras de esta tabla están contenidas en Shlwapi.dll. Para llamarlos, debe utilizar el ordinal mostrado en la tabla.

> [!Note]  
> Estas funciones de contenedor están disponibles en Windows XP, pero no proporcionan ninguna funcionalidad de contenedor en Windows XP Service Pack 2 (SP2) y versiones posteriores. Tampoco proporcionan funcionalidad de contenedor en Windows Server 2003. En su lugar, debe usar las funciones enumeradas en la columna reenviar **a** .

 



| Función                  | Ordinal | Se reenvía a                                             | Archivo DLL      | Observaciones                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| AppendMenuWrapW           | 36      | [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(menú)](#menu)                                                           |
| CallWindowProcWrapW       | 37      | [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | USER32   | [Configur](#shlwapi-wrapper-functions)                                                                                                   |
| CharLowerWrapW            | 38      | [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | KERNEL32 | [e:.](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperBufWrapW         | 44      | [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | KERNEL32 | [e:.](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperWrapW            | 43      | [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | KERNEL32 | [e:.](#shlwapi-wrapper-functions)                                                                                                   |
| CompareStringWrapW        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | KERNEL32 | [API](#comparestring)                                                                                                   |
| CopyFileWrapW             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateEventWrapW          | 51      | [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | KERNEL32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| CreateFileWrapW           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateWindowExWrapW       | 55      | [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| DefWindowProcWrapW        | 56      | [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | USER32   | [Configur](#shlwapi-wrapper-functions)                                                                                                   |
| DeleteFileWrapW           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| DialogBoxParamWrapW       | 59      | [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | USER32   | [(f)](#dragqueryfile), [(i)](#shlwapi-wrapper-functions), [(DialogBoxParam)](#dialogboxparam)                                       |
| DispatchMessageWrapW      | 60      | [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | USER32   | [Configur](#shlwapi-wrapper-functions)                                                                                                   |
| DragQueryFileWrapW        | 318     | [**DragQueryFile**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | SHELL32  | [(b)](#dialogboxparam), [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DragQueryFile)](#dragqueryfile)               |
| DrawTextExWrapW           | 301     | [**DrawTextEx**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | USER32   | [(a)](#shlwapi-wrapper-functions), [(d)](#shlwapi-wrapper-functions)                                                                |
| DrawTextWrapW             | 61      | [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| ExtTextOutWrapW           | 299     | [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [(d)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(ExtTextOut)](#exttextout)                                               |
| FormatMessageWrapW        | 68      | [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(FormatMessage)](#formatmessage)                                       |
| GetClassInfoWrapW         | 69      | [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | USER32   | [GetClassInfo](#getclassinfo)                                                                                                     |
| GetDateFormatWrapW        | 311     | [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetDlgItemTextWrapW       | 74      | [**GetDlgItemText**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | USER32   | [i](#compareexchange)                                                                                                             |
| GetFileAttributesWrapW    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| GetLocaleInfoWrapW        | 77      | [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | KERNEL32 | [i](#compareexchange)                                                                                                             |
| GetMenuItemInfoWrapW      | 302     | [**GetMenuItemInfo**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange), [(MenuItemInfo)](#menuiteminfo)                                                     |
| GetModuleFileNameWrapW    | 80      | [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetModuleHandleWrapW      | 83      | [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetObjectWrapW            | 84      | [**GetObject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [i](#compareexchange)                                                                                                             |
| GetOpenFileNameWrapW      | 403     | [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OPENFILENAME)](#openfilename)                 |
| GetSaveFileNameWrapW      | 389     | [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OPENFILENAME)](#openfilename)                 |
| GetSystemDirectoryWrapW   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetTimeFormatWrapW        | 310     | [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetWindowLongWrapW        | 94      | [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| GetWindowsDirectoryWrapW  | 97      | [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetWindowTextLengthWrapW  | 96      | [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | USER32   | [j](#j)                                                                                                                           |
| GetWindowTextWrapW        | 95      | [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange)                                                                                      |
| InsertMenuItemWrapW       | 98      | [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(menú)](#menu), [(MenuItemInfo)](#menuiteminfo)                          |
| IsCharAlphaWrapW          | 25      | [**IsCharAlpha**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | USER32   | [e:.](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharAlphaNumericWrapW   | 28      | [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | KERNEL32 | [e:.](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharUpperWrapW          | 26      | [**IsCharUpper**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | USER32   | [e:.](#shlwapi-wrapper-functions)                                                                                                   |
| LoadLibraryWrapW          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| LoadStringWrapW           | 107     | [**Fall**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | KERNEL32 | [e:.](#shlwapi-wrapper-functions)                                                                                                   |
| MessageBoxWrapW           | 340     | [**Cuadro de mensajes**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| MoveFileWrapW             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| OutputDebugStringWrapW    | 115     | [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | KERNEL32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| PeekMessageWrapW          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | USER32   | [(PeekMessage y PostMessage)](#peekmessage-and-postmessage)                                                                       |
| PostMessageWrapW          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | USER32   | [(PeekMessage y PostMessage)](#peekmessage-and-postmessage)                                                                       |
| RegCreateKeyExWrapW       | 120     | [**RegCreateKeyEx**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | ADVAPI32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| RegisterClassWrapW        | 131     | [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | USER32   | [(a)](#shlwapi-wrapper-functions), [(RegisterClass)](#registerclass)                                                                |
| RegOpenKeyExWrapW         | 125     | [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | ADVAPI32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| RegQueryValueExWrapW      | 128     | [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(ValueEx)](#regqueryvalueexw), [(RegQueryValueExW)](#regqueryvalueexw) |
| RegQueryValueWrapW        | 127     | [**RegQueryValue**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| RegSetValueExWrapW        | 130     | [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(ValueEx)](#regqueryvalueexw)                                                                   |
| SendMessageWrapW          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | USER32   | [SendMessage](#sendmessage)                                                                                                       |
| SetDlgItemTextWrapW       | 138     | [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| SetWindowLongWrapW        | 141     | [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| SetWindowTextWrapW        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| ShellExecuteExWrapW       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(ShellExecuteEx)](#shellexecuteex)                                      |
| ShellMessageBoxWrapW      | 388     | [**ShellMessageBox**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | SHLWAPI  | [(a)](#shlwapi-wrapper-functions), [(FormatMessage)](#formatmessage)                                                                |
| SHGetFileInfoWrapW        | 313     | [**SHGetFileInfo**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange)                                                  |
| SHGetPathFromIDListWrapW  | 334     | [**SHGetPathFromIDList**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | USER32   | [i](#compareexchange)                                                                                                             |
| TranslateAcceleratorWrapW | 146     | [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | USER32   | [Configur](#shlwapi-wrapper-functions)                                                                                                   |
| UnregisterClassWrapW      | 147     | [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |



 

Las funciones de contenedor de la tabla siguiente no realizan ninguna conversión de juego de caracteres. En su lugar, proporcionan compatibilidad limitada para las características del sistema operativo que no están disponibles en plataformas anteriores.



| Función                     | Ordinal | Se reenvía a                                                                     | Archivo DLL      | Observaciones                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| MLGetUILanguage              | 376     | [**GetUserDefaultUILanguage**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | KERNEL32 | [c](#shlwapi-wrapper-functions)                                              |
| SHCancelTimerQueueTimer      | 265     | [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | KERNEL32 | [c](#shlwapi-wrapper-functions)                                              |
| SHDeleteTimerQueue           | 262     | [**DeleteTimerQueue**](/windows/win32/api/winbase/nf-winbase-deletetimerqueue)                                   | KERNEL32 | [c](#shlwapi-wrapper-functions)                                              |
| SHInterlockedCompareExchange | 342     | [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | KERNEL32 | [CompareExchange](#compareexchange)                                          |
| SHQueueUserWorkItem          | 260     | [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | KERNEL32 | [(QueueUserWorkItem)](#queueuserworkitem), [(h)](#shlwapi-wrapper-functions)   |
| SHSetTimerQueueTimer         | 263     | [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | KERNEL32 | [(SetTimerQueueTimer)](#settimerqueuetimer), [(h)](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>Observaciones

### <a name="a"></a>un

Si es necesaria la conversión de cadenas, todas las cadenas se convierten a través de la \_ Página de códigos CP ACP.

Estas funciones emplean caracteres con ajuste perfecto y no realizan la comprobación predeterminada al convertir de Unicode a ANSI. Además, si la cadena no se puede convertir de Unicode a ANSI, la función contenedora pasa una cadena **null** a la función ANSI subyacente. Esto puede ocurrir, por ejemplo, cuando no hay suficiente memoria. Si se pasa una cadena **null** , es posible que se produzcan errores en algunas funciones con un parámetro no válido, pero otras funciones aceptan la cadena **null** y la tratan como parámetro previsto. Por ejemplo, se produce un error cuando la función **CreateWindowExWrapW** intenta convertir el parámetro *lpWindowName* en ANSI y [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crea una ventana con un título vacío. El contenedor no le avisa cuando se han producido estos problemas.

En la capa de Microsoft para Unicode (MSLU) se comprueban los errores durante la conversión de Unicode a ANSI y se devuelven los valores de error correspondientes. Por ejemplo, la función contenedora [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) de MSLU devuelve 0 si el elemento no se ha anexado correctamente.

### <a name="b"></a>b

Estas funciones usan un vínculo de carga retrasada a la función adecuada. Esto significa que el archivo DLL que contiene la función de la columna "reenviar a" no lo carga el Shlwapi.dll hasta que se llama a una función de ese archivo DLL. El enlazador Microsoft Visual C++ admite esta funcionalidad de forma más general a través de la opción/DELAYLOAD.

### <a name="c"></a>unidad

Esta función manipula los nombres de archivo. Como se indicó en [(a)](#shlwapi-wrapper-functions), las funciones convierten todas las cadenas a través de la \_ Página de códigos CP ACP. No comprueban si las funciones de e/s de archivo se han establecido en modo ANSI. Si las funciones de e/s de archivo están en modo OEM, las cadenas se convertirán en y desde el juego de caracteres equivocado. Una aplicación puede establecer las funciones de e/s de archivo en modo OEM explícitamente llamando a la función [**SetFileApisToOEM**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem) .

* * ADVERTENCIA de seguridad: * * el uso de estas funciones de contenedor para los nombres de archivo puede poner en peligro la seguridad de la aplicación. Dado que no se realiza ninguna comprobación predeterminada y se emplean los caracteres con ajuste perfecto, los caracteres de nombre de archivo se pueden convertir de maneras inesperadas. Esto podría provocar ataques de suplantación de identidad del sistema de archivos. Además, se puede producir una pérdida de datos silenciosa durante la conversión de Unicode a ANSI.

MSLU no tiene estas limitaciones.

### <a name="d"></a>d

Si la cadena que se va a dibujar requiere un juego de caracteres que no está disponible en la fuente seleccionada en el contexto del dispositivo, estas funciones de contenedor usan la característica de [vinculación de fuentes](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85)) de la biblioteca [MLang](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85)) para representar cada carácter en una fuente adecuada. A diferencia de la mayoría de las demás funciones de contenedor, son funcionales en Microsoft Windows NT 4,0, además de en las plataformas ANSI nativas.

### <a name="e"></a>e:.

Las implementaciones completas de Unicode de estas funciones están disponibles en las plataformas ANSI nativas. Estas funciones no llaman a la función ANSI relacionada.

### <a name="f"></a>formato

Si el idioma predeterminado de la interfaz de usuario usa un juego de caracteres diferente del idioma de la interfaz de usuario predeterminada del sistema, el sistema intenta volver a escribir plantillas de cuadro de diálogo y controles de subclases y convertir los elementos de menú en dibujado por el propietario, de modo que las cadenas del idioma de la interfaz de usuario predeterminada del usuario sigan apareciendo correctamente. Los únicos controles que admiten las reglas de reescritura de plantilla de cuadro de diálogo son los controles estáticos, de botón, de cuadro de lista y de cuadro combinado. Estos controles se subclasen de forma que la función **SendMessageWrapW** puede obtener la cadena Unicode original sin que se traduzca a través del juego de caracteres ANSI. A diferencia de la mayoría de las demás funciones de contenedor, son funcionales en Microsoft Windows NT 4,0 y en las plataformas ANSI nativas. Vea los comentarios en la documentación de la función [**MLLoadLibrary**](./callbacks.md) para obtener más información sobre cómo se determinan el idioma predeterminado de la interfaz de usuario y el idioma predeterminado del sistema.

### <a name="g"></a>i

Si es necesaria la conversión de cadenas, todas las cadenas se convierten a través de la \_ Página de códigos CP ACP.

Al convertir de ANSI a Unicode para la salida, si la cadena devuelta no cabe en el búfer proporcionado, las funciones de contenedor truncan la cadena. Las funciones que devuelven el número de caracteres que se copian en el búfer o el número de caracteres necesarios para evitar el truncamiento no devuelven el número de caracteres Unicode que se copian en el búfer proporcionado por o que son necesarios desde el autor de la llamada de la función de contenedor. Devuelven el número de caracteres ANSI copiados en el búfer o que requiere la función ANSI subyacente. MSLU no tiene estas limitaciones.

### <a name="h"></a>c

En sistemas anteriores a Windows XP, estas funciones implementan un grupo de subprocesos y una cola de temporizador simplificados. En Windows XP y versiones posteriores, estas funciones usan el grupo de subprocesos del sistema y la cola del temporizador del sistema. En el caso de las funciones de cola de temporizador, el parámetro *hQueue* debe establecerse en **null** para indicar que la operación se va a realizar en la cola del temporizador predeterminada.

### <a name="i"></a>Configur

En las plataformas Unicode, estas funciones traducen el mensaje de Unicode a ANSI si la ventana de destino es ANSI. Estas funciones no realizan la traducción de mensajes en las plataformas ANSI nativas. Por lo tanto, llamar a las aplicaciones que llaman a esta función debe asegurarse de que el mensaje está en formato Unicode en plataformas Unicode y en formato ANSI en plataformas ANSI. Por ejemplo, en la siguiente llamada de función, *wParam* debe ser un punto de código Unicode si el programa se está ejecutando en una plataforma Unicode y debe ser un carácter ANSI si el programa se ejecuta en una plataforma ANSI.

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

MSLU realiza un seguimiento del juego de caracteres del procedimiento de ventana de destino y convierte el mensaje según sea necesario.

### <a name="j"></a>j

En las plataformas ANSI, estas funciones devuelven la longitud de la cadena ANSI subyacente, no la longitud de la cadena Unicode traducida. MSLU no tiene estas limitaciones.

### <a name="compareexchange"></a>CompareExchange

La sintaxis de **SHInterlockedCompareExchange** es algo diferente de la de [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer), pero funciona de forma idéntica.

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a>API

Recuerde que en las plataformas ANSI nativas, ambas cadenas se convierten en ANSI y se comparan como cadenas ANSI. Si las cadenas Unicode contienen caracteres que no se pueden representar en ANSI, los resultados pueden ser inesperados. Por ejemplo, si la página de códigos ANSI predeterminada no es compatible con caracteres CJK, las cadenas L " \\ x66F0" y l " \\ x6708" se compararían como iguales en las plataformas ANSI nativas porque ambos se asignan a la cadena ANSI "?".

### <a name="datetime"></a>DateTime

En Shlwapi.dll versión 5,0, que se incluye con Windows 2000, la página de códigos del identificador de configuración regional que se pasa como primer parámetro de **GetDateFormatWrapW** y **GetTimeFormatWrapW** debe coincidir con la página de códigos ANSI actual. De lo contrario, la cadena devuelta se puede convertir incorrectamente. Esta limitación no se aplica a Shlwapi.dll versiones 5,5 o posteriores. Esto significa que los sistemas Windows XP y versiones posteriores no están sujetos a esta limitación. La MSLU no tiene esta limitación.

### <a name="dialogboxparam"></a>(DialogBoxParam)

El parámetro *lpTemplateName* para la función **DialogBoxParamWrapW** no puede ser una cadena. Debe ser un ordinal creado por la macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . El procedimiento de cuadro de diálogo especificado por el parámetro *lpDialogFunc* recibe mensajes ANSI en plataformas ANSI nativas y mensajes Unicode en plataformas Unicode nativas. El procedimiento del cuadro de diálogo debe estar preparado para controlar ambos casos. MSLU no tiene estas limitaciones.

### <a name="exttextout"></a>(ExtTextOut)

Las plataformas ANSI nativas implementan la función [**ExtTextOutW**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) y las plataformas Unicode nativas. El propósito de **ExtTextOutWrapW** es realizar la vinculación de fuentes, como se describe en un comentario independiente.

### <a name="dragqueryfile"></a>(DragQueryFile)

La función **DragQueryFileWrapW** no permite consultar la longitud de un archivo en el controlador de colocación pasando **null** como el parámetro *lpszFile* . MSLU no tiene estas limitaciones.

### <a name="formatmessage"></a>FormatMessage

En las plataformas ANSI nativas, los formatos de la cadena no se convierten de Unicode a ANSI. Por ejemplo, el siguiente ejemplo de código es erróneo.


```
WCHAR szBuffer[MAX_PATH];
DWORD_PTR Arguments[2] = { L"String1", L"String2" };

FormatMessageWrapW(FORMAT_MESSAGE_FROM_STRING, 
               L"%1!s! %2", 
               0, 0, 
               szBuffer, 
               MAX_PATH, 
               (va_list*)Arguments);
```



En este ejemplo de código se usa "! s!" expresa como formato HH:MM:SS… En las plataformas ANSI nativas, esta cadena se pasa a la versión ANSI de la función [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) . Por consiguiente, se espera una cadena ANSI en lugar de una cadena Unicode. Del mismo modo, el formato "%2" implica un argumento de cadena. Cuando se pasa a la función **FormatMessage** de ANSI, se interpreta como una cadena ANSI en lugar de una cadena Unicode. La cadena de formato correcta es L "%1! ws! %2! WS! ". Esto imprime las cadenas correctamente en las plataformas ANSI y Unicode.

La función no admite "%0" cadena de formato especial.

MSLU no tiene estas limitaciones.

### <a name="getclassinfo"></a>GetClassInfo

En las plataformas ANSI nativas, los miembros **lpszMenuName** y **lpszClassName** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) no se traducen a Unicode y siempre se establecen en **null**. Además, el procedimiento de ventana devuelto en el miembro **lpfnWndProc** de la estructura **WNDCLASS** no se traduce a Unicode y hace referencia a un procedimiento de ventana ANSI. MSLU no tiene estas limitaciones.

### <a name="menu"></a>MENU

En Shlwapi.dll versión 5,0, que se incluye con Windows 2000, es posible que las cadenas de elementos de menú que contengan caracteres de tabulación ( \\ t) no se muestren correctamente. Esta limitación no se aplica a Shlwapi.dll versiones 5,5 o posteriores. Esto significa que los sistemas Windows XP y versiones posteriores no están sujetos a esta limitación. La MSLU no tiene esta limitación.

### <a name="menuiteminfo"></a>(MenuItemInfo)

Esta función solo admite la versión Microsoft Windows NT 4,0 de la estructura [**MENUITEMINFOW**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Esta estructura carece de un miembro **hbmpItem** . Además, la función no admite la \_ marca de mapa de bits Miim. MSLU no tiene estas limitaciones.

### <a name="openfilename"></a>OPENFILENAME

El miembro **cbSize** de la estructura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) debe establecerse en sizeof (OPENFILENAME \_ NT4W).

El miembro **lpstrCustomFilter** de la estructura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) debe establecerse en **null**.

Los valores de los miembros **nMaxFile** y **nMaxFileTitle** de la estructura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) no deben superar la \_ ruta de acceso máxima.

Si el miembro **lpfnHook** de la estructura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) no es **null**, debe hacer referencia a un procedimiento de enlace ANSI en plataformas ANSI nativas y un procedimiento de enlace Unicode en plataformas Unicode nativas.

MSLU no tiene estas limitaciones.

### <a name="peekmessage-and-postmessage"></a>(PeekMessage y PostMessage)

En las plataformas ANSI nativas, no se realiza ninguna traducción en el mensaje transmitido o recuperado. El mensaje transmitido/recuperado es ANSI en plataformas ANSI nativas y Unicode en plataformas Unicode nativas. La aplicación que realiza la llamada debe estar preparada para controlar ambos casos. Por ejemplo, si el mensaje recuperado es WM \_ Char, el *wParam* es un código de carácter ANSI en plataformas ANSI nativas, pero es un punto de código Unicode en plataformas Unicode nativas. MSLU no tiene estas limitaciones.

### <a name="queueuserworkitem"></a>QueueUserWorkItem

La función **SHQueueUserWorkItem** es ligeramente diferente de la función [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) correspondiente. Aquí se muestra la sintaxis de **SHQueueUserWorkItem** .

``` syntax
BOOL SHQueueUserWorkItem(LPTHREAD_START_ROUTINE pfnCallback,
                     LPVOID pContext,
                     LONG lPriority,
                     DWORD_PTR dwTag,
                     DWORD_PTR * pdwId,
                     LPCSTR pszModule,
                     DWORD dwFlags);
```

Los parámetros deben establecerse de la siguiente manera:

-   Los parámetros *pfnCallback* y *pContext* tienen los mismos significados que la *función* y los parámetros de *contexto* , respectivamente, de [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem).
-   El parámetro *dwTag* no se utiliza y debe establecerse en 0.
-   El parámetro *pdwld* no se utiliza y debe establecerse en **null**.
-   El parámetro *pszModule* apunta a una cadena ANSI opcional terminada en null que especifica el nombre de una biblioteca que se va a cargar antes de que el elemento de trabajo se inicie y descargue una vez completado el elemento de trabajo. Este parámetro puede ser **NULL**.
-   El parámetro *dwFlags* solo admite un subconjunto de los valores admitidos por [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem). Se reconocen las marcas siguientes.

    

    | Nombre              | Value      | Significado                          |
    |-------------------|------------|----------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | Igual que WT \_ EXECUTEINIOTHREAD.   |
    | TPS \_ LONGEXECTIME | 0x00000008 | Igual que WT \_ EXECUTELONGFUNCTION. |

    

     

    > [!Note]  
    > La \_ marca TPS LONGEXECTIME no tiene el mismo valor numérico que la marca WT \_ EXECUTELONGFUNCTION. Al utilizar **SHQueueUserWorkItem**, el parámetro dwFlags debe ser una combinación de valores de TPS \_ \* , no de \_ \* los valores de wt.

     

**SHQueueUserWorkItem** devuelve un valor distinto de cero si el elemento de trabajo se puso en cola correctamente y 0 en caso contrario. Si se produce un error en la función, puede usar [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener información adicional.

### <a name="registerclass"></a>RegisterClass

En las plataformas ANSI nativas, no se realiza ninguna traducción en el miembro **lpfnWndProc** de la estructura [**WNDCLASSW**](/windows/win32/api/winuser/ns-winuser-wndclassa) . La ventana recibirá mensajes de ventana ANSI en plataformas ANSI nativas y mensajes de ventana Unicode en plataformas Unicode nativas. El procedimiento de ventana debe estar preparado para controlar ambos casos. MSLU no tiene estas limitaciones.

### <a name="regqueryvalueexw"></a>(RegQueryValueExW)

También se ha llamado a **RegQueryValueExWrapW** con el nombre **RegQueryValueExW**. Como con cualquier función sin nombre exportada estrictamente por ordinal, puede elegir el nombre que la función conoce en el código.

### <a name="sendmessage"></a>SendMessage

En las plataformas Unicode nativas, la función **SendMessageWrapW** reenvía a la función [**SendMessageW**](/windows/win32/api/winuser/nf-winuser-sendmessage) . En las plataformas ANSI nativas, **SendMessageWrapW** proporciona compatibilidad limitada para traducir mensajes Unicode a ANSI. La lista de mensajes admitidos se proporciona en la tabla siguiente. La función no traducirá ningún otro mensaje.

MSLU no tiene estas limitaciones.



|                      |                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| CB \_ ADDSTRING        | (b) (f) (c)                                                                                               |
| CB \_ FINDSTRING       | (b) (f) (c)                                                                                               |
| CB \_ FindExactString con  | (a) (f) (c)                                                                                               |
| CB \_ GETLBTEXT        | (b) (f) (c) (o) el búfer pasado en el parámetro *lParam* debe tener espacio para al menos 256 caracteres.   |
| CB \_ GETLBTEXTLEN     | un                                                                                                       |
| CB \_ INSERTSTRING     | (b) (f) (c)                                                                                               |
| CB \_ SELECTSTRING     | (b) (f) (c)                                                                                               |
| \_CHARFROMPOS em      |                                                                                                           |
| \_GETLINE em          | (e) el valor devuelto es el número de caracteres ANSI copiados.                                             |
| \_GETSEL em           |                                                                                                           |
| \_REPLACESEL em       | (b) (f)                                                                                                   |
| \_SETPASSWORDCHAR em  | un                                                                                                       |
| \_SETSEL em           |                                                                                                           |
| \_SETWORDBREAKPROC em | Este mensaje no tiene ningún efecto. No se ha establecido el procedimiento de separación de palabras.                                          |
| LB \_ ADDSTRING        | (b) (f) (d)                                                                                               |
| LB \_ FINDSTRING       | (b) (f) (d)                                                                                               |
| LB \_ FindExactString con  | (b) (f) (libras)                                                                                             |
| \_apgettext GETTEXT          | (b) (f) (lbs) (o) el búfer pasado en el parámetro *lParam* debe tener espacio para al menos 256 caracteres. |
| LB \_ GETTEXTLEN       | un                                                                                                       |
| LB \_ INSERTSTRING     | (b) (f) (d)                                                                                               |
| LB \_ SELECTSTRING     | (b) (f) (d)                                                                                               |
| GETTEXT de WM \_          | (b) (f)                                                                                                   |
| GETTEXTLENGTH de WM \_    | un                                                                                                       |
| SETTEXT de WM \_          | (b) (f)                                                                                                   |
| SETTINGCHANGE de WM \_    | (a) el mensaje se envía con un tiempo de espera de tres segundos.                                                  |



 


-   (a) la cadena ANSI que se mide o se recupera debe cumplir la siguiente condición: la longitud de la versión Unicode correspondiente de la cadena no puede superar la longitud de la versión ANSI de la cadena. Si no se cumple esta condición, la longitud devuelta será breve. Si no hay memoria suficiente para determinar la longitud de la cadena Unicode, la función devuelve cero, no LB \_ Err o CB \_ Err como cabría esperar.
-   (b) si es necesaria la conversión de cadenas, todas las cadenas se convierten a través de la \_ Página de códigos CP ACP.

    Esta función emplea caracteres con ajuste perfecto y no realiza la comprobación predeterminada al convertir de Unicode a ANSI. Además, si la cadena no se puede convertir de Unicode a ANSI, la función pasa una cadena null a la función ANSI subyacente. Esto puede ocurrir, por ejemplo, cuando no hay suficiente memoria. Si se pasa una cadena null, es posible que se produzcan errores en algunas funciones con un parámetro no válido, pero otras funciones aceptan la cadena NULL y la tratan como parámetro previsto. Por ejemplo, si se produce un error cuando el \_ contenedor de WM SETTEXT intenta convertir el título de la ventana en ANSI, la ventana tendrá un título vacío. La función no le avisa cuando se producen estos problemas. MSLU no tiene estas limitaciones.

-   (c) el identificador de ventana especificado debe ser el identificador de un control [ComboBox](../controls/combo-boxes.md) o [ComboBoxEx](../controls/comboboxex-controls.md) . Si el identificador es un control ComboBox que está dibujado por el propietario y no se ha creado con el estilo de [estilos de cuadro de lista](../controls/list-box-styles.md) , la traducción de este mensaje producirá un error y puede incluso bloquearse.
-   (d) el identificador de ventana especificado debe ser el identificador de un control ListBox. Si el control ListBox está dibujado por el propietario y no se ha creado con el estilo de [estilos de cuadro de lista](../controls/list-box-styles.md) , se producirá un error en la traducción de este mensaje y puede incluso bloquearse.
-   (e) si es necesaria la conversión de cadenas, todas las cadenas se convierten a través de la \_ Página de códigos CP ACP.

    Al convertir de ANSI a Unicode para la salida, las funciones de contenedor truncan la cadena devuelta si no cabe en el búfer proporcionado. El valor devuelto para las funciones que devuelven el número de caracteres copiados en el búfer o el número de caracteres necesarios para evitar el truncamiento se refiere al número de caracteres ANSI copiados en el búfer o que requiere la función ANSI subyacente, no el número de caracteres Unicode copiados en el búfer proporcionado por o que son necesarios desde la aplicación que llama. La MSLU no tiene esta limitación. Para obtener más información, consulte la [capa de Microsoft para Unicode en sistemas Windows 95/98/me](/previous-versions/ms812865(v=msdn.10)).

### <a name="settimerqueuetimer"></a>(SetTimerQueueTimer)

La función **SHSetTimerQueueTimer** es ligeramente diferente de la función [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) correspondiente. Su sintaxis es la siguiente:

``` syntax
HANDLE SHSetTimerQueueTimer(HANDLE hQueue,
                        WAITORTIMERCALLBACK pfnCallback,
                        LPVOID pContext,
                        DWORD dwDueTime,
                        DWORD dwPeriod,
                        LPCSTR lpszLibrary,
                        DWORD dwFlags);
```

Los parámetros deben establecerse de la siguiente manera:

-   El parámetro *hQueue* debe establecerse en **null**, especificando la cola de temporizador predeterminada.
-   Los *parámetros pfnCallback*, *pContext*, *dwDueTime* y *dwPeriod* tienen los mismos significados que los parámetros *callback*, *Parameter*, *DueTime* y *period* , respectivamente, de [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).
-   El parámetro *lpszLibrary* no se utiliza y debe establecerse en **null**.
-   El parámetro *Flags* solo admite un subconjunto de los valores admitidos por [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).

    

    | Nombre              | Value      | Significado                         |
    |-------------------|------------|---------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | Igual que WT \_ EXECUTEINIOTHREAD   |
    | TPS \_ LONGEXECTIME | 0x00000008 | Igual que WT \_ EXECUTELONGFUNCTION |

    

     

    > [!Note]  
    > La \_ marca TPS LONGEXECTIME no tiene el mismo valor numérico que la marca WT \_ EXECUTELONGFUNCTION. Al utilizar **SHSetTimerQueueTimer**, el parámetro *dwFlags* debe ser una combinación de valores de TPS \_ \* , no de \_ \* los valores de wt.

     

**SHSetTimerQueueTimer** devuelve el identificador del temporizador creado si se realiza correctamente y **null** en caso contrario.

### <a name="shellexecuteex"></a>ShellExecuteEx

El miembro **lpFile** de la estructura [**SHELLEXECUTEINFO**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa) pasada en el único parámetro de esta función no puede superar los caracteres de \_ longitud máxima de \_ dirección URL de Internet \_ . Si \_ \_ se omite la marca de className de Mask, se debe inicializar el miembro **lpClass** en **null**.

### <a name="valueex"></a>(ValueEx)

Solo se admiten los siguientes tipos de datos del registro: REG \_ SZ, REG \_ Expand \_ , REG \_ y reg \_ DWORD. A diferencia de estas funciones de contenedor, MSLU también admite REG \_ multi \_ Expand \_ .

### <a name="windowlong"></a>(WindowLong)

En las plataformas ANSI nativas, la función no realiza ninguna conversión en ninguno de los periodos de tiempo de la ventana. Por ejemplo, si se pasa GWLP \_ WndProc, la función devuelve el procedimiento de ventana ANSI, no un código thunk. MSLU no tiene estas limitaciones.

 

 
