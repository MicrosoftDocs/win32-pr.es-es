---
title: Palabra clave sh_thread
description: La \_ palabra clave \ SH Thread \ especifica que el objeto del sistema es un identificador de un subproceso.
keywords:
- palabra clave sh_thread MIDL
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2c82dc41d2b1c7cba740c897ef6cea9094979cc3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104279729"
---
# <a name="sh_thread-keyword"></a><span data-ttu-id="bf717-104">SH \_ Thread (palabra clave)</span><span class="sxs-lookup"><span data-stu-id="bf717-104">sh\_thread keyword</span></span>

<span data-ttu-id="bf717-105">La palabra clave de **\_ subproceso SH** especifica que un `system_handle` contiene un identificador de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="bf717-105">The **sh\_thread** keyword specifies that a `system_handle` holds a handle to a thread.</span></span>

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="bf717-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf717-106">Parameters</span></span>

<span data-ttu-id="bf717-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="bf717-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="bf717-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="bf717-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="bf717-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="bf717-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf717-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf717-110">Remarks</span></span>

<span data-ttu-id="bf717-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="bf717-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="bf717-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bf717-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="bf717-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf717-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="bf717-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf717-114">Minimum supported client</span></span> | <span data-ttu-id="bf717-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="bf717-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="bf717-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf717-116">Minimum supported server</span></span> | <span data-ttu-id="bf717-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="bf717-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="bf717-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf717-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf717-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="bf717-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="bf717-120">Acerca de los procesos y los subprocesos</span><span class="sxs-lookup"><span data-stu-id="bf717-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="bf717-121">Seguridad para subprocesos y derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="bf717-121">Thread Security and Access Rights</span></span>](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="bf717-122">**CreateThread** (función)</span><span class="sxs-lookup"><span data-stu-id="bf717-122">**CreateThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[<span data-ttu-id="bf717-123">**OpenThread** función)</span><span class="sxs-lookup"><span data-stu-id="bf717-123">**OpenThread** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>