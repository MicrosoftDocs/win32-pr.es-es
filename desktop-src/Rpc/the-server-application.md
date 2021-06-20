---
title: La aplicación de servidor
description: Vea la parte de la aplicación de servidor de un ejemplo de llamada a procedimiento remoto (RPC). El ejemplo es de la aplicación "Hola mundo" del SDK de plataforma.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406068"
---
# <a name="the-server-application"></a>La aplicación de servidor

El ejemplo siguiente es de la aplicación "Hola mundo" en el directorio RPC Hello del \\ Kit de desarrollo de software (SDK) de plataforma. El lado servidor de la aplicación distribuida informa al sistema de que sus servicios están disponibles. A continuación, espera las solicitudes de cliente. El compilador MIDL debe usarse con el ejemplo siguiente.

Según el tamaño de la aplicación y las preferencias de codificación, puede optar por implementar procedimientos remotos en uno o varios archivos independientes. En este programa de tutorial, el archivo de origen Hellos.c contiene la rutina de servidor principal. El archivo Hellop.c contiene el procedimiento remoto.

La ventaja de organizar los procedimientos remotos en archivos independientes es que los procedimientos se pueden vincular con un programa independiente para depurar el código antes de convertirlo en una aplicación distribuida. Una vez que los procedimientos funcionan en el programa independiente, puede compilar y vincular los archivos de origen que contienen los procedimientos remotos con la aplicación de servidor. Al igual que con el archivo de origen de aplicación cliente, el archivo de origen de aplicación de servidor debe incluir el archivo de encabezado Hello.h.

El servidor llama a las funciones en tiempo de ejecución [**rpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) y [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para que la información de enlace esté disponible para el cliente. Este programa de ejemplo pasa el nombre del identificador de interfaz **a RpcServerRegisterIf**. Los demás parámetros se establecen en **NULL.** A continuación, el servidor llama [**a la función RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para indicar que está esperando solicitudes de cliente.

La aplicación de servidor también debe incluir las dos funciones de administración de memoria a las que llama el código auxiliar del servidor: [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) y [**midl \_ user \_ free**](the-midl-user-free-function.md). Estas funciones asignan y liberan memoria en el servidor cuando un procedimiento remoto pasa parámetros al servidor. En este programa de ejemplo, **midl \_ user \_ allocate** y **midl \_ user \_ free** son simplemente contenedores para las funciones [**malloc**](pointers-and-memory-allocation.md) y **free** de la biblioteca de C. (Tenga en cuenta que, en las declaraciones de reenvío generadas por el compilador MIDL, "MIDL" está en mayúsculas. El archivo de encabezado Rpc rpcl.h define midl user free y midl user allocate para que sea midL user free y \_ \_ \_ \_ \_ \_ MIDL \_ user \_ allocate, respectivamente).


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
 }

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 




