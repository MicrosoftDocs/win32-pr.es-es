---
description: Puede girar las fuentes TrueType en cualquier ángulo.
ms.assetid: 371ddb04-410a-425b-857f-ed3d4749b0f9
title: Girar líneas de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 703dd4543caaa083d0b2d66512b53a0b5a213c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984807"
---
# <a name="rotating-lines-of-text"></a>Girar líneas de texto

Puede girar las fuentes TrueType en cualquier ángulo. Esto resulta útil para etiquetar gráficos y otras ilustraciones. En el ejemplo siguiente se gira una cadena en incrementos de 10 grados en torno al centro del área cliente cambiando el valor de los miembros **lfEscapement** y **lfOrientation** de la estructura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) utilizada para crear la fuente.


```C++
#include "strsafe.h"
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    
    case WM_PAINT:
        {
        hdc = BeginPaint(hWnd, &ps);
        RECT rc; 
        int angle; 
        HGDIOBJ hfnt, hfntPrev; 
        WCHAR lpszRotate[22] = TEXT("String to be rotated.");
        HRESULT hr; 
        size_t pcch = 22;
 
// Allocate memory for a LOGFONT structure. 
 
PLOGFONT plf = (PLOGFONT) LocalAlloc(LPTR, sizeof(LOGFONT)); 
 
 
// Specify a font typeface name and weight. 
 
hr = StringCchCopy(plf->lfFaceName, 6, TEXT("Arial"));
if (FAILED(hr))
{
// TODO: write error handler
}

plf->lfWeight = FW_NORMAL; 
 
// Retrieve the client-rectangle dimensions. 
 
GetClientRect(hWnd, &rc); 
 
// Set the background mode to transparent for the 
// text-output operation. 
 
SetBkMode(hdc, TRANSPARENT); 
 
// Draw the string 36 times, rotating 10 degrees 
// counter-clockwise each time. 
 
for (angle = 0; angle < 3600; angle += 100) 
{ 
    plf->lfEscapement = angle; 
    hfnt = CreateFontIndirect(plf); 
    hfntPrev = SelectObject(hdc, hfnt);
    
    //
    // The StringCchLength call is fitted to the lpszRotate string
    //
    hr = StringCchLength(lpszRotate, 22, &pcch);
    if (FAILED(hr))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, rc.right / 2, rc.bottom / 2, 
        lpszRotate, pcch); 
    SelectObject(hdc, hfntPrev); 
    DeleteObject(hfnt); 
} 
 
// Reset the background mode to its default. 
 
SetBkMode(hdc, OPAQUE); 
 
// Free the memory allocated for the LOGFONT structure. 
 
LocalFree((LOCALHANDLE) plf); 
        EndPaint(hWnd, &ps);
        break;
        }
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 



