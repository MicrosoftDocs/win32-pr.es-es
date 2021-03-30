---
description: Una secuencia contiene un campo ordenado de uno o más tipos.
ms.assetid: b1a37cde-d5a2-4b01-a076-cb09741ae51d
title: SEQUENCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28602a122303f341507029375a2e4762581ec197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001939"
---
# <a name="sequence"></a><span data-ttu-id="c3873-103">SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="c3873-103">SEQUENCE</span></span>

<span data-ttu-id="c3873-104">Una **secuencia** contiene un campo ordenado de uno o más tipos.</span><span class="sxs-lookup"><span data-stu-id="c3873-104">A **SEQUENCE** contains an ordered field of one or more types.</span></span> <span data-ttu-id="c3873-105">Se codifica en un tripledo TLV que comienza con un byte de **etiqueta** de 0x30.</span><span class="sxs-lookup"><span data-stu-id="c3873-105">It is encoded into a TLV triplet that begins with a **Tag** byte of 0x30.</span></span> <span data-ttu-id="c3873-106">La siguiente Certutil.exe salida del tema [ \# ASN. 1 codificado PKCS 10](pkcs--10-encoded-asn-1.md) proporciona varios ejemplos de estructuras de datos de **secuencia** .</span><span class="sxs-lookup"><span data-stu-id="c3873-106">The following Certutil.exe output from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic provides multiple examples of **SEQUENCE** data structures.</span></span> <span data-ttu-id="c3873-107">La salida muestra una clave pública de 128 bytes y un exponente de tres bytes.</span><span class="sxs-lookup"><span data-stu-id="c3873-107">The output shows a 128 byte public key and three byte exponent.</span></span>

``` syntax
30 81 9f                             ; SEQUENCE (9f Bytes)
|  30 0d                             ; SEQUENCE (d Bytes)
|  |  |  06 09                       ; OBJECT_ID (9 Bytes)
|  |  |  2a 86 48 86 f7 0d 01 01 01  ; 1.2.840.113549.1.1.1 
|  |  05 00                          ; NULL (0 Bytes)
|  03 81 8d                          ; BIT_STRING (8d Bytes)
|     00
|     30 81 89                       ; SEQUENCE (89 Bytes)
|        02 81 81                    ; INTEGER (81 Bytes)
|        |  00
|        |  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|        |  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|        |  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|        |  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|        |  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|        |  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|        |  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|        |  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
|        02 03                       ; INTEGER (3 Bytes)
|           01 00 01
```

<span data-ttu-id="c3873-108">Si la **secuencia** contiene menos de 128 bytes, el campo de **longitud** del tripledo TLV requiere un solo byte para especificar la longitud del contenido.</span><span class="sxs-lookup"><span data-stu-id="c3873-108">If the **SEQUENCE** contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="c3873-109">Si tiene más de 127 bytes, el bit 7 del campo **longitud** se establece en 1 y los bits 6 a 0 especifican el número de bytes adicionales que se usan para identificar la longitud del contenido.</span><span class="sxs-lookup"><span data-stu-id="c3873-109">If it is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="c3873-110">Por ejemplo, el segundo byte de la primera línea del ejemplo anterior indica que hay un byte de **longitud** final que especifica 0x9F bytes de contenido (la mayoría de la **secuencia** no se muestra).</span><span class="sxs-lookup"><span data-stu-id="c3873-110">For example, the second byte of the first line in the preceding example indicates that there is one trailing **Length** byte that specifies 0x9F bytes of content (most of the **SEQUENCE** is not shown).</span></span> <span data-ttu-id="c3873-111">Para obtener más información, vea [longitud codificada y bytes de valor](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="c3873-111">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3873-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3873-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3873-113">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="c3873-113">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="c3873-114">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="c3873-114">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



