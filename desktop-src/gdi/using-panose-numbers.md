---
description: Los archivos de fuente TrueType incluyen números Panose, que las aplicaciones pueden usar para elegir una fuente que se ajuste a sus especificaciones.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Usar números Panose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278514"
---
# <a name="using-panose-numbers"></a><span data-ttu-id="5e71f-103">Usar números Panose</span><span class="sxs-lookup"><span data-stu-id="5e71f-103">Using PANOSE Numbers</span></span>

<span data-ttu-id="5e71f-104">Los archivos de fuente TrueType incluyen números Panose, que las aplicaciones pueden usar para elegir una fuente que se ajuste a sus especificaciones.</span><span class="sxs-lookup"><span data-stu-id="5e71f-104">TrueType font files include PANOSE numbers, which applications can use to choose a font that closely matches their specifications.</span></span> <span data-ttu-id="5e71f-105">El sistema Panose clasifica caras por 10 atributos diferentes.</span><span class="sxs-lookup"><span data-stu-id="5e71f-105">The PANOSE system classifies faces by 10 different attributes.</span></span> <span data-ttu-id="5e71f-106">Para obtener más información acerca de estos atributos, vea [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose).</span><span class="sxs-lookup"><span data-stu-id="5e71f-106">For more information about these attributes, see [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose).</span></span> <span data-ttu-id="5e71f-107">Una estructura **PAnose** forma parte de la estructura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (cuyos valores se rellenan mediante una llamada a la función [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).</span><span class="sxs-lookup"><span data-stu-id="5e71f-107">A **PANOSE** structure is part of the [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) structure (whose values are filled in by calling the [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) function).</span></span>

<span data-ttu-id="5e71f-108">Los atributos Panose se clasifican individualmente en una escala.</span><span class="sxs-lookup"><span data-stu-id="5e71f-108">The PANOSE attributes are rated individually on a scale.</span></span> <span data-ttu-id="5e71f-109">Los valores resultantes se concatenan para generar un número.</span><span class="sxs-lookup"><span data-stu-id="5e71f-109">The resulting values are concatenated to produce a number.</span></span> <span data-ttu-id="5e71f-110">Dado este número para una fuente y una métrica matemática para medir las distancias en el espacio de la Panose, una aplicación puede determinar los vecinos más cercanos.</span><span class="sxs-lookup"><span data-stu-id="5e71f-110">Given this number for a font and a mathematical metric to measure distances in the PANOSE space, an application can determine the nearest neighbors.</span></span>

 

 



