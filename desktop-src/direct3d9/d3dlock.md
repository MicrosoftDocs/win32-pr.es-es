---
description: Combinación de cero o más opciones de bloqueo que describen el tipo de bloqueo que se debe realizar.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adaeddbc1aff0812d3e0f67df90c2cf9b1118347
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999432"
---
# <a name="d3dlock"></a><span data-ttu-id="a053b-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="a053b-103">D3DLOCK</span></span>

<span data-ttu-id="a053b-104">Combinación de cero o más opciones de bloqueo que describen el tipo de bloqueo que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="a053b-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



| <span data-ttu-id="a053b-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="a053b-105">\#define</span></span>                   | <span data-ttu-id="a053b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a053b-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a053b-107">D3DLOCK \_ DISCARD</span><span class="sxs-lookup"><span data-stu-id="a053b-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="a053b-108">La aplicación descarta toda la memoria dentro de la región bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a053b-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="a053b-109">En el caso de los búferes de vértices e índices, se descartará todo el búfer.</span><span class="sxs-lookup"><span data-stu-id="a053b-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="a053b-110">Esta opción solo es válida cuando el recurso se crea con uso dinámico (consulte [D3DUSAGE).](d3dusage.md)</span><span class="sxs-lookup"><span data-stu-id="a053b-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a053b-111">D3DLOCK \_ DONOTWAIT</span><span class="sxs-lookup"><span data-stu-id="a053b-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="a053b-112">Permite a una aplicación recuperar ciclos de CPU si el controlador no puede bloquear la superficie inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a053b-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="a053b-113">Si se establece esta marca y el controlador no puede bloquear la superficie inmediatamente, la llamada de bloqueo devolverá D3DERR \_ WASST ODBCDRAWING.</span><span class="sxs-lookup"><span data-stu-id="a053b-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="a053b-114">Esta marca solo se puede usar al bloquear una superficie creada mediante [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateRenderTarget**](/windows/desktop/api)o [**CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)</span><span class="sxs-lookup"><span data-stu-id="a053b-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="a053b-115">Esta marca también se puede usar con un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="a053b-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="a053b-116">D3DLOCK \_ NO \_ DIRTY \_ UPDATE</span><span class="sxs-lookup"><span data-stu-id="a053b-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="a053b-117">De forma predeterminada, un bloqueo en un recurso agrega una región desarroba a ese recurso.</span><span class="sxs-lookup"><span data-stu-id="a053b-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="a053b-118">Esta opción evita cualquier cambio en el estado desasecionado del recurso.</span><span class="sxs-lookup"><span data-stu-id="a053b-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="a053b-119">Las aplicaciones deben usar esta opción cuando tengan información adicional sobre el conjunto de regiones modificadas durante la operación de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a053b-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a053b-120">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="a053b-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="a053b-121">Indica que la memoria a la que se hizo referencia en una llamada de dibujo desde el último bloqueo sin esta marca no se modificará durante el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a053b-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="a053b-122">Esto puede habilitar las optimizaciones cuando la aplicación anexa datos a un recurso.</span><span class="sxs-lookup"><span data-stu-id="a053b-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="a053b-123">Al especificar esta marca, el controlador puede devolver inmediatamente si el recurso está en uso; de lo contrario, el controlador debe terminar de usar el recurso antes de volver del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a053b-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="a053b-124">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="a053b-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="a053b-125">El comportamiento predeterminado de un bloqueo de memoria de vídeo es reservar una sección crítica para todo el sistema, lo que garantiza que no se producirá ningún cambio en el modo de presentación mientras dure el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a053b-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="a053b-126">Esta opción hace que la sección crítica de todo el sistema no se mantiene mientras dure el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a053b-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="a053b-127">La operación de bloqueo lleva mucho tiempo, pero puede permitir que el sistema realice otras tareas, como mover el cursor del mouse.</span><span class="sxs-lookup"><span data-stu-id="a053b-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="a053b-128">Esta opción es útil para bloqueos de larga duración, como el bloqueo del búfer de reserva para la representación de software que, de lo contrario, afectaría negativamente a la capacidad de respuesta del sistema.</span><span class="sxs-lookup"><span data-stu-id="a053b-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="a053b-129">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="a053b-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="a053b-130">La aplicación no escribirá en el búfer.</span><span class="sxs-lookup"><span data-stu-id="a053b-130">The application will not write to the buffer.</span></span> <span data-ttu-id="a053b-131">Esto permite que los recursos almacenados en formatos no nativos guarden el paso de recompresión al desbloquear.</span><span class="sxs-lookup"><span data-stu-id="a053b-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="a053b-132">Información constante</span><span class="sxs-lookup"><span data-stu-id="a053b-132">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="a053b-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a053b-133">Header</span></span>                   | <span data-ttu-id="a053b-134">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="a053b-134">d3d9types.h</span></span> |
| <span data-ttu-id="a053b-135">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="a053b-135">Minimum operating system</span></span> | <span data-ttu-id="a053b-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a053b-136">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="a053b-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a053b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a053b-138">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a053b-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="a053b-139">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="a053b-139">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="a053b-140">**Lock**</span><span class="sxs-lookup"><span data-stu-id="a053b-140">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="a053b-141">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="a053b-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="a053b-142">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="a053b-142">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="a053b-143">**Lock**</span><span class="sxs-lookup"><span data-stu-id="a053b-143">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="a053b-144">**Caja**</span><span class="sxs-lookup"><span data-stu-id="a053b-144">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="a053b-145">**Caja**</span><span class="sxs-lookup"><span data-stu-id="a053b-145">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="a053b-146">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="a053b-146">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="a053b-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="a053b-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="a053b-148">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="a053b-148">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="a053b-149">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="a053b-149">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="a053b-150">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="a053b-150">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="a053b-151">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="a053b-151">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="a053b-152">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="a053b-152">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
