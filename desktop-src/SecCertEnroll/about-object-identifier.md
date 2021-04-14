---
description: El tipo de datos del identificador de objeto se codifica en un tripledo TLV que comienza con un valor de etiqueta de 0x06.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: IDENTIFICADOR DE OBJETO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cc81169968bfb3be5a49b0f30b8171cd904bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276810"
---
# <a name="object-identifier"></a>IDENTIFICADOR DE OBJETO

El tipo de datos del **identificador de objeto** se codifica en un tripledo TLV que comienza con un valor de **etiqueta** de 0x06. Cada entero de un identificador de objeto decimal con puntos (OID) se codifica según las siguientes reglas:

-   Los dos primeros nodos del OID se codifican en un solo byte. El primer nodo se multiplica por el decimal 40 y el resultado se agrega al valor del segundo nodo.
-   Los valores de nodo menores o iguales a 127 se codifican en un byte.
-   Los valores de nodo mayores o iguales que 128 se codifican en varios bytes. El bit 7 del byte situado más a la izquierda se establece en uno. Los bits del 0 al 6 de cada byte contienen el valor codificado.

Estos puntos se muestran en la siguiente ilustración.

![codificación der del tipo de datos del identificador de objeto](images/der-tlv-oid.png)

En el ejemplo siguiente se muestra cómo el atributo **ClientID** se codifica en una solicitud de certificado.

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

 

 



