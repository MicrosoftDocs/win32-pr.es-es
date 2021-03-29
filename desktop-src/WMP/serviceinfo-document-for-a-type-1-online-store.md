---
title: Documento ServiceInfo para una tienda en línea de tipo 1
description: Documento ServiceInfo para una tienda en línea de tipo 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 1 tiendas en línea, documento de ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075869"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a><span data-ttu-id="03098-107">Documento ServiceInfo para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="03098-107">ServiceInfo Document for a Type 1 Online Store</span></span>

<span data-ttu-id="03098-108">Tipo 1 las tiendas en línea deben proporcionar a Microsoft la dirección URL de un documento XML que describa la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="03098-108">Type 1 online stores must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="03098-109">Windows Media Player 11 usa este documento para determinar cómo configurar la interfaz de usuario para hospedar la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="03098-109">Windows Media Player 11 uses this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="03098-110">El documento ServiceInfo para un almacén de tipo 1 proporciona la siguiente información a Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="03098-110">The ServiceInfo document for a type 1 store provides the following information to Windows Media Player:</span></span>

-   <span data-ttu-id="03098-111">Información utilizada para configurar el botón **tiendas en línea** (también denominado pestaña), como el texto del botón, el color del botón y la información sobre herramientas del botón.</span><span class="sxs-lookup"><span data-stu-id="03098-111">Information used to configure the **Online Stores** button (also called a tab), such as the button text, the button color, and the tooltip for the button.</span></span>
-   <span data-ttu-id="03098-112">Direcciones URL para las imágenes que Windows Media Player muestra para identificar la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="03098-112">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="03098-113">Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Windows Media Player hospeda en su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="03098-113">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="03098-114">Dirección URL donde Windows Media Player puede recuperar el complemento de la tienda en línea para que el complemento se pueda instalar en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="03098-114">URL where Windows Media Player can retrieve the online store's plug-in so that the plug-in can be installed on the user's computer.</span></span>

<span data-ttu-id="03098-115">Cuando Windows Media Player recupera el documento ServiceInfo de la web, anexa una cadena de consulta a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="03098-115">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="03098-116">La cadena de consulta contiene parámetros que proporcionan información sobre la configuración regional y la ubicación geográfica del usuario, así como la versión de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="03098-116">The query string contains parameters that provide information about the user's locale and geographic location and the version of Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03098-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03098-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03098-118">**Acerca de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="03098-118">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="03098-119">**Creación dinámica del documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="03098-119">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="03098-120">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="03098-120">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="03098-121">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="03098-121">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




