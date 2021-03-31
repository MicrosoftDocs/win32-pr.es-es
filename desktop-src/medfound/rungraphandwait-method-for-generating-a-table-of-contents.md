---
description: Función RunGraphAndWait para generar una tabla de contenido
ms.assetid: f6eac1cf-05c3-48b6-b9b4-02966facdc95
title: Función RunGraphAndWait para generar una tabla de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d14b71454bd8c47ab22f165ba59951037bf669a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275818"
---
# <a name="rungraphandwait-function-for-generating-a-table-of-contents"></a>Función RunGraphAndWait para generar una tabla de contenido

La siguiente función es una función auxiliar de un programa de ejemplo que se describe en [generación automática de una tabla de contenido](generating-a-table-of-contents-automatically.md).


```C++
HRESULT RunGraphAndWait(IGraphBuilder* pGraph)
{
   IMediaControl* pControl = NULL;
   HRESULT hr = pGraph->QueryInterface(IID_IMediaControl, (VOID**)&pControl);

   if(SUCCEEDED(hr))
   {
      hr = pControl->Run();

      if(SUCCEEDED(hr))
      {
         IMediaEvent* pEvent = NULL;
         hr = pControl->QueryInterface(IID_IMediaEvent, (VOID**)&pEvent);

         if(SUCCEEDED(hr))
         {
           long eventCode = 0;
           hr = pEvent->WaitForCompletion(INFINITE, &eventCode);
           pEvent->Release();
           pEvent = NULL;
         }
      }

      pControl->Release();
      pControl = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Generar automáticamente una tabla de contenido](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



