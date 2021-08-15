---
description: El tipo de datos STRING de OCTET ASN.1 se codifica en un triplete TLV que comienza con un byte tag de 0x04.
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: OCTET STRING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588547e5211efbe6b4b91a8a72f6644de0c7c4dcbacc570f0a1f272e7cc97962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903759"
---
# <a name="octet-string"></a>OCTET STRING

El tipo de datos ASN.1 **OCTET STRING** se codifica en un triplete TLV que comienza con un byte **tag** de 0x04. Los **tipos de datos OCTET STRING** y BIT [STRING](about-bit-string.md) son muy similares. Por lo tanto, los dos tipos se codifican de forma similar, salvo que, dado que el byte final de una **CADENA OCTET** no puede tener bits sin usar, no se debe agregar ningún bytes iniciales al contenido. En el ejemplo siguiente, adaptado del tema [ASN.1](cmc-encoded-asn-1.md) con codificación CMC, se muestra cómo se codifica el nombre de una plantilla de certificado como una matriz de bytes.

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

Si la matriz de bytes contiene menos de 128 bytes, el campo **Longitud** del triplete TLV solo requiere un byte para especificar la longitud del contenido. Si tiene más de 127 bytes, el bit 7 del campo **Longitud** se establece en 1 y los bits del 6 al 0 especifican el número de bytes adicionales usados para identificar la longitud del contenido. Esto se muestra en el ejemplo siguiente, donde el bit de orden superior del segundo byte de la primera línea se establece en 1 y el byte indica que hay un byte **de longitud** final. Por lo tanto, el tercer byte especifica que el contenido tiene una longitud 0x80 bytes.

``` syntax
04 81 80                       ; OCTET_STRING (80 Bytes)
   38 10 60 e2 70 69 91 4a     ;   8.`.pi.J
   8b b5 22 57 2a 62 ef de     ;   .."W*b..
   15 7d 59 d6 4e 20 9a 45     ;   .}Y.N .E
   2b e3 fd fc 68 ba af bf     ;   +...h...
   9c 17 b0 8e 6d c4 29 1e     ;   ....m.).
   e3 21 ac bb 5a 8a c9 67     ;   .!..Z..g
   0a d4 45 93 10 c0 26 eb     ;   ..E...&.
   0a 83 c2 b1 40 87 36 f7     ;   ....@.6.
   a0 26 da b9 bb 46 73 88     ;   .&...Fs.
   7a 67 b9 e6 b3 6f ea 59     ;   zg...o.Y
   28 8a d3 92 72 f6 7b 89     ;   (...r.{.
   a0 d8 2d 9e 40 eb 1e bb     ;   ..-.@...
   6e ae f0 5a ed 16 c9 e3     ;   n..Z....
   27 59 37 8f f3 4a 98 60     ;   'Y7..J.`
   f8 fb a7 0a ee 1b 6e 91     ;   ......n.
   95 96 cf 0d 56 ac ab 35     ;   ....V..5
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sistema de tipo ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificación DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



