---
title: Recibir cancelaciones
description: La aplicación de servidor puede llamar a RpcServerTestCancel con el identificador de enlace de la llamada en cuestión para averiguar si el cliente ha solicitado la cancelación de la llamada asincrónica. Devolverá RPC \_ S \_ OK si el cliente canceló la llamada.
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b8b48ef2796dab071ac705edf0ffca5156e235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076091"
---
# <a name="receiving-cancellations"></a><span data-ttu-id="c9a77-104">Recibir cancelaciones</span><span class="sxs-lookup"><span data-stu-id="c9a77-104">Receiving Cancellations</span></span>

<span data-ttu-id="c9a77-105">La aplicación de servidor puede llamar a [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) con el identificador de enlace de la llamada en cuestión para averiguar si el cliente ha solicitado la cancelación de la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c9a77-105">The server application can call [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) with the binding handle of the call in question to find out if the client has requested cancellation of the asynchronous call.</span></span> <span data-ttu-id="c9a77-106">Devolverá RPC \_ S \_ OK si el cliente canceló la llamada.</span><span class="sxs-lookup"><span data-stu-id="c9a77-106">It will return RPC\_S\_OK if the client canceled the call.</span></span>

 

 




