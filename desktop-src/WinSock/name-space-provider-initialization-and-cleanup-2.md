---
description: Usar NSPStartup y NSPCleanup para la inicialización y limpieza del proveedor de espacios de nombres en el SPI de Windows Sockets (Winsock).
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Inicialización y limpieza del proveedor de espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fedd7b40d79e755262df581c92e1fe3bdbfb06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541542"
---
# <a name="namespace-provider-initialization-and-cleanup"></a><span data-ttu-id="e1744-103">Inicialización y limpieza del proveedor de espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="e1744-103">Namespace Provider Initialization and Cleanup</span></span>

-   [<span data-ttu-id="e1744-104">**NSPStartup**</span><span class="sxs-lookup"><span data-stu-id="e1744-104">**NSPStartup**</span></span>](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [<span data-ttu-id="e1744-105">**NSPCleanup**</span><span class="sxs-lookup"><span data-stu-id="e1744-105">**NSPCleanup**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

<span data-ttu-id="e1744-106">Como es el caso del SPI de transporte, un proveedor de espacios de nombres se inicializa con una llamada a [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) y finaliza con una llamada final a [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup).</span><span class="sxs-lookup"><span data-stu-id="e1744-106">As is the case for the transport SPI, a namespace provider is initialized with a call to [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) and is terminated with a final call to [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup).</span></span> <span data-ttu-id="e1744-107">Las llamadas a la función startup pueden estar anidadas, pero coincidirán con las llamadas correspondientes a la función Cleanup.</span><span class="sxs-lookup"><span data-stu-id="e1744-107">Calls to the startup function may be nested, but will be matched by corresponding calls to the cleanup function.</span></span> <span data-ttu-id="e1744-108">Un proveedor debe emplear el recuento de referencias para determinar cuándo se ha producido la llamada final a **NSPCleanup** .</span><span class="sxs-lookup"><span data-stu-id="e1744-108">A provider should employ reference counting to determine when the final call to **NSPCleanup** has occurred.</span></span>

 

 



