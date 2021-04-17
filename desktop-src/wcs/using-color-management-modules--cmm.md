---
title: Uso de módulos de administración del color (CMM)
description: Los módulos de administración de color (CMMs) son módulos de código WCS que usan la información de perfiles de dispositivo para realizar la conversión de colores y la asignación de colores.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Sistema de color de Windows (WCS), módulo de administración de color (CMM)
- WCS (sistema de colores de Windows), módulo de administración del color (CMM)
- Administración del color de imagen, módulo de administración del color (CMM)
- Administración del color, módulo de administración del color (CMM)
- colores, módulo de administración del color (CMM)
- Módulo de administración del color (CMM)
- CMM (módulo de administración del color)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518558305639f0699358f22fb3544698741cfedf
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/02/2021
ms.locfileid: "105721157"
---
# <a name="using-color-management-modules-cmm"></a>Uso de módulos de administración del color (CMM)

Los módulos de administración de color (CMMs) son módulos de código WCS que usan la información de perfiles de dispositivo para realizar la conversión de colores y la asignación de colores. Los desarrolladores de aplicaciones no deben tener que implementar CMMs. Microsoft proporciona la CMM predeterminada. Sin embargo, si escribe software que requiere el uso de algoritmos de conversión de colores y de asignación de colores especializados, puede crear uno.

> [!Note]  
> Los puntos de entrada de CMM *no* son funciones de API y las aplicaciones no deben llamarlos.

 

Cuando se instalan CMMs, el programa de instalación los registra en el registro de Windows. Las aplicaciones pueden enumerar el CMMs registrado y seleccionar uno mediante la función [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) . En la aplicación de ejemplo siguiente se muestra cómo enumerar todas las CMMs registradas.


```C++
#include <stdio.h>
#include <stdlib.h>
#include <stddef.h>
#include <string.h>
#include <mbstring.h>
#include <windows.h>
#include <icm.h>

#ifdef WINDOWS_98
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\ICM\\ICMatchers");
#else
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ICMatchers");
#endif

_CRTAPI1 main (int argc, char *argv[])
{
    DWORD dwNumCMM = 0;

    HANDLE hkCMM;
    DWORD dwErr = RegCreateKey(HKEY_LOCAL_MACHINE,
                 gszICMatcher, &amp;hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&amp;hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &amp;dwMaxName, &amp;dwMaxValue,
                                NULL, NULL);
    TCHAR chCMM[dwMaxName];
    ULONG cjCMM = sizeof(chCMM)/sizeof(chCMM[0]);
    DWORD dwType;
    TCHAR chCMMFile[dwMaxValue];
    ULONG cjCMMFile = sizeof(chCMMFile)/sizeof(chCMMFile[0]);

    if (dwErr != ERROR_SUCCESS)
    {
        printf("Could not open ICMatcher registry key: %d\n", dwErr);
    }

    if (dwErr == ERROR_SUCCESS)
    {
        while (RegEnumValue(
                   hkCMM,dwNumCMM,chCMM,
                   &amp;cjCMM,NULL,&amp;dwType,
                   chCMMFile,&amp;cjCMMFile) == ERROR_SUCCESS)
        {
            if (dwType == REG_SZ)
            {
                printf("%d: %-80s - %-80s\n",dwNumCMM,chCMM,chCMMFile);
            }
            else
            {
                printf("%d: error\n");
            }

            dwNumCMM++;
            cjCMM = sizeof(chCMM);
            cjCMMFile = sizeof(chCMMFile);
        }
    }

    RegCloseKey(hkCMM);
}
```



 

 




