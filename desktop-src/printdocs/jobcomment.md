---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210b80d4f81771dfa98d79d4ecf187b3ef145f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998352"
---
# <a name="jobcomment"></a>JobComment

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica un comentario asociado al trabajo. Ejemplo: "Entrega a la sala 1234 cuando haya finalizado".

-   [Información de elemento](#element-information)
-   [Contenido de la estructura](#structure-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Value |
|----------------------------|-------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/> |
| Prefijo de ámbito <br/> | Trabajo<br/>          |
| Notas <br/>          | Ninguno<br/>         |



 

## <a name="structure-content"></a>Contenido de la estructura

La estructura XML de este elemento es la siguiente:

``` syntax
<psf:ParameterDef name="psk:JobComment">
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

## <a name="structure-properties"></a>Propiedades de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Propiedad                | xsi:type           | Value                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | no definido<br/>       |
| MaxLength<br/>    | integer<br/> | no definido<br/>       |
| MinLength<br/>    | integer<br/> | 1<br/>               |
| Mandatory<br/>    | string<br/>  | psk:Conditional<br/> |
| UnitType<br/>     | string<br/>  | caracteres<br/>      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




