---
description: Las API de prevención de pérdida de datos (DLP) del punto de conexión permiten a las aplicaciones notificar al sistema operativo antes y después de ciertas operaciones, como abrir o guardar un archivo.
title: Prevención de pérdida de datos de punto de conexión
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 867e059e0accfc1208c96394c3065d69cf9f576c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495831"
---
# <a name="endpoint-data-loss-prevention"></a><span data-ttu-id="7167f-103">Prevención de pérdida de datos de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="7167f-103">Endpoint data loss prevention</span></span>

<span data-ttu-id="7167f-104">Windows 10 implementa mecanismos que ayudan a evitar la pérdida de datos de archivos confidenciales.</span><span class="sxs-lookup"><span data-stu-id="7167f-104">Windows 10 implements mechanisms that help to prevent data loss for sensitive files.</span></span> <span data-ttu-id="7167f-105">Las API de prevención de pérdida de datos (DLP) del punto de conexión permiten a las aplicaciones notificar al sistema operativo antes y después de ciertas operaciones, como abrir o guardar un archivo.</span><span class="sxs-lookup"><span data-stu-id="7167f-105">The endpoint data loss prevention (DLP) APIs allow applications to notify the OS before and after certain operations, such as opening or saving a file.</span></span> <span data-ttu-id="7167f-106">Estas notificaciones sirven como "sugerencias" que permiten al sistema optimizar las operaciones de pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="7167f-106">These notifications serve as "hints" that allow the system to optimize data loss operations.</span></span>

## <a name="location-of-the-dlp-dll"></a><span data-ttu-id="7167f-107">Ubicación del archivo DLL dlp</span><span class="sxs-lookup"><span data-stu-id="7167f-107">Location of the DLP dll</span></span>

<span data-ttu-id="7167f-108">Puesto que el archivo DLL DLP del punto de conexión no está incluido con el Windows SDK, las aplicaciones detendrán que cargar el archivo DLL manualmente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7167f-108">Since the endpoint DLP dll isn't bundled with the Windows SDK, applications will need to load the dll manually at runtime.</span></span> <span data-ttu-id="7167f-109">La ruta de acceso a la ubicación del archivo DLL se almacena en el Registro.</span><span class="sxs-lookup"><span data-stu-id="7167f-109">The path to the dll location is stored in the registry.</span></span> <span data-ttu-id="7167f-110">En la tabla siguiente se enumeran las claves y los valores del Registro que almacenan esta información.</span><span class="sxs-lookup"><span data-stu-id="7167f-110">The following table lists the registry keys and values that store this information.</span></span> <span data-ttu-id="7167f-111">Estas rutas de acceso se definen como constantes en la lista de código endpointdlp.h de ejemplo que se proporciona a continuación para mayor comodidad para los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="7167f-111">These paths are defined as constants in the sample endpointdlp.h code listing provided below as a convenience for developers.</span></span>

| <span data-ttu-id="7167f-112">Constante</span><span class="sxs-lookup"><span data-stu-id="7167f-112">Constant</span></span> | <span data-ttu-id="7167f-113">Value</span><span class="sxs-lookup"><span data-stu-id="7167f-113">Value</span></span> | <span data-ttu-id="7167f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7167f-114">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="7167f-115">ENDPOINTDLP_DLL_NAME</span><span class="sxs-lookup"><span data-stu-id="7167f-115">ENDPOINTDLP_DLL_NAME</span></span> | <span data-ttu-id="7167f-116">"EndpointDlp.dll"</span><span class="sxs-lookup"><span data-stu-id="7167f-116">"EndpointDlp.dll"</span></span> | <span data-ttu-id="7167f-117">El nombre del archivo DLL dlp de punto de conexión que proporciona la API.</span><span class="sxs-lookup"><span data-stu-id="7167f-117">The name of the Endpoint DLP DLL that provides the API</span></span> |
| <span data-ttu-id="7167f-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="7167f-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> | <span data-ttu-id="7167f-119">"SOFTWARE \\ Microsoft \\ Windows Defender"</span><span class="sxs-lookup"><span data-stu-id="7167f-119">"SOFTWARE\\Microsoft\\Windows Defender"</span></span> | <span data-ttu-id="7167f-120">Windows Defender clave del Registro en HKLM donde se almacenan algunos valores de DLP de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="7167f-120">Windows Defender registry key under HKLM where some Endpoint DLP settings are stored</span></span> |
| <span data-ttu-id="7167f-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span><span class="sxs-lookup"><span data-stu-id="7167f-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span></span> | <span data-ttu-id="7167f-122">Valor de ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="7167f-122">Value of ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |  <span data-ttu-id="7167f-123">La ruta de acceso del Registro bajo la clave HKLM desde la que EndpointDlp.dll la ubicación de instalación</span><span class="sxs-lookup"><span data-stu-id="7167f-123">The registry path under HKLM key from which the EndpointDlp.dll install location can be obtained</span></span> |
| <span data-ttu-id="7167f-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="7167f-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span></span> | <span data-ttu-id="7167f-125">"InstallLocation"</span><span class="sxs-lookup"><span data-stu-id="7167f-125">"InstallLocation"</span></span> | <span data-ttu-id="7167f-126">Valor del Registro en ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY donde se almacena la EndpointDlp.dll de instalación</span><span class="sxs-lookup"><span data-stu-id="7167f-126">The registry value under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in which the EndpointDlp.dll install location is stored</span></span> |
| <span data-ttu-id="7167f-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span><span class="sxs-lookup"><span data-stu-id="7167f-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span></span> | <span data-ttu-id="7167f-128">"x86"</span><span class="sxs-lookup"><span data-stu-id="7167f-128">"x86"</span></span> | <span data-ttu-id="7167f-129">En plataformas x64, concatene este directorio para obtener la versión x86 de EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="7167f-129">On x64 platforms, concatenate this directory to obtain the x86 version of EndpointDlp.dll</span></span> |

## <a name="check-if-endpoint-dlp-is-enabled"></a><span data-ttu-id="7167f-130">Comprobación de si el punto de conexión DLP está habilitado</span><span class="sxs-lookup"><span data-stu-id="7167f-130">Check if endpoint DLP is enabled</span></span>

<span data-ttu-id="7167f-131">Para determinar si dlp del punto de conexión está habilitado en el sistema, compruebe el siguiente valor de clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="7167f-131">To determine if endpoint DLP is enabled on the system, check the following registry key value.</span></span> 

| <span data-ttu-id="7167f-132">Constante</span><span class="sxs-lookup"><span data-stu-id="7167f-132">Constant</span></span> | <span data-ttu-id="7167f-133">Value</span><span class="sxs-lookup"><span data-stu-id="7167f-133">Value</span></span> | <span data-ttu-id="7167f-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="7167f-134">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="7167f-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span><span class="sxs-lookup"><span data-stu-id="7167f-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span></span> |  <span data-ttu-id="7167f-136">" \\ Características"</span><span class="sxs-lookup"><span data-stu-id="7167f-136">"\\Features"</span></span> | <span data-ttu-id="7167f-137">Ruta de acceso a la clave de marca habilitada para DLP de punto de conexión en (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="7167f-137">The path to the Endpoint DLP enabled flag key under (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |
| <span data-ttu-id="7167f-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="7167f-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span></span> | <span data-ttu-id="7167f-139">"SenseDlpEnabled"</span><span class="sxs-lookup"><span data-stu-id="7167f-139">"SenseDlpEnabled"</span></span> | <span data-ttu-id="7167f-140">Valor del Registro en ENDPOINTDLP_ENABLED_FLAG_REGKEY que contiene la clave del Registro de marca habilitada para DLP</span><span class="sxs-lookup"><span data-stu-id="7167f-140">The registry value under ENDPOINTDLP_ENABLED_FLAG_REGKEY containing the DLP enabled flag registry key</span></span>

## <a name="endpoint-dlp-apis"></a><span data-ttu-id="7167f-141">API DLP de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="7167f-141">Endpoint DLP APIs</span></span>

<span data-ttu-id="7167f-142">En las tablas siguientes se muestran las API proporcionadas por el archivo DLL DLP del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="7167f-142">The following tables list the APIs provided by the endpoint DLP dll.</span></span>

### <a name="initialization-and-versioning"></a><span data-ttu-id="7167f-143">Inicialización y control de versiones</span><span class="sxs-lookup"><span data-stu-id="7167f-143">Initialization and versioning</span></span>

| <span data-ttu-id="7167f-144">API</span><span class="sxs-lookup"><span data-stu-id="7167f-144">API</span></span> | <span data-ttu-id="7167f-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="7167f-145">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="7167f-146">DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="7167f-146">DlpInitializeEnforcementMode</span></span>](endpointdlp-dlpinitializeenforcementmode.md)                       | <span data-ttu-id="7167f-147">Notifica al sistema los modos de cumplimiento deseados para un conjunto de operaciones de prevención de pérdida de datos (DLP) de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="7167f-147">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>                                  |
| [<span data-ttu-id="7167f-148">DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="7167f-148">DlpGetEnforcementApiVersion</span></span>](endpointdlp-dlpgetenforcementapiversion.md)                       | <span data-ttu-id="7167f-149">Recupera la versión de la API de prevención de pérdida de datos (DLP) del punto de conexión en el dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="7167f-149">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>                                  |


### <a name="document-operations"></a><span data-ttu-id="7167f-150">Operaciones de documento</span><span class="sxs-lookup"><span data-stu-id="7167f-150">Document operations</span></span>

| <span data-ttu-id="7167f-151">API</span><span class="sxs-lookup"><span data-stu-id="7167f-151">API</span></span> | <span data-ttu-id="7167f-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="7167f-152">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="7167f-153">DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="7167f-153">DlpNotifyPreOpenDocument</span></span>](endpointdlp-dlpnotifypreopendocument.md) | <span data-ttu-id="7167f-154">Proporciona al sistema información sobre un documento antes de iniciar la operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="7167f-154">Provides the system with information about a document before the open operation is initiated.</span></span> |
| [<span data-ttu-id="7167f-155">DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="7167f-155">DlpNotifyPostOpenDocument</span></span>](endpointdlp-dlpnotifypostopendocument.md) | <span data-ttu-id="7167f-156">Proporciona al sistema información sobre un documento una vez completada la operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="7167f-156">Provides the system with information about a document after the open operation is completed.</span></span>  |
| [<span data-ttu-id="7167f-157">DlpNotifyCloseDocument</span><span class="sxs-lookup"><span data-stu-id="7167f-157">DlpNotifyCloseDocument</span></span>](endpointdlp-dlpnotifyclosedocument.md)                       | <span data-ttu-id="7167f-158">Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del documento.</span><span class="sxs-lookup"><span data-stu-id="7167f-158">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |
| [<span data-ttu-id="7167f-159">DlpNotifyPreOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="7167f-159">DlpNotifyPreOpenDocumentFile</span></span>](endpointdlp-dlpnotifypreopendocumentfile.md)                         | <span data-ttu-id="7167f-160">Proporciona al sistema información sobre un documento antes de iniciar la operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="7167f-160">Provides the system with information about a document before the open operation is initiated.</span></span>  |
| [<span data-ttu-id="7167f-161">DlpNotifyPostOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="7167f-161">DlpNotifyPostOpenDocumentFile</span></span>](endpointdlp-dlpnotifypostopendocumentfile.md)                       | <span data-ttu-id="7167f-162">Proporciona al sistema información sobre un documento una vez completada la operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="7167f-162">Provides the system with information about a document after the open operation is completed.</span></span>                                  |
| [<span data-ttu-id="7167f-163">DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="7167f-163">DlpNotifyCloseDocumentFile</span></span>](endpointdlp-dlpnotifyclosedocumentfile.md)                       | <span data-ttu-id="7167f-164">Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del documento.</span><span class="sxs-lookup"><span data-stu-id="7167f-164">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |

### <a name="save-as-operations"></a><span data-ttu-id="7167f-165">Guardar como operaciones</span><span class="sxs-lookup"><span data-stu-id="7167f-165">Save as operations</span></span>
| <span data-ttu-id="7167f-166">API</span><span class="sxs-lookup"><span data-stu-id="7167f-166">API</span></span> | <span data-ttu-id="7167f-167">Descripción</span><span class="sxs-lookup"><span data-stu-id="7167f-167">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="7167f-168">DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="7167f-168">DlpNotifyPreSaveAsDocument</span></span>](endpointdlp-dlpnotifypresaveasdocument.md)                       | <span data-ttu-id="7167f-169">Proporciona al sistema información sobre un documento antes de iniciar una operación de guardar como.</span><span class="sxs-lookup"><span data-stu-id="7167f-169">Provides the system with information about a document before a save as operation is initiated.</span></span>                                  |
| [<span data-ttu-id="7167f-170">DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="7167f-170">DlpNotifyPostSaveAsDocument</span></span>](endpointdlp-dlpnotifypostsaveasdocument.md)                       | <span data-ttu-id="7167f-171">Proporciona al sistema información sobre un documento una vez completada la operación guardar como.</span><span class="sxs-lookup"><span data-stu-id="7167f-171">Provides the system with information about a document after the save as operation is completed.</span></span>                                  |


### <a name="drag-and-drop-operations"></a><span data-ttu-id="7167f-172">Operaciones de arrastrar y colocar</span><span class="sxs-lookup"><span data-stu-id="7167f-172">Drag and drop operations</span></span>

| <span data-ttu-id="7167f-173">API</span><span class="sxs-lookup"><span data-stu-id="7167f-173">API</span></span> | <span data-ttu-id="7167f-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="7167f-174">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="7167f-175">DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="7167f-175">DlpNotifyEnterDropTarget</span></span>](endpointdlp-dlpnotifyenterdroptarget.md)                       | <span data-ttu-id="7167f-176">Proporciona al sistema información sobre un documento cuando se introduce un destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="7167f-176">Provides the system with information about a document when a drop target is entered.</span></span>                                  |
| [<span data-ttu-id="7167f-177">DlpNotifyLeaveDropTarget</span><span class="sxs-lookup"><span data-stu-id="7167f-177">DlpNotifyLeaveDropTarget</span></span>](endpointdlp-dlpnotifyleavedroptarget.md)                       | <span data-ttu-id="7167f-178">Proporciona al sistema información sobre un documento cuando se sale de un destino de colocación.</span><span class="sxs-lookup"><span data-stu-id="7167f-178">Provides the system with information about a document when a drop target is exited.</span></span>                                  |
| [<span data-ttu-id="7167f-179">DlpNotifyPreDragDrop</span><span class="sxs-lookup"><span data-stu-id="7167f-179">DlpNotifyPreDragDrop</span></span>](endpointdlp-dlpnotifypredragdrop.md)                         | <span data-ttu-id="7167f-180">Proporciona al sistema información sobre un documento antes de iniciar una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="7167f-180">Provides the system with information about a document before a drag drop operation is initiated.</span></span>  |
| [<span data-ttu-id="7167f-181">DlpNotifyPostDragDrop</span><span class="sxs-lookup"><span data-stu-id="7167f-181">DlpNotifyPostDragDrop</span></span>](endpointdlp-dlpnotifypostdragdrop.md)                         | <span data-ttu-id="7167f-182">Proporciona al sistema información sobre un documento una vez completada una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="7167f-182">Provides the system with information about a document after a drag drop operation is completed.</span></span>  |


### <a name="clipboard-operations"></a><span data-ttu-id="7167f-183">opciones de Portapapeles</span><span class="sxs-lookup"><span data-stu-id="7167f-183">Clipboard operations</span></span>

| <span data-ttu-id="7167f-184">API</span><span class="sxs-lookup"><span data-stu-id="7167f-184">API</span></span> | <span data-ttu-id="7167f-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="7167f-185">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="7167f-186">DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="7167f-186">DlpNotifyPreCopyToClipboard</span></span>](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | <span data-ttu-id="7167f-187">Proporciona al sistema información sobre un documento antes de iniciar una operación de copia en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="7167f-187">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="7167f-188">DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="7167f-188">DlpNotifyPostCopyToClipboard</span></span>](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | <span data-ttu-id="7167f-189">Proporciona al sistema información sobre un documento una vez completada una operación de copia en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="7167f-189">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>  |
| [<span data-ttu-id="7167f-190">DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="7167f-190">DlpNotifyPrePasteFromClipboard</span></span>](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | <span data-ttu-id="7167f-191">Proporciona al sistema información sobre un documento antes de iniciar una operación de pegar desde el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="7167f-191">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="7167f-192">DlpNotifyPostPasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="7167f-192">DlpNotifyPostPasteFromClipboard</span></span>](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | <span data-ttu-id="7167f-193">Proporciona al sistema información sobre un documento después de que se haya completado una operación de pegado del Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="7167f-193">Provides the system with information about a document after a paste from clipboard operation has completed.</span></span>                                  |
| [<span data-ttu-id="7167f-194">DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="7167f-194">DlpNotifyPostStashClipboard</span></span>](endpointdlp-dlpnotifypoststashclipboard.md)                       | <span data-ttu-id="7167f-195">Proporciona al sistema información de estado una vez completada una operación de almacenamiento escalonado del Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="7167f-195">Provides the system with status information after a stash clipboard operation is completed.</span></span>                                  |
| [<span data-ttu-id="7167f-196">DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="7167f-196">DlpNotifyPreStashClipboard</span></span>](endpointdlp-dlpnotifyprestashclipboard.md)                       | <span data-ttu-id="7167f-197">Notifica al sistema antes de que se inicie una operación de almacenamiento escalonado del Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="7167f-197">Notifies the system before a stash clipboard operation is initiated.</span></span>                                  |
| [<span data-ttu-id="7167f-198">DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="7167f-198">DlpMustPasteFromSystemClipboard</span></span>](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | <span data-ttu-id="7167f-199">Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomar los datos de su caché interna.</span><span class="sxs-lookup"><span data-stu-id="7167f-199">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>                                  |

### <a name="print-operations"></a><span data-ttu-id="7167f-200">Operaciones de impresión</span><span class="sxs-lookup"><span data-stu-id="7167f-200">Print operations</span></span>

| <span data-ttu-id="7167f-201">API</span><span class="sxs-lookup"><span data-stu-id="7167f-201">API</span></span> | <span data-ttu-id="7167f-202">Descripción</span><span class="sxs-lookup"><span data-stu-id="7167f-202">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="7167f-203">DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="7167f-203">DlpNotifyPrePrint</span></span>](endpointdlp-dlpnotifypreprint.md)                         | <span data-ttu-id="7167f-204">Proporciona al sistema información sobre un documento antes de iniciar una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="7167f-204">Provides the system with information about a document before a print operation is initiated.</span></span>  |
| [<span data-ttu-id="7167f-205">DlpNotifyPostStartPrint</span><span class="sxs-lookup"><span data-stu-id="7167f-205">DlpNotifyPostStartPrint</span></span>](endpointdlp-dlpnotifypoststartprint.md)                       | <span data-ttu-id="7167f-206">Proporciona al sistema información sobre un documento después de que se haya iniciado una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="7167f-206">Provides the system with information about a document after an print operation has started.</span></span>                                  |
| [<span data-ttu-id="7167f-207">DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="7167f-207">DlpNotifyPostPrint</span></span>](endpointdlp-dlpnotifypostprint.md)                       | <span data-ttu-id="7167f-208">Proporciona al sistema información sobre un documento una vez completada una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="7167f-208">Provides the system with information about a document after a print operation has completed.</span></span>                                  |

## <a name="endpoint-dlp-example-header"></a><span data-ttu-id="7167f-209">Encabezado de ejemplo dlp de punto de conexión</span><span class="sxs-lookup"><span data-stu-id="7167f-209">Endpoint DLP example header</span></span>

<span data-ttu-id="7167f-210">Dado que el encabezado DLP del punto de conexión no se incluye en el Windows SDK, debe crear el archivo de encabezado usted mismo para obtener firmas de API que se usarán en la implementación.</span><span class="sxs-lookup"><span data-stu-id="7167f-210">Because the endpoint DLP header is not included in the Windows SDK, you must create the header file yourself to get API signatures to use in your implementation.</span></span> <span data-ttu-id="7167f-211">Para su comodidad, proporcionamos código de ejemplo que puede copiar y pegar en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7167f-211">For your convenience we're providing example code that you can copy and paste into your application.</span></span> <span data-ttu-id="7167f-212">Además de las declaraciones de función, esta lista de código también define constantes útiles, como la información de control de versiones y las rutas de acceso de clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="7167f-212">In addition to function declarations, this code listing also defines useful constants such as versioning information and registry key paths.</span></span>

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


```


