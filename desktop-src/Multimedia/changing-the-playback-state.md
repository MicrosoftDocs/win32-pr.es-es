---
title: Cambiar el estado de reproducción
description: Cambiar el estado de reproducción
ms.assetid: 69ede616-aea4-4b7c-a12b-014ac0485b1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9401c79e6bb89f4f21c5e3c220b48dc99a2b6109
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791644"
---
# <a name="changing-the-playback-state"></a><span data-ttu-id="a3755-103">Cambiar el estado de reproducción</span><span class="sxs-lookup"><span data-stu-id="a3755-103">Changing the Playback State</span></span>

<span data-ttu-id="a3755-104">En los siguientes ejemplos se muestra cómo usar los comandos [**PAUSE**](pause.md), [**resume**](resume.md), [**Stop**](stop.md)y [**Seek**](seek.md) en la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a3755-104">The following examples show how to use the [**pause**](pause.md), [**resume**](resume.md), [**stop**](stop.md), and [**seek**](seek.md) commands in the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>


```C++
// Assume the file was opened with the alias 'movie'. 
 
// Pause play. 
mciSendString("pause movie", NULL, 0, NULL); 
 
// Resume play. 
mciSendString("resume movie", NULL, 0, NULL); 
 
// Stop play. 
mciSendString("stop movie", NULL, 0, NULL); 
 
// Seek to the beginning. 
mciSendString("seek movie to start", NULL, 0, NULL); 
 
```



<span data-ttu-id="a3755-105">En el ejemplo siguiente se muestra cómo cambiar el modo de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="a3755-105">The following example shows how to change the seek mode:</span></span>


```C++
// Set seek mode with the string interface. 
// Assume the file was opened with the alias 'movie'. 
 
void SetSeekMode(BOOL fExact) 
{ 
    if (fExact) 
        mciSendString("set movie seek exactly on", NULL, 0, NULL); 
    else 
        mciSendString("set movie seek exactly off", NULL, 0, NULL); 
} 
```



 

 