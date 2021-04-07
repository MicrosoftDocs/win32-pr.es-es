---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d3e12591f6c648e6e636e1bb72f4df694d0d13
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003477"
---
# <a name="pagewatermarkoriginheight"></a>PageWatermarkOriginHeight

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica el origen de una marca de agua en relación con el origen de PageImageableSize.

-   [Información de elemento](#element-information)
-   [Contenido de la estructura](#structure-content)

## <a name="element-information"></a>Información de elemento



| Nombre                       |                                            |
|----------------------------|--------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                    |
| Prefijo de ámbito <br/> | Página<br/>                            |
| Notas <br/>          | Vinculado al elemento PageWatermark<br/> |



 

## <a name="structure-content"></a>Contenido de la estructura

La estructura XML de este elemento es la siguiente:

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propiedades de la estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Propiedad                | xsi:type           | Value                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>                                                   |
| DefaultValue<br/> | integer<br/> | no definido<br/>                                                    |
| MaxValue<br/>     | integer<br/> | Menor o igual que el valor de PageImageableSize-ExtentHeight<br/> |
| MinValue<br/>     | integer<br/> | 0<br/>                                                            |
| Múltiple<br/>     | integer<br/> | 1<br/>                                                            |
| Mandatory<br/>    | string<br/>  | PSK: condicional<br/>                                              |
| UnitType<br/>     | string<br/>  | microns<br/>                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




