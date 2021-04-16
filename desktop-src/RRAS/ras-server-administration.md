---
title: Administración del servidor RAS
description: Windows NT Server 4,0 proporciona un conjunto de funciones para administrar los permisos y puertos de usuario en servidores RAS de Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administración del servidor, RAS
- Administración, servidor RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269225"
---
# <a name="ras-server-administration"></a><span data-ttu-id="bc678-105">Administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="bc678-105">RAS Server Administration</span></span>

<span data-ttu-id="bc678-106">Windows NT Server 4,0 proporciona un conjunto de funciones para administrar los permisos y puertos de usuario en servidores RAS de Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="bc678-106">Windows NT Server 4.0 provides a set of functions for administering user permissions and ports on Windows NT/Windows 2000 RAS servers.</span></span> <span data-ttu-id="bc678-107">Windows 95 no admite estas funciones.</span><span class="sxs-lookup"><span data-stu-id="bc678-107">Windows 95 does not support these functions.</span></span> <span data-ttu-id="bc678-108">Con estas funciones, puede desarrollar una aplicación de administración del servidor RAS para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="bc678-108">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="bc678-109">Enumerar a los usuarios que tienen un conjunto especificado de permisos de RAS</span><span class="sxs-lookup"><span data-stu-id="bc678-109">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="bc678-110">Asignar o revocar permisos RAS para un usuario especificado</span><span class="sxs-lookup"><span data-stu-id="bc678-110">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="bc678-111">Enumerar los puertos configurados en un servidor RAS</span><span class="sxs-lookup"><span data-stu-id="bc678-111">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="bc678-112">Obtener información y estadísticas acerca de un puerto específico en un servidor RAS</span><span class="sxs-lookup"><span data-stu-id="bc678-112">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="bc678-113">Restablecer los contadores de estadísticas de un puerto específico</span><span class="sxs-lookup"><span data-stu-id="bc678-113">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="bc678-114">Desconectar un puerto especificado</span><span class="sxs-lookup"><span data-stu-id="bc678-114">Disconnect a specified port</span></span>

<span data-ttu-id="bc678-115">También puede instalar un archivo DLL de administración del servidor RAS para auditar las conexiones de usuario y asignar direcciones IP a los usuarios de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="bc678-115">You can also install a RAS server administration DLL for auditing user connections and assigning IP addresses to dial-in users.</span></span> <span data-ttu-id="bc678-116">El archivo DLL exporta un conjunto de funciones a las que el servidor RAS llama cuando un usuario intenta conectarse o desconectarse.</span><span class="sxs-lookup"><span data-stu-id="bc678-116">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

 

 




