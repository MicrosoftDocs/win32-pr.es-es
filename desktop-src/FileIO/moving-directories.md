---
description: Para mover un directorio a otra ubicación, junto con los archivos y subdirectorios que contiene, llame a la función MoveFileEx, MoveFileWithProgress o MoveFileTransacted.
ms.assetid: ca56c109-d6a3-456e-956c-126ce4aee8ba
title: Mover directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da891e22c2840ad9460f5fb43c8cc1b130905b86de80a988be2eeeb9a4010ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951144"
---
# <a name="moving-directories"></a>Mover directorios

Para mover un directorio a otra ubicación, junto con los archivos y subdirectorios que contiene, llame a la función [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa), [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)o [**MoveFileTransacted.**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) La [**función MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa) tiene la misma funcionalidad que [**MoveFileEx,**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)salvo que **MoveFileWithProgress** permite especificar una rutina de devolución de llamada que recibe notificaciones sobre el progreso de la operación. La [**función MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) permite realizar la operación como una operación con transacciones.

En el ejemplo siguiente se muestra el uso de la [**función MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) con un directorio .


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    printf("\n");
    if( argc != 3 )
    {
        printf("ERROR:  Incorrect number of arguments\n\n");
        printf("Description:\n");
        printf("  Moves a directory and its contents\n\n");
        printf("Usage:\n");
        _tprintf(TEXT("  %s [source_dir] [target_dir]\n\n"), argv[0]);
        printf("  The target directory cannot exist already.\n\n");
        return;
    }

    // Move the source directory to the target directory location.
    // The target directory must be on the same drive as the source.
    // The target directory cannot already exist.

    if (!MoveFileEx(argv[1], argv[2], MOVEFILE_WRITE_THROUGH))
    { 
        printf ("MoveFileEx failed with error %d\n", GetLastError());
        return;
    }
    else _tprintf(TEXT("%s has been moved to %s\n"), argv[1], argv[2]);
}
```



 

 



