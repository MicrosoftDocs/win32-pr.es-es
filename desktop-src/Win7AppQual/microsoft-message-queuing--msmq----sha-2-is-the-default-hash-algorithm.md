---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f0d2476133ca7939bc90effa3842c0b90482ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278219"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="f7a22-103">Microsoft Message Queuing (MSMQ): SHA 2 es el algoritmo hash predeterminado</span><span class="sxs-lookup"><span data-stu-id="f7a22-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f7a22-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="f7a22-104">Affected Platforms</span></span>

 <span data-ttu-id="f7a22-105">**Clientes** -Windows XP Windows \| vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="f7a22-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="f7a22-106">**Servidores** : windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7a22-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="f7a22-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="f7a22-107">Feature Impact</span></span>

 <span data-ttu-id="f7a22-108">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="f7a22-108">**Severity** - Low</span></span>  
<span data-ttu-id="f7a22-109">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="f7a22-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="f7a22-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7a22-110">Description</span></span>

<span data-ttu-id="f7a22-111">En Windows 7, MSMQ usa SHA-2 como valor predeterminado al firmar un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="f7a22-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="f7a22-112">Además, todos los mensajes entrantes deben estar firmados con SHA-2.</span><span class="sxs-lookup"><span data-stu-id="f7a22-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="f7a22-113">Puede habilitar la compatibilidad con un algoritmo de cifrado inferior a través de una clave del registro accesible para el administrador.</span><span class="sxs-lookup"><span data-stu-id="f7a22-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="f7a22-114">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="f7a22-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="f7a22-115">MSMQ en Windows 2003 o inferior no aceptará mensajes firmados que se originan en MSMQ en Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7a22-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="f7a22-116">MSMQ en Windows 7 no aceptará mensajes firmados procedentes de Windows 2008 o inferior</span><span class="sxs-lookup"><span data-stu-id="f7a22-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="f7a22-117">Mitigación</span><span class="sxs-lookup"><span data-stu-id="f7a22-117">Mitigation</span></span>

<span data-ttu-id="f7a22-118">Los usuarios deben considerar la posibilidad de actualizar a Windows 7 para aprovechar el algoritmo de firma más seguro.</span><span class="sxs-lookup"><span data-stu-id="f7a22-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="f7a22-119">Para habilitar el intercambio de mensajes con firma directa entre Windows 7 y cualquier sistema operativo de nivel inferior, el administrador debe agregar las excepciones adecuadas en los equipos MSMQ.</span><span class="sxs-lookup"><span data-stu-id="f7a22-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



