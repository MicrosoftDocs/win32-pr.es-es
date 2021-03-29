---
title: Optimización de archivos compuestos
description: El almacenamiento asincrónico permite a las aplicaciones diseñar con precisión los archivos compuestos para que los datos estén disponibles en el orden en que las aplicaciones lo requieran.
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- Optimización de archivos compuestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773735"
---
# <a name="compound-file-optimization"></a><span data-ttu-id="2247d-104">Optimización de archivos compuestos</span><span class="sxs-lookup"><span data-stu-id="2247d-104">Compound File Optimization</span></span>

<span data-ttu-id="2247d-105">El almacenamiento asincrónico permite a las aplicaciones diseñar con precisión los archivos compuestos para que los datos estén disponibles en el orden en que las aplicaciones lo requieran.</span><span class="sxs-lookup"><span data-stu-id="2247d-105">Asynchronous storage enables applications to precisely layout compound files so that data is available in the order in which applications will require it.</span></span> <span data-ttu-id="2247d-106">Si una aplicación requiere solo parte de sus datos para mostrar la primera página de información, estos datos se pueden colocar al principio del archivo, incluso si reside lógicamente al final de un flujo...</span><span class="sxs-lookup"><span data-stu-id="2247d-106">If an application requires only part of its data to display a first page of information, this data can be placed at the beginning of the file, even if it logically resides at the end of a stream.</span></span> <span data-ttu-id="2247d-107">Los datos de diferentes flujos se pueden intercalar.</span><span class="sxs-lookup"><span data-stu-id="2247d-107">Data from different streams can be interleaved.</span></span> <span data-ttu-id="2247d-108">Los datos de audio y vídeo, por ejemplo, se pueden intercalar para que las operaciones de lectura posteriores recuperen ambos simultáneamente, un requisito para las aplicaciones multimedia.</span><span class="sxs-lookup"><span data-stu-id="2247d-108">Audio and video data, for example, can be interleaved so that subsequent read operations retrieve both simultaneously, a requirement for multimedia applications.</span></span>

<span data-ttu-id="2247d-109">[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) se puede usar para diseñar un doc, mejorando así el rendimiento en la mayoría de los escenarios.</span><span class="sxs-lookup"><span data-stu-id="2247d-109">[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) can be used to layout a docfile, thus improving performance in most scenarios.</span></span>

 

 




