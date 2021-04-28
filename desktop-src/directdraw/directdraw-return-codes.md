---
title: Códigos de retorno de DirectDraw (Ddraw.h)
description: 'Códigos de retorno de DirectDraw: los errores se representan mediante valores negativos y no se pueden combinar.'
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d789a233df777d98860e519f7e877a030aba55a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087813"
---
# <a name="directdraw-return-codes"></a><span data-ttu-id="2e276-103">Códigos de retorno de DirectDraw</span><span class="sxs-lookup"><span data-stu-id="2e276-103">DirectDraw Return Codes</span></span>

<span data-ttu-id="2e276-104">Los errores se representan mediante valores negativos y no se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="2e276-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="2e276-105">En esta tabla se enumeran los valores que pueden devolver todos los métodos de las funciones [DirectDraw Interfaces](directdraw-interfaces.md) [y DirectDraw](directdraw-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2e276-105">This table lists the values that can be returned by all methods of the [DirectDraw Interfaces](directdraw-interfaces.md) and [DirectDraw Functions](directdraw-functions.md).</span></span> <span data-ttu-id="2e276-106">Para obtener una lista de los códigos de error que puede devolver cada método o función, vea la descripción del método o la función.</span><span class="sxs-lookup"><span data-stu-id="2e276-106">For a list of the error codes that each method or function can return, see the method or function description.</span></span>

<dl> <dt>

<span data-ttu-id="2e276-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**</span><span class="sxs-lookup"><span data-stu-id="2e276-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD\_OK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-108">La solicitud se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e276-108">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR \_ YA INICIALIZADO**</span><span class="sxs-lookup"><span data-stu-id="2e276-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR\_ALREADYINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-110">El objeto ya se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="2e276-110">The object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR \_ BLTFASTCANTCLIP**</span><span class="sxs-lookup"><span data-stu-id="2e276-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR\_BLTFASTCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-112">Un objeto DirectDrawClipper se adjunta a una superficie de origen que ha pasado a una llamada al método [**IDirectDrawSurface7::BltFast.**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast)</span><span class="sxs-lookup"><span data-stu-id="2e276-112">A DirectDrawClipper object is attached to a source surface that has passed into a call to the [**IDirectDrawSurface7::BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR \_ CANNOTATTACHSURFACE**</span><span class="sxs-lookup"><span data-stu-id="2e276-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR\_CANNOTATTACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-114">Una superficie no se puede adjuntar a otra superficie solicitada.</span><span class="sxs-lookup"><span data-stu-id="2e276-114">A surface cannot be attached to another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR \_ CANNOTDETACHSURFACE**</span><span class="sxs-lookup"><span data-stu-id="2e276-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR\_CANNOTDETACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-116">Una superficie no se puede desasociar de otra superficie solicitada.</span><span class="sxs-lookup"><span data-stu-id="2e276-116">A surface cannot be detached from another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR \_ CANTCREATEDC**</span><span class="sxs-lookup"><span data-stu-id="2e276-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR\_CANTCREATEDC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-118">Windows no puede crear más contextos de dispositivo (DC) o un controlador de dominio ha solicitado una superficie indizada por paleta cuando la superficie no tenía ninguna paleta y el modo de presentación no estaba indexado por paleta (en este caso, DirectDraw no puede seleccionar una paleta adecuada en el controlador de dominio).</span><span class="sxs-lookup"><span data-stu-id="2e276-118">Windows cannot create any more device contexts (DCs), or a DC has requested a palette-indexed surface when the surface had no palette and the display mode was not palette-indexed (in this case, DirectDraw cannot select a proper palette into the DC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR \_ CANTDUPLICATE**</span><span class="sxs-lookup"><span data-stu-id="2e276-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR\_CANTDUPLICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-120">Las superficies principal y 3D, o las superficies que se crean implícitamente, no se pueden duplicar.</span><span class="sxs-lookup"><span data-stu-id="2e276-120">Primary and 3-D surfaces, or surfaces that are implicitly created, cannot be duplicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR \_ CANTLOCKSURFACE**</span><span class="sxs-lookup"><span data-stu-id="2e276-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR\_CANTLOCKSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-122">Se rechaza el acceso a esta superficie porque se intentó bloquear la superficie principal sin compatibilidad con la Interfaz de control de pantalla (DCI).</span><span class="sxs-lookup"><span data-stu-id="2e276-122">Access to this surface is refused because an attempt was made to lock the primary surface without Display Control Interface (DCI) support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR \_ CANTPAGELOCK**</span><span class="sxs-lookup"><span data-stu-id="2e276-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR\_CANTPAGELOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-124">Error al intentar bloquear la página de una superficie.</span><span class="sxs-lookup"><span data-stu-id="2e276-124">An attempt to page-lock a surface failed.</span></span> <span data-ttu-id="2e276-125">El bloqueo de página no funciona en una superficie de memoria para mostrar ni en una superficie principal emulada.</span><span class="sxs-lookup"><span data-stu-id="2e276-125">Page lock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR \_ CANTPAGEUNLOCK**</span><span class="sxs-lookup"><span data-stu-id="2e276-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR\_CANTPAGEUNLOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-127">Error al intentar desbloquear una superficie.</span><span class="sxs-lookup"><span data-stu-id="2e276-127">An attempt to page-unlock a surface failed.</span></span> <span data-ttu-id="2e276-128">El desbloqueo de página no funciona en una superficie de memoria para mostrar ni en una superficie principal emulada.</span><span class="sxs-lookup"><span data-stu-id="2e276-128">Page unlock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**\_CLIPPERISUSINGHWND de DDERR**</span><span class="sxs-lookup"><span data-stu-id="2e276-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR\_CLIPPERISUSINGHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-130">Se intentó establecer una lista de clips para un objeto DirectDrawClipper que ya está supervisando un identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="2e276-130">An attempt was made to set a clip list for a DirectDrawClipper object that is already monitoring a window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR \_ COLORKEYNOTSET**</span><span class="sxs-lookup"><span data-stu-id="2e276-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR\_COLORKEYNOTSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-132">No se especifica ninguna clave de color de origen para esta operación.</span><span class="sxs-lookup"><span data-stu-id="2e276-132">No source color key is specified for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR \_ CURRENTLYNOTAVAIL**</span><span class="sxs-lookup"><span data-stu-id="2e276-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR\_CURRENTLYNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-134">Actualmente no hay soporte técnico disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-134">No support is currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR \_ DDSCAPSCOMPLEXREQUIRED**</span><span class="sxs-lookup"><span data-stu-id="2e276-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR\_DDSCAPSCOMPLEXREQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-136">Novedad de DirectX 7.0.</span><span class="sxs-lookup"><span data-stu-id="2e276-136">New for DirectX 7.0.</span></span> <span data-ttu-id="2e276-137">La superficie requiere la marca COMPLEX de DDSCAPS. \_</span><span class="sxs-lookup"><span data-stu-id="2e276-137">The surface requires the DDSCAPS\_COMPLEX flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR \_ DCALREADYCREATED**</span><span class="sxs-lookup"><span data-stu-id="2e276-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR\_DCALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-139">Ya se ha devuelto un contexto de dispositivo (DC) para esta superficie.</span><span class="sxs-lookup"><span data-stu-id="2e276-139">A device context (DC) has already been returned for this surface.</span></span> <span data-ttu-id="2e276-140">Solo se puede recuperar un controlador de dominio para cada superficie.</span><span class="sxs-lookup"><span data-stu-id="2e276-140">Only one DC can be retrieved for each surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNSURFACE**</span><span class="sxs-lookup"><span data-stu-id="2e276-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR\_DEVICEDOESNTOWNSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-142">Las superficies creadas por un dispositivo DirectDraw no se pueden usar directamente en otro dispositivo DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="2e276-142">Surfaces created by one DirectDraw device cannot be used directly by another DirectDraw device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**</span><span class="sxs-lookup"><span data-stu-id="2e276-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR\_DIRECTDRAWALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-144">Ya se ha creado un objeto DirectDraw que representa este controlador para este proceso.</span><span class="sxs-lookup"><span data-stu-id="2e276-144">A DirectDraw object representing this driver has already been created for this process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR \_ EXCEPTION**</span><span class="sxs-lookup"><span data-stu-id="2e276-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-146">Se encontró una excepción al realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="2e276-146">An exception was encountered while performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR \_ EXCLUSIVEMODEALREADYSET**</span><span class="sxs-lookup"><span data-stu-id="2e276-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR\_EXCLUSIVEMODEALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-148">Se intentó establecer el nivel de cooperación cuando ya estaba establecido en exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2e276-148">An attempt was made to set the cooperative level when it was already set to exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ EXPIRÓ**</span><span class="sxs-lookup"><span data-stu-id="2e276-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-150">Los datos han expirado y, por tanto, ya no son válidos.</span><span class="sxs-lookup"><span data-stu-id="2e276-150">The data has expired and is therefore no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR \_ GENÉRICO**</span><span class="sxs-lookup"><span data-stu-id="2e276-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-152">Hay una condición de error indefinido.</span><span class="sxs-lookup"><span data-stu-id="2e276-152">There is an undefined error condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR \_ HEIGHTALIGN**</span><span class="sxs-lookup"><span data-stu-id="2e276-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR\_HEIGHTALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-154">El alto del rectángulo proporcionado no es un múltiplo de la alineación necesaria.</span><span class="sxs-lookup"><span data-stu-id="2e276-154">The height of the provided rectangle is not a multiple of the required alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR \_ HWJUNREADYSET**</span><span class="sxs-lookup"><span data-stu-id="2e276-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR\_HWNDALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-156">Ya se ha establecido el identificador de ventana de nivel cooperativo de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="2e276-156">The DirectDraw cooperative-level window handle has already been set.</span></span> <span data-ttu-id="2e276-157">No se puede restablecer mientras el proceso tiene superficies o paletas creadas.</span><span class="sxs-lookup"><span data-stu-id="2e276-157">It cannot be reset while the process has surfaces or palettes created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR \_ HWNDSUBCLASSED**</span><span class="sxs-lookup"><span data-stu-id="2e276-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR\_HWNDSUBCLASSED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-159">DirectDraw no puede restaurar el estado porque el identificador de ventana de nivel cooperativo de DirectDraw se ha subclasificado.</span><span class="sxs-lookup"><span data-stu-id="2e276-159">DirectDraw is prevented from restoring state because the DirectDraw cooperative-level window handle has been subclassed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR \_ IMPLICITLYCREATED**</span><span class="sxs-lookup"><span data-stu-id="2e276-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR\_IMPLICITLYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-161">La superficie no se puede restaurar porque es una superficie creada implícitamente.</span><span class="sxs-lookup"><span data-stu-id="2e276-161">The surface cannot be restored because it is an implicitly created surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR \_ INCOMPATIBLEPRIMARY**</span><span class="sxs-lookup"><span data-stu-id="2e276-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR\_INCOMPATIBLEPRIMARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-163">La solicitud de creación de la superficie principal no coincide con la superficie principal existente.</span><span class="sxs-lookup"><span data-stu-id="2e276-163">The primary surface creation request does not match the existing primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**INVALIDCAPS de DDERR \_**</span><span class="sxs-lookup"><span data-stu-id="2e276-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR\_INVALIDCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-165">Uno o varios de los bits de funcionalidad pasados a la función de devolución de llamada son incorrectos.</span><span class="sxs-lookup"><span data-stu-id="2e276-165">One or more of the capability bits passed to the callback function are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR \_ INVALIDCLIPLIST**</span><span class="sxs-lookup"><span data-stu-id="2e276-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR\_INVALIDCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-167">DirectDraw no admite la lista de clips proporcionada.</span><span class="sxs-lookup"><span data-stu-id="2e276-167">DirectDraw does not support the provided clip list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR \_ INVALIDDIRECTDRAWGUID**</span><span class="sxs-lookup"><span data-stu-id="2e276-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR\_INVALIDDIRECTDRAWGUID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-169">El identificador único global (GUID) pasado a la [**función DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) no es un identificador de controlador de DirectDraw válido.</span><span class="sxs-lookup"><span data-stu-id="2e276-169">The globally unique identifier (GUID) passed to the [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) function is not a valid DirectDraw driver identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR \_ INVALIDMODE**</span><span class="sxs-lookup"><span data-stu-id="2e276-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR\_INVALIDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-171">DirectDraw no admite el modo solicitado.</span><span class="sxs-lookup"><span data-stu-id="2e276-171">DirectDraw does not support the requested mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR \_ INVALIDOBJECT**</span><span class="sxs-lookup"><span data-stu-id="2e276-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR\_INVALIDOBJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-173">DirectDraw recibió un puntero que era un objeto DirectDraw no válido.</span><span class="sxs-lookup"><span data-stu-id="2e276-173">DirectDraw received a pointer that was an invalid DirectDraw object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR \_ INVALIDPARAMS**</span><span class="sxs-lookup"><span data-stu-id="2e276-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR\_INVALIDPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-175">Uno o varios de los parámetros pasados al método son incorrectos.</span><span class="sxs-lookup"><span data-stu-id="2e276-175">One or more of the parameters passed to the method are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR \_ INVALIDPIXELFORMAT**</span><span class="sxs-lookup"><span data-stu-id="2e276-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR\_INVALIDPIXELFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-177">El formato de píxel no era válido como se especificó.</span><span class="sxs-lookup"><span data-stu-id="2e276-177">The pixel format was invalid as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR \_ INVALIDPOSITION**</span><span class="sxs-lookup"><span data-stu-id="2e276-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR\_INVALIDPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-179">La posición de la superposición en el destino ya no es válida.</span><span class="sxs-lookup"><span data-stu-id="2e276-179">The position of the overlay on the destination is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR \_ INVALIDRECT**</span><span class="sxs-lookup"><span data-stu-id="2e276-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR\_INVALIDRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-181">El rectángulo proporcionado no era válido.</span><span class="sxs-lookup"><span data-stu-id="2e276-181">The provided rectangle was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR \_ INVALIDSTREAM**</span><span class="sxs-lookup"><span data-stu-id="2e276-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR\_INVALIDSTREAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-183">La secuencia especificada contiene datos no válidos.</span><span class="sxs-lookup"><span data-stu-id="2e276-183">The specified stream contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR \_ INVALIDSURFACETYPE**</span><span class="sxs-lookup"><span data-stu-id="2e276-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR\_INVALIDSURFACETYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-185">La superficie era del tipo incorrecto.</span><span class="sxs-lookup"><span data-stu-id="2e276-185">The surface was of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR \_ LOCKEDSURFACES**</span><span class="sxs-lookup"><span data-stu-id="2e276-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR\_LOCKEDSURFACES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-187">Una o varias superficies están bloqueadas, lo que provoca el error de la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="2e276-187">One or more surfaces are locked, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="2e276-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR\_MOREDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-189">Hay más datos disponibles de los que puede contener el tamaño de búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="2e276-189">There is more data available than the specified buffer size can hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**NEWMODE de DDERR \_**</span><span class="sxs-lookup"><span data-stu-id="2e276-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR\_NEWMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-191">Novedad de DirectX 7.0.</span><span class="sxs-lookup"><span data-stu-id="2e276-191">New for DirectX 7.0.</span></span> <span data-ttu-id="2e276-192">Cuando se llama a [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) con la marca DDSMT ISTESTREQUIRED, podría devolver este valor para indicar que algunas o todas las resoluciones pueden y deben \_ probarse.</span><span class="sxs-lookup"><span data-stu-id="2e276-192">When [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) is called with the DDSMT\_ISTESTREQUIRED flag, it might return this value to denote that some or all of the resolutions can and should be tested.</span></span> <span data-ttu-id="2e276-193">[**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) devuelve este valor para indicar que la prueba ha cambiado a un nuevo modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="2e276-193">[**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) returns this value to indicate that the test has switched to a new display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR \_ NO3D**</span><span class="sxs-lookup"><span data-stu-id="2e276-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR\_NO3D**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-195">No hay hardware 3D ni emulación presente.</span><span class="sxs-lookup"><span data-stu-id="2e276-195">No 3-D hardware or emulation is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR \_ NOALPHAHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR\_NOALPHAHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-197">No hay ningún hardware de aceleración alfa presente o disponible, lo que provoca el error de la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="2e276-197">No alpha-acceleration hardware is present or available, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR \_ NOBLTHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR\_NOBLTHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-199">No hay ningún bloque de bits que transfiera hardware.</span><span class="sxs-lookup"><span data-stu-id="2e276-199">No bit block transferring hardware is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOCLIPLIST**</span><span class="sxs-lookup"><span data-stu-id="2e276-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR\_NOCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-201">No hay ninguna lista de clips disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-201">No clip list is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR \_ NOCLIPPERATTACHED**</span><span class="sxs-lookup"><span data-stu-id="2e276-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR\_NOCLIPPERATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-203">No hay ningún objeto DirectDrawClipper asociado al objeto de superficie.</span><span class="sxs-lookup"><span data-stu-id="2e276-203">No DirectDrawClipper object is attached to the surface object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR \_ NOCOLORCONVHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR\_NOCOLORCONVHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-205">No hay ningún hardware de conversión de colores presente o disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-205">No color-conversion hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR \_ NOCOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="2e276-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR\_NOCOLORKEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-207">La superficie no tiene actualmente una clave de color.</span><span class="sxs-lookup"><span data-stu-id="2e276-207">The surface does not currently have a color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR \_ NOCOLORKEYHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR\_NOCOLORKEYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-209">No hay compatibilidad de hardware con la clave de color de destino.</span><span class="sxs-lookup"><span data-stu-id="2e276-209">There is no hardware support for the destination color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR \_ NOCOOPERATIVELEVELSET**</span><span class="sxs-lookup"><span data-stu-id="2e276-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR\_NOCOOPERATIVELEVELSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-211">Se llamó a una función create [**sin el método IDirectDraw7::SetCooperativeLevel.**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel)</span><span class="sxs-lookup"><span data-stu-id="2e276-211">A create function was called without the [**IDirectDraw7::SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR \_ NODC**</span><span class="sxs-lookup"><span data-stu-id="2e276-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR\_NODC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-213">No se ha creado ningún contexto de dispositivo (DC) para esta superficie.</span><span class="sxs-lookup"><span data-stu-id="2e276-213">No device context (DC) has ever been created for this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR \_ NODDROPSHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR\_NODDROPSHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-215">No hay ningún hardware de operación de trama (ROP) de DirectDraw disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-215">No DirectDraw raster-operation (ROP) hardware is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR \_ NODIRECTDRAWHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR\_NODIRECTDRAWHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-217">No es posible crear objetos DirectDraw solo de hardware; el controlador no admite ningún hardware.</span><span class="sxs-lookup"><span data-stu-id="2e276-217">Hardware-only DirectDraw object creation is not possible; the driver does not support any hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR \_ NODIRECTDRAWSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="2e276-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR\_NODIRECTDRAWSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-219">La compatibilidad con DirectDraw no es posible con el controlador de pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="2e276-219">DirectDraw support is not possible with the current display driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR \_ NODRIVERSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="2e276-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR\_NODRIVERSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-221">Novedad de DirectX 7.0.</span><span class="sxs-lookup"><span data-stu-id="2e276-221">New for DirectX 7.0.</span></span> <span data-ttu-id="2e276-222">Las pruebas no pueden continuar porque el controlador del adaptador de pantalla no enumera las tasas de actualización.</span><span class="sxs-lookup"><span data-stu-id="2e276-222">Testing cannot proceed because the display adapter driver does not enumerate refresh rates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR \_ NOEMULATION**</span><span class="sxs-lookup"><span data-stu-id="2e276-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR\_NOEMULATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-224">La emulación de software no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-224">Software emulation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR \_ NOEXCLUSIVEMODE**</span><span class="sxs-lookup"><span data-stu-id="2e276-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR\_NOEXCLUSIVEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-226">La operación requiere que la aplicación tenga el modo exclusivo, pero la aplicación no tiene modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2e276-226">The operation requires the application to have exclusive mode, but the application does not have exclusive mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR \_ NOFLIPHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR\_NOFLIPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-228">No se admite la volteo de superficies visibles.</span><span class="sxs-lookup"><span data-stu-id="2e276-228">Flipping visible surfaces is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR \_ NOFOCUSWINDOW**</span><span class="sxs-lookup"><span data-stu-id="2e276-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR\_NOFOCUSWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-230">Se intentó crear o establecer una ventana del dispositivo sin establecer primero la ventana de foco.</span><span class="sxs-lookup"><span data-stu-id="2e276-230">An attempt was made to create or set a device window without first setting the focus window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR \_ NOGDI**</span><span class="sxs-lookup"><span data-stu-id="2e276-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR\_NOGDI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-232">No hay GDI presente.</span><span class="sxs-lookup"><span data-stu-id="2e276-232">No GDI is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOHWND**</span><span class="sxs-lookup"><span data-stu-id="2e276-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR\_NOHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-234">La notificación de Clipper requiere un identificador de ventana o no se ha establecido previamente ningún identificador de ventana como identificador de ventana de nivel cooperativo.</span><span class="sxs-lookup"><span data-stu-id="2e276-234">Clipper notification requires a window handle, or no window handle has been previously set as the cooperative level window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR \_ NOMIPMAPHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR\_NOMIPMAPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-236">No hay ningún hardware de asignación de textura compatible con mipmap presente o disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-236">No mipmap-capable texture mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR \_ NOMIRRORHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR\_NOMIRRORHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-238">No hay ningún hardware de creación de reflejo presente o disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-238">No mirroring hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR \_ NOMONITORINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="2e276-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR\_NOMONITORINFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-240">Novedad de DirectX 7.0.</span><span class="sxs-lookup"><span data-stu-id="2e276-240">New for DirectX 7.0.</span></span> <span data-ttu-id="2e276-241">Las pruebas no pueden continuar porque el monitor no tiene datos EDID asociados.</span><span class="sxs-lookup"><span data-stu-id="2e276-241">Testing cannot proceed because the monitor has no associated EDID data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR \_ NONONLOCALVIDMEM**</span><span class="sxs-lookup"><span data-stu-id="2e276-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR\_NONONLOCALVIDMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-243">Se intentó asignar memoria de vídeo no local desde un dispositivo que no admite memoria de vídeo no local.</span><span class="sxs-lookup"><span data-stu-id="2e276-243">An attempt was made to allocate nonlocal video memory from a device that does not support nonlocal video memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR \_ NOOPTIMIZEHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR\_NOOPTIMIZEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-245">El dispositivo no admite superficies optimizadas.</span><span class="sxs-lookup"><span data-stu-id="2e276-245">The device does not support optimized surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR \_ NOOVERLAYDEST**</span><span class="sxs-lookup"><span data-stu-id="2e276-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR\_NOOVERLAYDEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-247">Se llama al método [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) en una superposición en la que no se ha llamado al método [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) para establecer como destino.</span><span class="sxs-lookup"><span data-stu-id="2e276-247">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method is called on an overlay that the [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) method has not been called on to establish as a destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR \_ NOOVERLAYHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR\_NOOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-249">No hay ningún hardware de superposición presente o disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-249">No overlay hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR \_ NOPALETTEATTACHED**</span><span class="sxs-lookup"><span data-stu-id="2e276-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR\_NOPALETTEATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-251">No hay ningún objeto de paleta asociado a esta superficie.</span><span class="sxs-lookup"><span data-stu-id="2e276-251">No palette object is attached to this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR \_ NOPALETTEHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR\_NOPALETTEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-253">No hay compatibilidad con hardware para paletas de 16 o 256 colores.</span><span class="sxs-lookup"><span data-stu-id="2e276-253">There is no hardware support for 16- or 256-color palettes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR \_ NORASTEROPHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR\_NORASTEROPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-255">No hay ningún hardware de operación de trama adecuado presente o disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-255">No appropriate raster-operation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR \_ NOROTATIONHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR\_NOROTATIONHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-257">No hay hardware de rotación presente ni disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-257">No rotation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR \_ NOSTEREOHARDWARE**</span><span class="sxs-lookup"><span data-stu-id="2e276-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR\_NOSTEREOHARDWARE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-259">No hay ningún hardware estéreo presente o disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-259">There is no stereo hardware present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR \_ NOSTRETCHHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR\_NOSTRETCHHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-261">No hay compatibilidad con hardware para el stretching.</span><span class="sxs-lookup"><span data-stu-id="2e276-261">There is no hardware support for stretching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR \_ NOSURFACELEFT**</span><span class="sxs-lookup"><span data-stu-id="2e276-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR\_NOSURFACELEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-263">No hay ningún hardware que admita superficies estéreo.</span><span class="sxs-lookup"><span data-stu-id="2e276-263">There is no hardware present that supports stereo surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR \_ NOT4BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="2e276-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR\_NOT4BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-265">El objeto DirectDrawSurface no usa una paleta de colores de 4 bits y la operación solicitada requiere una paleta de colores de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="2e276-265">The DirectDrawSurface object is not using a 4-bit color palette, and the requested operation requires a 4-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR \_ NOT4BITCOLORINDEX**</span><span class="sxs-lookup"><span data-stu-id="2e276-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR\_NOT4BITCOLORINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-267">El objeto DirectDrawSurface no usa una paleta de índices de color de 4 bits y la operación solicitada requiere una paleta de índices de color de 4 bits.</span><span class="sxs-lookup"><span data-stu-id="2e276-267">The DirectDrawSurface object is not using a 4-bit color index palette, and the requested operation requires a 4-bit color index palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR \_ NOT8BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="2e276-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR\_NOT8BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-269">El objeto DirectDrawSurface no usa una paleta de colores de 8 bits y la operación solicitada requiere una paleta de colores de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="2e276-269">The DirectDrawSurface object is not using an 8-bit color palette, and the requested operation requires an 8-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR \_ NOTAOVERLAYSURFACE**</span><span class="sxs-lookup"><span data-stu-id="2e276-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR\_NOTAOVERLAYSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-271">Se llama a un componente de superposición para una superficie no superpuesta.</span><span class="sxs-lookup"><span data-stu-id="2e276-271">An overlay component is called for a nonoverlay surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR \_ NOTEXTUREHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR\_NOTEXTUREHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-273">La operación no se puede llevar a cabo porque no hay ningún hardware de asignación de texturas presente o disponible.</span><span class="sxs-lookup"><span data-stu-id="2e276-273">The operation cannot be carried out because no texture-mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR \_ NOTFLIPPABLE**</span><span class="sxs-lookup"><span data-stu-id="2e276-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR\_NOTFLIPPABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-275">Se intentó voltear una superficie que no se puede voltear.</span><span class="sxs-lookup"><span data-stu-id="2e276-275">An attempt was made to flip a surface that cannot be flipped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR \_ NOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="2e276-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-277">No se encontró el elemento solicitado.</span><span class="sxs-lookup"><span data-stu-id="2e276-277">The requested item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR \_ NOTINITIALIZED**</span><span class="sxs-lookup"><span data-stu-id="2e276-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR\_NOTINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-279">Se intentó llamar a un método de interfaz de un objeto DirectDraw creado por [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) antes de inicializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="2e276-279">An attempt was made to call an interface method of a DirectDraw object created by [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) before the object was initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR \_ NO CARGADO**</span><span class="sxs-lookup"><span data-stu-id="2e276-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR\_NOTLOADED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-281">La superficie es una superficie optimizada, pero aún no se le ha asignado memoria.</span><span class="sxs-lookup"><span data-stu-id="2e276-281">The surface is an optimized surface, but it has not yet been allocated any memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR \_ NOTLOCKED**</span><span class="sxs-lookup"><span data-stu-id="2e276-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR\_NOTLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-283">Se intentó desbloquear una superficie que no estaba bloqueada.</span><span class="sxs-lookup"><span data-stu-id="2e276-283">An attempt was made to unlock a surface that was not locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR \_ NOTPAGELOCKED**</span><span class="sxs-lookup"><span data-stu-id="2e276-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR\_NOTPAGELOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-285">Se intentó desbloquear una superficie sin bloqueos de página pendientes.</span><span class="sxs-lookup"><span data-stu-id="2e276-285">An attempt was made to page-unlock a surface with no outstanding page locks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR \_ NOTPALETTIZED**</span><span class="sxs-lookup"><span data-stu-id="2e276-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR\_NOTPALETTIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-287">La superficie que se usa no es una superficie basada en paleta.</span><span class="sxs-lookup"><span data-stu-id="2e276-287">The surface being used is not a palette-based surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR \_ NOVSYNCHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR\_NOVSYNCHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-289">No hay compatibilidad de hardware para las operaciones sincronizadas verticales en blanco.</span><span class="sxs-lookup"><span data-stu-id="2e276-289">There is no hardware support for vertical blank synchronized operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR \_ NOZBUFFERHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR\_NOZBUFFERHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-291">La operación para crear un búfer z en la memoria para mostrar o para realizar una transferencia de bloque de bits (bitblt), mediante un búfer z no se puede llevar a cabo porque no hay compatibilidad de hardware con los búferes z.</span><span class="sxs-lookup"><span data-stu-id="2e276-291">The operation to create a z-buffer in display memory or to perform a bit block transfer (bitblt), using a z-buffer cannot be carried out because there is no hardware support for z-buffers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR \_ NOZOVERLAYHW**</span><span class="sxs-lookup"><span data-stu-id="2e276-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR\_NOZOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-293">Las superficies superpuestas no se pueden superponer en capas z, en función del orden z porque el hardware no admite el orden z de las superposiciones.</span><span class="sxs-lookup"><span data-stu-id="2e276-293">The overlay surfaces cannot be z-layered, based on the z-order because the hardware does not support z-ordering of overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**OUTOFCAPS de DDERR \_**</span><span class="sxs-lookup"><span data-stu-id="2e276-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR\_OUTOFCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-295">Ya se ha asignado el hardware necesario para la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="2e276-295">The hardware needed for the requested operation has already been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="2e276-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-297">DirectDraw no tiene suficiente memoria para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="2e276-297">DirectDraw does not have enough memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR \_ OUTOFVIDEOMEMORY**</span><span class="sxs-lookup"><span data-stu-id="2e276-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR\_OUTOFVIDEOMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-299">DirectDraw no tiene suficiente memoria de presentación para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="2e276-299">DirectDraw does not have enough display memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR \_ OVERLAPPINGRECTS**</span><span class="sxs-lookup"><span data-stu-id="2e276-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR\_OVERLAPPINGRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-301">Los rectángulos de origen y destino están en la misma superficie y se superponen entre sí.</span><span class="sxs-lookup"><span data-stu-id="2e276-301">The source and destination rectangles are on the same surface and overlap each other.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**SUPERPOSICIÓN DE \_ DDERRCANTCLIP**</span><span class="sxs-lookup"><span data-stu-id="2e276-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR\_OVERLAYCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-303">El hardware no admite superposiciones recortadas.</span><span class="sxs-lookup"><span data-stu-id="2e276-303">The hardware does not support clipped overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR \_ OVERLAYCOLORKEYONLYONEACTIVE**</span><span class="sxs-lookup"><span data-stu-id="2e276-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR\_OVERLAYCOLORKEYONLYONEACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-305">Se intentó tener más de una clave de color activa en una superposición.</span><span class="sxs-lookup"><span data-stu-id="2e276-305">An attempt was made to have more than one color key active on an overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**SUPERPOSICIÓN DE \_ DDERRNOTVISIBLE**</span><span class="sxs-lookup"><span data-stu-id="2e276-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR\_OVERLAYNOTVISIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-307">Se [**llamó al método IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) en una superposición oculta.</span><span class="sxs-lookup"><span data-stu-id="2e276-307">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method was called on a hidden overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**PALETA DE \_ DDERRBUSY**</span><span class="sxs-lookup"><span data-stu-id="2e276-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR\_PALETTEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-309">Se rechaza el acceso a esta paleta porque otro subproceso bloquea la paleta.</span><span class="sxs-lookup"><span data-stu-id="2e276-309">Access to this palette is refused because the palette is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR \_ PRIMARYSURFACEALREADYEXISTS**</span><span class="sxs-lookup"><span data-stu-id="2e276-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR\_PRIMARYSURFACEALREADYEXISTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-311">Este proceso ya ha creado una superficie principal.</span><span class="sxs-lookup"><span data-stu-id="2e276-311">This process has already created a primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**REGIÓN DE \_ DDERRTOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="2e276-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR\_REGIONTOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-313">La región que se pasa [**al método IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) es demasiado pequeña.</span><span class="sxs-lookup"><span data-stu-id="2e276-313">The region passed to the [**IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) method is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR \_ SURFACEALREADYATTACHED**</span><span class="sxs-lookup"><span data-stu-id="2e276-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR\_SURFACEALREADYATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-315">Se intentó adjuntar una superficie a otra superficie a la que ya está asociada.</span><span class="sxs-lookup"><span data-stu-id="2e276-315">An attempt was made to attach a surface to another surface to which it is already attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR \_ SURFACEALREADYDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="2e276-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR\_SURFACEALREADYDEPENDENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-317">Se intentó convertir una superficie en una dependencia de otra superficie de la que ya depende.</span><span class="sxs-lookup"><span data-stu-id="2e276-317">An attempt was made to make a surface a dependency of another surface on which it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR \_ SURFACEBUSY**</span><span class="sxs-lookup"><span data-stu-id="2e276-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR\_SURFACEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-319">Se rechaza el acceso a la superficie porque otro subproceso bloquea la superficie.</span><span class="sxs-lookup"><span data-stu-id="2e276-319">Access to the surface is refused because the surface is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR \_ SURFACEISOBSCURED**</span><span class="sxs-lookup"><span data-stu-id="2e276-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR\_SURFACEISOBSCURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-321">Se rechaza el acceso a la superficie porque la superficie está oculta.</span><span class="sxs-lookup"><span data-stu-id="2e276-321">Access to the surface is refused because the surface is obscured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR \_ SURFACELOST**</span><span class="sxs-lookup"><span data-stu-id="2e276-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR\_SURFACELOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-323">Se rechaza el acceso a la superficie porque la memoria de la superficie ha desaparecido.</span><span class="sxs-lookup"><span data-stu-id="2e276-323">Access to the surface is refused because the surface memory is gone.</span></span> <span data-ttu-id="2e276-324">Llame al [**método IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) en esta superficie para restaurar la memoria asociada a él.</span><span class="sxs-lookup"><span data-stu-id="2e276-324">Call the [**IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) method on this surface to restore the memory associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR \_ SURFACENOTATTACHED**</span><span class="sxs-lookup"><span data-stu-id="2e276-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR\_SURFACENOTATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-326">La superficie solicitada no está adjunta.</span><span class="sxs-lookup"><span data-stu-id="2e276-326">The requested surface is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR \_ TESTFINISHED**</span><span class="sxs-lookup"><span data-stu-id="2e276-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR\_TESTFINISHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-328">Novedad de DirectX 7.0.</span><span class="sxs-lookup"><span data-stu-id="2e276-328">New for DirectX 7.0.</span></span> <span data-ttu-id="2e276-329">Cuando lo devuelve el método [**IDirectDraw7::StartModeTest,**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) este valor significa que no se podría iniciar ninguna prueba porque todas las resoluciones elegidas para las pruebas ya tienen información de frecuencia de actualización en el Registro.</span><span class="sxs-lookup"><span data-stu-id="2e276-329">When returned by the [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) method, this value means that no test could be initiated because all the resolutions chosen for testing already have refresh rate information in the registry.</span></span> <span data-ttu-id="2e276-330">Cuando [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)lo devuelve, el valor significa que DirectDraw ha completado una prueba de frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="2e276-330">When returned by [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), the value means that DirectDraw has completed a refresh rate test.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR \_ TOOBIIGHT**</span><span class="sxs-lookup"><span data-stu-id="2e276-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR\_TOOBIGHEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-332">El alto solicitado por DirectDraw es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="2e276-332">The height requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR \_ TOOBIGSIZE**</span><span class="sxs-lookup"><span data-stu-id="2e276-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR\_TOOBIGSIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-334">El tamaño solicitado por DirectDraw es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="2e276-334">The size requested by DirectDraw is too large.</span></span> <span data-ttu-id="2e276-335">Sin embargo, el alto y el ancho individuales son tamaños válidos.</span><span class="sxs-lookup"><span data-stu-id="2e276-335">However, the individual height and width are valid sizes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR \_ TOOBIGWIDTH**</span><span class="sxs-lookup"><span data-stu-id="2e276-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR\_TOOBIGWIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-337">El ancho solicitado por DirectDraw es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="2e276-337">The width requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR \_ NO COMPATIBLE**</span><span class="sxs-lookup"><span data-stu-id="2e276-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-339">La operación no es compatible.</span><span class="sxs-lookup"><span data-stu-id="2e276-339">The operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR \_ UNSUPPORTEDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="2e276-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR\_UNSUPPORTEDFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-341">DirectDraw no admite el formato de píxel solicitado.</span><span class="sxs-lookup"><span data-stu-id="2e276-341">The pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR \_ UNSUPPORTEDMASK**</span><span class="sxs-lookup"><span data-stu-id="2e276-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR\_UNSUPPORTEDMASK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-343">DirectDraw no admite la máscara de bits en el formato de píxel solicitado.</span><span class="sxs-lookup"><span data-stu-id="2e276-343">The bitmask in the pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR \_ UNSUPPORTEDMODE**</span><span class="sxs-lookup"><span data-stu-id="2e276-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR\_UNSUPPORTEDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-345">La pantalla está actualmente en modo no compatible.</span><span class="sxs-lookup"><span data-stu-id="2e276-345">The display is currently in an unsupported mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR \_ VERTICALBLANKINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="2e276-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR\_VERTICALBLANKINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-347">Hay un espacio en blanco vertical en curso.</span><span class="sxs-lookup"><span data-stu-id="2e276-347">A vertical blank is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**VÍDEO DE \_ DDERRNOTACTIVE**</span><span class="sxs-lookup"><span data-stu-id="2e276-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR\_VIDEONOTACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-349">El puerto de vídeo no está activo.</span><span class="sxs-lookup"><span data-stu-id="2e276-349">The video port is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR \_ WASSTFUNDDRAWING**</span><span class="sxs-lookup"><span data-stu-id="2e276-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR\_WASSTILLDRAWING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-351">La operación bitblt anterior que transfiere información hacia o desde esta superficie está incompleta.</span><span class="sxs-lookup"><span data-stu-id="2e276-351">The previous bitblt operation that is transferring information to or from this surface is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR \_ WRONGMODE**</span><span class="sxs-lookup"><span data-stu-id="2e276-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR\_WRONGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-353">Esta superficie no se puede restaurar porque se creó en un modo diferente.</span><span class="sxs-lookup"><span data-stu-id="2e276-353">This surface cannot be restored because it was created in a different mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2e276-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR \_ XALIGN**</span><span class="sxs-lookup"><span data-stu-id="2e276-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR\_XALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2e276-355">El rectángulo proporcionado no estaba alineado horizontalmente en un límite necesario.</span><span class="sxs-lookup"><span data-stu-id="2e276-355">The provided rectangle was not horizontally aligned on a required boundary.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e276-356">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e276-356">Requirements</span></span>



| <span data-ttu-id="2e276-357">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e276-357">Requirement</span></span> | <span data-ttu-id="2e276-358">Value</span><span class="sxs-lookup"><span data-stu-id="2e276-358">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e276-359">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e276-359">Header</span></span><br/> | <dl> <span data-ttu-id="2e276-360"><dt>Ddraw.h</dt></span><span class="sxs-lookup"><span data-stu-id="2e276-360"><dt>Ddraw.h</dt></span></span> </dl> |



 

