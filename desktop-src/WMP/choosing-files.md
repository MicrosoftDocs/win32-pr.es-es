---
title: Elegir archivos
description: Elegir archivos
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- crear máscaras, elegir archivos
- Aspectos de Windows Media Player, elegir archivos
- máscaras, elegir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269221"
---
# <a name="choosing-files"></a>Elegir archivos

Si desea elegir un archivo, puede usar código similar al ejemplo de lista de reproducción, pero sustituya lo siguiente por la sección PLAYELEMENT:


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



Esta línea usará el método **openDialog** de **Theme** para definir una **dirección URL** para el reproductor. Puede utilizar esta opción para elegir archivos que no están en listas de reproducción.

Puede ver un ejemplo de **openDialog** en funcionamiento similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




