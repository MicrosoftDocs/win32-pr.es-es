---
description: El controlador de símbolos cargará símbolos al llamar a la función SymInitialize con el parámetro fInvadeProcess establecido en TRUE o al llamar a la función SymLoadModuleEx para especificar un módulo.
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: Carga de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1459f0fd05b490730739852b77edd29df38c04cbe246699552a53b7e30decf11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912384"
---
# <a name="symbol-loading"></a>Carga de símbolos

El controlador de símbolos cargará símbolos al llamar a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) con el parámetro *fInvadeProcess* establecido en **TRUE** o al llamar a la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) para especificar un módulo. En cualquier caso, el controlador de símbolos carga los símbolos o aplaza la carga de símbolos hasta que se solicitan los símbolos, en función de las opciones establecidas por la [**función SymSetOptions.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)

El controlador de símbolos se puede usar para recuperar información simbólica de cualquier módulo; no es necesario asociarlo a un proceso especificado en la [**llamada a SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) Para usar un módulo arbitrario, especifique la ruta de acceso completa a la imagen del módulo en el *parámetro ImageName.* Puede usar una ruta de acceso a cualquier módulo ejecutable que tenga información de depuración (.exe, .dll, .drv, .sys, .scr, .cpl o .com). Use el *parámetro BaseOfDll* para especificar cualquier dirección de carga y, a continuación, las direcciones de símbolos se basarán desde esa dirección.

Es posible que no sea necesario mantener un módulo de símbolos cargado durante la duración de una aplicación. Para liberar el módulo de símbolos de la lista de módulos del controlador de símbolos, use la [**función SymUnloadModule64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) Esta función libera la memoria asignada para el módulo de símbolos. Para volver a usar símbolos para ese módulo, debe llamar a la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) aunque se establezca la opción de carga diferida de símbolos.

## <a name="diagnosing-symbol-load-problems"></a>Diagnóstico de problemas de carga de símbolos

Para ver todos los intentos de cargar símbolos, llame [**a SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con SYMOPT \_ DEBUG. Esto hace que DbgHelp llame a la función [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) con información detallada sobre las búsquedas de símbolos, como los directorios que está buscando y los mensajes de error. Si el código usa [**SymRegisterCallback64,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)DbgHelp llamará a la función de devolución de llamada en lugar de llamar a **OutputDebugString**. El *parámetro ActionCode* se establece en CBA DEBUG INFO y el parámetro \_ \_ *CallbackData* es una cadena que se puede mostrar.

Para permitir que esta salida de depuración se muestre en la consola sin cambiar el código fuente, establezca la variable de entorno DBGHELP DBGOUT en un valor distinto de NULL antes de llamar a la función \_ [**SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  Para registrar la información en un archivo, establezca la variable de entorno DBGHELP LOG en el nombre del archivo de registro que \_ se va a usar.

Tenga en cuenta que estas características solo se deben usar cuando sea necesario. Pueden ralentizar la carga de símbolos de módulos que contienen muchos símbolos.

 

 
