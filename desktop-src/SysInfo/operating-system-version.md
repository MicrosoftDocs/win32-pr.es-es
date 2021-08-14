---
description: Las funciones auxiliares de api de versión se usan para determinar la versión del sistema operativo que se está ejecutando actualmente. Para obtener más información, vea Obtener la versión del sistema.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Versión de sistema operativo
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: ae90f4eac5546fccd7513d781234896fbbbda93ff3723a9ac1db438321ecf214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763957"
---
# <a name="operating-system-version"></a>Versión de sistema operativo

Las [funciones auxiliares de api de](version-helper-apis.md) versión se usan para determinar la versión del sistema operativo que se está ejecutando actualmente. Para obtener más información, vea [Obtener la versión del sistema](getting-the-system-version.md).

En la tabla siguiente se resumen los números de versión más recientes del sistema operativo.

| Sistema operativo | Número de la versión |
|------------------|----------------|
| Windows 10       | 10.0\*         |
| Windows Server 2019 | 10.0\*      |
| Windows Server 2016 | 10.0\*      |
| Windows 8.1      | 6.3\*          |
| Windows Server 2012 R2 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6,0         |
| Windows Vista    | 6,0            |
| Windows Server 2003 R2 | 5.2      |
| Windows Server 2003 | 5.2         |
| Windows XP 64-Bit Edition | 5.2   |
| Windows XP | 5,1                  |
| Windows 2000     | 5.0            |

**\*** Para las aplicaciones que se han manifiesto para Windows 8.1 o Windows 10. Las aplicaciones no manifestadas para Windows 8.1 o Windows 10 devolverán el Windows 8 versión del sistema operativo (6.2). Para manifiesto las aplicaciones para Windows 8.1 o Windows 10, consulte Destino [de la aplicación para Windows](targeting-your-application-at-windows-8-1.md).<br/>

La identificación del sistema operativo actual no suele ser la mejor manera de determinar si una característica de sistema operativo determinada está presente. Esto se debe a que el sistema operativo puede haber tenido nuevas características agregadas en un archivo DLL redistribuible. En lugar de usar las [funciones auxiliares](version-helper-apis.md) de api de versión para determinar la plataforma del sistema operativo o el número de versión, compruebe la presencia de la propia característica.

Para determinar la mejor manera de probar una característica, consulte la documentación de la característica de interés. En la lista siguiente se de analizan algunas técnicas comunes para la detección de características:

- Puede probar la presencia de las funciones asociadas a una característica. Para comprobar la presencia de una función en un archivo DLL del sistema, llame a la [**función LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar el archivo DLL. A continuación, [**llame a la función GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para determinar si la función de interés está presente en el archivo DLL. Use el puntero devuelto por **GetProcAddress** para llamar a la función. Tenga en cuenta que incluso si la función está presente, puede ser un código auxiliar que simplemente devuelve un código de error como ERROR \_ CALL \_ NOT \_ IMPLEMENTED.
- Puede determinar la presencia de algunas características mediante la [**función GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Por ejemplo, puede detectar varios monitores de pantalla llamando a **GetSystemMetrics**(SM \_ CMONITORS).
- Hay varias versiones de los archivos DLL redistribuibles que implementan características de shell y control comunes. Para obtener información sobre cómo determinar qué versiones están presentes en el sistema en el que se ejecuta la aplicación, vea el tema Versiones de [shell y controles comunes](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)).

Si necesita un sistema operativo determinado, asegúrese de usarlo como versión mínima admitida, en lugar de diseñar la prueba para el único sistema operativo. De este modo, el código de detección seguirá funcionando en versiones futuras de Windows.

Tenga en cuenta que una aplicación de 32 bits puede detectar si se ejecuta en WOW64 llamando a la [**función IsWow64Process.**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) Puede obtener información adicional del procesador llamando a la [**función GetNativeSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

Para obtener más información, consulte Windows 10 [de la versión y](/windows/release-information/) Windows de datos del ciclo de [vida.](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)

