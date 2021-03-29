---
title: Animar una paleta
description: Animar una paleta
ms.assetid: 89493cc3-eca9-407f-99c2-903fba16992c
keywords:
- DrawDib, paletas
- DrawDibRealize función)
- DrawDibDraw función)
- DrawDibChangePalette función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e023ba8ee2c4791ebc8c3f2ac7ebf9a198f4a5ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791194"
---
# <a name="animating-a-palette"></a><span data-ttu-id="23074-107">Animar una paleta</span><span class="sxs-lookup"><span data-stu-id="23074-107">Animating a Palette</span></span>

<span data-ttu-id="23074-108">En el ejemplo siguiente se anima una paleta mediante las funciones [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette)y [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="23074-108">The following example animates a palette by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize), [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette), and [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) functions.</span></span>

<span data-ttu-id="23074-109">Puede cambiar los colores de un mapa de bits mediante la función [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) en combinación con [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span><span class="sxs-lookup"><span data-stu-id="23074-109">You can change the colors of a bitmap by using the [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) function in combination with [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette).</span></span> <span data-ttu-id="23074-110">En primer lugar, para permitir cambios en la paleta, especifique la \_ marca DDF Animate en la llamada a **DrawDibBegin**.</span><span class="sxs-lookup"><span data-stu-id="23074-110">First, to allow palette changes, specify the DDF\_ANIMATE flag in the call to **DrawDibBegin**.</span></span> <span data-ttu-id="23074-111">En segundo lugar, establezca los valores de la tabla de colores de las entradas de la paleta mediante **DrawDibChangePalette**.</span><span class="sxs-lookup"><span data-stu-id="23074-111">Second, set the color table values from the palette entries by using **DrawDibChangePalette**.</span></span>

<span data-ttu-id="23074-112">Por ejemplo, si *lppe* es una dirección de la matriz [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) que contiene los nuevos colores y *lpbi* es la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) utilizada en [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) o [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), el siguiente fragmento actualiza la tabla de colores Dib.</span><span class="sxs-lookup"><span data-stu-id="23074-112">For example, if *lppe* is an address of the [PALETTEENTRY](/previous-versions//ms532623(v=vs.85)) array containing the new colors, and *lpbi* is the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure used in [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) or [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw), the following fragment updates the DIB color table.</span></span>


```C++
hdc = GetDC(hwnd); 
DrawDibBegin(hdd, ....., DDF_ANIMATE); 
DrawDibRealize(hdd, hdc, fBackground); 
DrawDibDraw(hdd, hdc, ...., DDF_SAME_DRAW|DDF_SAME_HDC); 
 
// Call to change color. 
DrawDibChangePalette(hDD, iStart, iLen, lppe); 
. 
. 
. 
ReleaseDC(hwnd, hdc); 

```



## <a name="related-topics"></a><span data-ttu-id="23074-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23074-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23074-114">Usar DrawDib</span><span class="sxs-lookup"><span data-stu-id="23074-114">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 