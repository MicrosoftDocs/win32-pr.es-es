---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bae72b69f83697cc2f482f21995acb587a2ace
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104279918"
---
# <a name="pageoutputbin"></a>PageOutputBin

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe la lista completa de ubicaciones compatibles para el dispositivo. Permite la especificación de la ubicación de salida por página. Las palabras clave JobOutputBin, DocumentOutputBin y PageOutputBin se excluyen mutuamente solo se debe especificar una en un documento de funcionalidades de impresión o PrintTicket.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [Contenido de lenguaje de marcado extensible (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre                       |                    |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Característica<br/> |
| Prefijo de ámbito <br/> | Página<br/>    |
| Notas <br/>          | Ninguno<br/>    |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:PageOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                                   | Tipo de datos          | Unidad                  | Valores admitidos                                                                                                                                                                      | Resumen                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| \_OptionName\_<br/>              | string<br/>  | caracteres<br/> | Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                                  |
| \_IdentityOptionValue\_<br/>     | string<br/>  | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/>        |
| \_BinTypeValue\_<br/>            | string<br/>  | N/D<br/>        | FaceDownTray, FaceUpTray, buzón, clasificador, apilador, no finalizador ninguno.<br/>                                                                                                         | Especifica el tipo general de la ubicación.<br/>                                   |
| \_MediaSheetCapacityValue\_<br/> | integer<br/> | Sheet<br/>     | Mayor que 0.<br/>                                                                                                                                                            | Especifica la capacidad de los medios en número de páginas (nivel completo) de la ubicación.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenido de lenguaje de marcado extensible (XML)

Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres. El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:PageOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
    
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




