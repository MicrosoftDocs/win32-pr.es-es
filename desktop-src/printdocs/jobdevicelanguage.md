---
description: Obtenga información sobre el elemento JobDeviceLanguage, que describe los idiomas de dispositivo admitidos para enviar datos desde el controlador al dispositivo físico.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7bf56018a2b395ec5aa182336a89d8872057e7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408999"
---
# <a name="jobdevicelanguage"></a>JobDeviceLanguage

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Describe los idiomas de dispositivo admitidos para enviar datos desde el controlador al dispositivo físico. A menudo se denomina "Idioma de descripción de página". Esta palabra clave define qué idioma de descripción de página es compatible con el controlador y el dispositivo físico.

-   [Información de elemento](#element-information)
-   [Contenido estructural](#structural-content)
-   [lenguaje de marcado extensible (XML) Content](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Información de elemento



| Nombre | Valor |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Característica<br/> |
| Prefijo de ámbito <br/> | Trabajo<br/>     |
| Notas <br/>          | Ninguno<br/>    |



 

## <a name="structural-content"></a>Contenido estructural

La estructura XML de este elemento es:

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variables de estructura

En la tabla siguiente se describen las características de las variables definidas en la estructura XML.



| Nombre                                 | Tipo de datos         | Unidad                  | Valores admitidos                                                                                                                                                                      | Resumen                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>            | string<br/> | caracteres<br/> | Nombre completo válido tal y como se define en [Espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.<br/> | Nombre de la opción.<br/>                                           |
| \_IdentityOptionValue\_<br/>   | string<br/> | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define una opción que, cuando se selecciona, deshabilitaría esta característica.<br/> |
| \_LanguageLevelValue\_<br/>    | string<br/> | N/D<br/>        | Ninguno.<br/>                                                                                                                                                                      | Especifica el nivel de idioma (por ejemplo, nivel 2 de PS).<br/>           |
| \_LanguageEncodingValue\_<br/> | string<br/> | N/D<br/>        | Ninguno.<br/>                                                                                                                                                                      | Especifica la codificación de idioma (por ejemplo, ISOLatin1).<br/>         |
| \_LanguageVersionValue\_<br/>  | string<br/> | N/D<br/>        | Ninguno.<br/>                                                                                                                                                                      | Especifica la versión de idioma.<br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a>lenguaje de marcado extensible (XML) Content

Las palabras clave de esquema de impresión públicas se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres . El contenido lenguaje de marcado extensible (XML) de esta palabra clave se define a continuación:

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




