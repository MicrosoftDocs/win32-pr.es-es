---
description: El espacio de trabajo de un programa es una colección de las páginas de su espacio de direcciones virtuales a las que se ha hecho referencia recientemente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Espacio de trabajo del proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276817"
---
# <a name="process-working-set"></a>Espacio de trabajo del proceso

El espacio de *trabajo* de un programa es una colección de las páginas de su espacio de direcciones virtuales a las que se ha hecho referencia recientemente. Incluye datos compartidos y privados. Los datos compartidos incluyen páginas que contienen todas las instrucciones que ejecuta la aplicación, incluidas las de los archivos dll y los archivos DLL del sistema. A medida que aumenta el tamaño del espacio de trabajo, aumenta la demanda de memoria.

Un proceso tiene un tamaño de espacio de trabajo mínimo asociado y un tamaño máximo del espacio de trabajo. Cada vez que se llama a [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), reserva el tamaño mínimo del espacio de trabajo para el proceso. El administrador de memoria virtual intenta mantener suficiente memoria para el espacio de trabajo mínimo residente cuando el proceso está activo, pero no mantiene más que el tamaño máximo.

Para obtener los tamaños mínimos y máximos solicitados del espacio de trabajo para la aplicación, llame a la función [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) .

El sistema establece los tamaños predeterminados del espacio de trabajo. También puede modificar los tamaños del espacio de trabajo mediante la función [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) . Establecer estos valores no es una garantía de que la memoria estará reservada o residente. Tenga cuidado al solicitar un tamaño de espacio de trabajo mínimo o máximo, ya que esto puede reducir el rendimiento del sistema.

Para obtener el tamaño actual o máximo del espacio de trabajo para el proceso, utilice la función [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información de rendimiento de memoria](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[Espacio de trabajo](../memory/working-set.md)
</dt> </dl>

 

 
