---
title: Enumerar recursos
description: En este tema se describen las funciones que se usan para obtener listas de recursos.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ea7f2600f6da98cff6f16853092004a542b0f206
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105653297"
---
# <a name="enumerating-resources"></a><span data-ttu-id="2b014-103">Enumerar recursos</span><span class="sxs-lookup"><span data-stu-id="2b014-103">Enumerating resources</span></span>

<span data-ttu-id="2b014-104">En determinadas situaciones, puede que desee detectar el contenido de los recursos de un módulo ejecutable portable (PE) desconocido.</span><span class="sxs-lookup"><span data-stu-id="2b014-104">In certain situations, you might want to discover the resource contents of an unknown portable executable (PE) module.</span></span> <span data-ttu-id="2b014-105">El Windows SDK proporciona funciones de enumeración de recursos que permiten a la aplicación obtener listas de tipos de recursos, nombres y lenguajes en un módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="2b014-105">The Windows SDK provides resource enumeration functions that enable your application to obtain lists of resource types, names, and languages in a specified module.</span></span>

* <span data-ttu-id="2b014-106">Las funciones [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) y [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) proporcionan una lista de los tipos de recursos que se encuentran en el módulo.</span><span class="sxs-lookup"><span data-stu-id="2b014-106">The [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) and [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) functions provide a list of resource types found in the module.</span></span>
* <span data-ttu-id="2b014-107">Las funciones [**EnumResourceNamesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) y [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) proporcionan el nombre de cada recurso dentro de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="2b014-107">The [**EnumResourceNamesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcenamesw) and [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) functions provide the name of each resource within a given type.</span></span>
* <span data-ttu-id="2b014-108">Las funciones [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) y [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) proporcionan el idioma de cada recurso de un nombre y tipo determinados.</span><span class="sxs-lookup"><span data-stu-id="2b014-108">The [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) and [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) functions provide the language of each resource of a given name and type.</span></span> 

<span data-ttu-id="2b014-109">Estas funciones y sus funciones de devolución de llamada asociadas permiten a la aplicación crear una lista de todos los recursos de un módulo.</span><span class="sxs-lookup"><span data-stu-id="2b014-109">These functions and their associated callback functions enable your application to create a list of all resources in a module.</span></span> <span data-ttu-id="2b014-110">Este proceso se describe en [creación de una lista de recursos](using-resources.md).</span><span class="sxs-lookup"><span data-stu-id="2b014-110">This process is described in [Creating a resource list](using-resources.md).</span></span>

## <a name="-see-also"></a><span data-ttu-id="2b014-111">-véase: también</span><span class="sxs-lookup"><span data-stu-id="2b014-111">-see-also</span></span>

[<span data-ttu-id="2b014-112">Msistuff.exe aplicación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b014-112">Msistuff.exe sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
