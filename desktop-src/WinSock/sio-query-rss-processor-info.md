---
description: El código de control consulta la asociación entre un socket y un nodo principal y NUMA del procesador de RSS.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: Código de control de SIO_QUERY_RSS_PROCESSOR_INFO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001135"
---
# <a name="sio_query_rss_processor_info-control-code"></a><span data-ttu-id="5f823-103">Código de control de SIO_QUERY_RSS_PROCESSOR_INFO</span><span class="sxs-lookup"><span data-stu-id="5f823-103">SIO_QUERY_RSS_PROCESSOR_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="5f823-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f823-104">Description</span></span>

<span data-ttu-id="5f823-105">El código de control de **\_ \_ \_ \_ información del procesador RSS de la consulta SiO consulta** la asociación entre un socket y un nodo principal y Numa del procesador de RSS.</span><span class="sxs-lookup"><span data-stu-id="5f823-105">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** control code queries the association between a socket and an RSS processor core and NUMA node.</span></span>

<span data-ttu-id="5f823-106">Para realizar esta operación, llame a la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="5f823-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="5f823-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f823-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="5f823-108">s</span><span class="sxs-lookup"><span data-stu-id="5f823-108">s</span></span>

<span data-ttu-id="5f823-109">Un descriptor que identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="5f823-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="5f823-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="5f823-110">dwIoControlCode</span></span>

<span data-ttu-id="5f823-111">Código de control de la operación.</span><span class="sxs-lookup"><span data-stu-id="5f823-111">The control code for the operation.</span></span>
<span data-ttu-id="5f823-112">Use **la \_ \_ información del \_ procesador \_ RSS de la consulta SiO** para esta operación.</span><span class="sxs-lookup"><span data-stu-id="5f823-112">Use **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="5f823-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="5f823-113">lpvInBuffer</span></span>

<span data-ttu-id="5f823-114">Puntero al búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="5f823-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="5f823-115">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="5f823-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="5f823-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="5f823-116">cbInBuffer</span></span>

<span data-ttu-id="5f823-117">Tamaño, en bytes, del búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="5f823-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="5f823-118">Este parámetro no se usa para esta operación.</span><span class="sxs-lookup"><span data-stu-id="5f823-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="5f823-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="5f823-119">lpvOutBuffer</span></span>

<span data-ttu-id="5f823-120">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5f823-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="5f823-121">Este parámetro debe apuntar a una estructura de [**\_ \_ afinidad de procesador de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) si los parámetros *lpOverlapped* y *lpCompletionRoutine* son **null**.</span><span class="sxs-lookup"><span data-stu-id="5f823-121">This parameter should point to a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="5f823-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="5f823-122">cbOutBuffer</span></span>

<span data-ttu-id="5f823-123">Tamaño, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5f823-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="5f823-124">Este parámetro debe ser al menos el tamaño de una estructura de [**\_ \_ afinidad de procesador de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="5f823-124">This parameter must be at least the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="5f823-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="5f823-125">lpcbBytesReturned</span></span>

<span data-ttu-id="5f823-126">Puntero a una variable que recibe el tamaño, en bytes, de los datos almacenados en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5f823-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="5f823-127">Si el búfer de salida es demasiado pequeño, se produce un error en la llamada, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) devuelve [**WSAEINVAL**](windows-sockets-error-codes-2.md)y el parámetro *LpcbBytesReturned* apunta a un valor *DWORD* de cero.</span><span class="sxs-lookup"><span data-stu-id="5f823-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a *DWORD* value of zero.</span></span>

<span data-ttu-id="5f823-128">Si *lpOverlapped* es **null**, el valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* devuelto en una llamada correcta no puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f823-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="5f823-129">Si el parámetro *lpOverlapped* no es **null** para los sockets superpuestos, las operaciones que no se pueden completar inmediatamente se iniciarán y la finalización se indicará más adelante.</span><span class="sxs-lookup"><span data-stu-id="5f823-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="5f823-130">El valor **DWORD** al que apunta el parámetro *lpcbBytesReturned* que se devuelve puede ser cero, ya que no se puede determinar el tamaño de los datos almacenados hasta que se haya completado la operación superpuesta.</span><span class="sxs-lookup"><span data-stu-id="5f823-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="5f823-131">Se puede recuperar el estado final de finalización cuando se señala el método de finalización adecuado cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="5f823-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="5f823-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="5f823-132">lpvOverlapped</span></span>

<span data-ttu-id="5f823-133">Puntero a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="5f823-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="5f823-134">Si el socket *s* se creó sin el atributo superpuesto, se omite el parámetro *lpOverlapped* .</span><span class="sxs-lookup"><span data-stu-id="5f823-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="5f823-135">Si se abrió *s* con el atributo superpuesto y el parámetro *LpOverlapped* no es **null**, la operación se realiza como una operación superpuesta (asincrónica).</span><span class="sxs-lookup"><span data-stu-id="5f823-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="5f823-136">En este caso, el parámetro *lpOverlapped* debe apuntar a una estructura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.</span><span class="sxs-lookup"><span data-stu-id="5f823-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="5f823-137">En el caso de las operaciones superpuestas, las funciones [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** se devuelven inmediatamente y el método de finalización adecuado se señala cuando se ha completado la operación.</span><span class="sxs-lookup"><span data-stu-id="5f823-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="5f823-138">De lo contrario, la función no devuelve ningún resultado hasta que se haya completado la operación o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="5f823-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="5f823-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="5f823-139">lpCompletionRoutine</span></span>

<span data-ttu-id="5f823-140">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="5f823-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="5f823-141">Puntero a la rutina de finalización a la que se llama cuando la operación se ha completado (se omite para los sockets no superpuestos).</span><span class="sxs-lookup"><span data-stu-id="5f823-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="5f823-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="5f823-142">lpThreadId</span></span>

<span data-ttu-id="5f823-143">Puntero a una estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) que va a usar el proveedor en una llamada subsiguiente a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="5f823-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="5f823-144">El proveedor debe almacenar la estructura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a la que se hace referencia (no el puntero a la misma) hasta que se devuelva la función [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="5f823-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="5f823-145">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5f823-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="5f823-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="5f823-146">lpErrno</span></span>

<span data-ttu-id="5f823-147">Puntero al código de error.</span><span class="sxs-lookup"><span data-stu-id="5f823-147">A pointer to the error code.</span></span>

<span data-ttu-id="5f823-148">**Nota:**  Este parámetro solo se aplica a la función **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5f823-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f823-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f823-149">Return value</span></span>

<span data-ttu-id="5f823-150">Si la operación se completa correctamente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5f823-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="5f823-151">Si se produce un error en la operación o está pendiente, la función [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** devuelve un **\_ error de socket**.</span><span class="sxs-lookup"><span data-stu-id="5f823-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="5f823-152">Para obtener información de error extendida, llame a [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="5f823-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="5f823-153">Código de error</span><span class="sxs-lookup"><span data-stu-id="5f823-153">Error code</span></span> | <span data-ttu-id="5f823-154">Significado</span><span class="sxs-lookup"><span data-stu-id="5f823-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="5f823-155">**ERROR \_ de \_ búfer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="5f823-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="5f823-156">El área de datos que se pasa a una llamada del sistema es demasiado pequeña.</span><span class="sxs-lookup"><span data-stu-id="5f823-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="5f823-157">Se devuelve este error si el búfer señalado por el parámetro *lpvOutBuffer* con un tamaño de búfer pasado en el parámetro *cbOutBuffer* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="5f823-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="5f823-158">El tamaño de búfer necesario se devolverá en el parámetro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="5f823-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> <span data-ttu-id="5f823-159">Se devuelve este error si el parámetro *cbOutBuffer* es menor que el tamaño de una estructura de [**\_ \_ afinidad de procesador de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="5f823-159">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span> |
| <span data-ttu-id="5f823-160">**\_e/s de WSA \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="5f823-160">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="5f823-161">Se inició correctamente una operación superpuesta y la finalización se indicará en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="5f823-161">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="5f823-162">**\_operación WSA \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="5f823-162">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="5f823-163">Se canceló una operación superpuesta debido al cierre del socket o a la ejecución del comando **SiO \_ Flush** ioctl.</span><span class="sxs-lookup"><span data-stu-id="5f823-163">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="5f823-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="5f823-164">**WSAEFAULT**</span></span> | <span data-ttu-id="5f823-165">Los parámetros *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* no están totalmente contenidos en una parte válida del espacio de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="5f823-165">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="5f823-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="5f823-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="5f823-167">La función se invoca cuando una devolución de llamada está en curso.</span><span class="sxs-lookup"><span data-stu-id="5f823-167">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="5f823-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="5f823-168">**WSAEINTR**</span></span> | <span data-ttu-id="5f823-169">Se interrumpió una operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="5f823-169">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="5f823-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="5f823-170">**WSAEINVAL**</span></span> | <span data-ttu-id="5f823-171">El parámetro *dwIoControlCode* no es un comando válido o un parámetro de entrada especificado no es aceptable, o bien el comando no es aplicable al tipo de socket especificado.</span><span class="sxs-lookup"><span data-stu-id="5f823-171">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="5f823-172">Se devuelve este error si el parámetro *cbOutBuffer* es menor que el tamaño de una estructura de [**\_ \_ afinidad de procesador de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="5f823-172">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>
| <span data-ttu-id="5f823-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="5f823-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="5f823-174">Error en el subsistema de red.</span><span class="sxs-lookup"><span data-stu-id="5f823-174">The network subsystem has failed.</span></span> |
| <span data-ttu-id="5f823-175">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="5f823-175">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="5f823-176">No se admite la opción socket en el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="5f823-176">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="5f823-177">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="5f823-177">**WSAENOTCONN**</span></span> | <span data-ttu-id="5f823-178">El socket *s* no está conectado.</span><span class="sxs-lookup"><span data-stu-id="5f823-178">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="5f823-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="5f823-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="5f823-180">El descriptor *s* no es un socket.</span><span class="sxs-lookup"><span data-stu-id="5f823-180">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="5f823-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="5f823-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="5f823-182">No se admite el comando IOCTL especificado.</span><span class="sxs-lookup"><span data-stu-id="5f823-182">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="5f823-183">Este error se devuelve si el proveedor de transporte no admite la **\_ \_ \_ \_ información del procesador RSS de la consulta SiO** .</span><span class="sxs-lookup"><span data-stu-id="5f823-183">This error is returned if the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="5f823-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f823-184">Remarks</span></span>

<span data-ttu-id="5f823-185">La **\_ información del \_ \_ procesador RSS \_ de la consulta SiO** es compatible con Windows 8, Windows Server 2012 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5f823-185">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="5f823-186">La **\_ información del \_ \_ procesador \_ de RSS de la consulta SiO** se usa para determinar la asociación entre un socket y un nodo de núcleo de procesador RSS y Numa.</span><span class="sxs-lookup"><span data-stu-id="5f823-186">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is used to determine the association between a socket and an RSS processor core and NUMA node.</span></span>
<span data-ttu-id="5f823-187">Este IOCTL devuelve una estructura de [**\_ \_ afinidad de procesador de sockets**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) que contiene el [**\_ número de procesador**](/windows/desktop/api/winnt/ns-winnt-processor_number) y el identificador de nodo Numa.</span><span class="sxs-lookup"><span data-stu-id="5f823-187">This IOCTL returns a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure that contains the [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) and the NUMA node ID.</span></span>
<span data-ttu-id="5f823-188">La estructura [**del \_ número de procesador**](/windows/desktop/api/winnt/ns-winnt-processor_number) devuelto contiene un número de grupo y un número de procesador relativo dentro del grupo.</span><span class="sxs-lookup"><span data-stu-id="5f823-188">The returned [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) structure contains a group number and relative processor number within the group.</span></span>

<span data-ttu-id="5f823-189">Si el socket es un socket UDP, el socket debe estar conectado para que el ioctl de **\_ \_ \_ \_ información del procesador RSS de la consulta SiO** funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="5f823-189">If the socket is a UDP socket, the socket must be connected for the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL to work properly.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f823-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f823-190">See also</span></span>

[<span data-ttu-id="5f823-191">**PROCESSOR_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="5f823-191">**PROCESSOR_NUMBER**</span></span>](/windows/desktop/api/winnt/ns-winnt-processor_number)

[<span data-ttu-id="5f823-192">**tomacorriente**</span><span class="sxs-lookup"><span data-stu-id="5f823-192">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="5f823-193">**SOCKET_PROCESSOR_AFFINITY**</span><span class="sxs-lookup"><span data-stu-id="5f823-193">**SOCKET_PROCESSOR_AFFINITY**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[<span data-ttu-id="5f823-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="5f823-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="5f823-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="5f823-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="5f823-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="5f823-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="5f823-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="5f823-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="5f823-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="5f823-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="5f823-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="5f823-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
