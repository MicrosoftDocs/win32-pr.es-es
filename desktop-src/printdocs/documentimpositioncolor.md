---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea74db8ac616bc9ca6b7f6cde22f62bea742e7fb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717410"
---
# <a name="documentimpositioncolor"></a>DocumentImpositionColor

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El contenido de la aplicación etiquetado con el color con nombre especificado debe aparecer en todas las separaciones de color.

-   [Información de elemento](#element-information)
-   [Contenido de la estructura](#structure-content)

## <a name="element-information"></a>Información de elemento



| Nombre                       |                         |
|----------------------------|-------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/> |
| Prefijo de ámbito <br/> | Documento<br/>     |
| Notas <br/>          | Ninguno<br/>         |



 

## <a name="structure-content"></a>Contenido de la estructura

La estructura XML de este elemento es:

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a>Propiedades de la estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Propiedad                | xsi:type           | Value                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | no definido<br/>       |
| MaxLength<br/>    | integer<br/> | no definido<br/>       |
| MinLength<br/>    | integer<br/> | 1<br/>               |
| Mandatory<br/>    | string<br/>  | PSK: condicional<br/> |
| UnitType<br/>     | string<br/>  | caracteres<br/>      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




