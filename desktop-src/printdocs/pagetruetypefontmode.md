---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: PageTrueTypeFontMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9fbbfc17582042c6f4f5b5d96838ba48f46825
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "103820450"
---
# <a name="pagetruetypefontmode"></a><span data-ttu-id="c533e-104">PageTrueTypeFontMode</span><span class="sxs-lookup"><span data-stu-id="c533e-104">PageTrueTypeFontMode</span></span>

<span data-ttu-id="c533e-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="c533e-105">This topic is not current.</span></span> <span data-ttu-id="c533e-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c533e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c533e-107">Describe el método de control de fuentes TrueType que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="c533e-107">Describes the method of TrueType font handling to be used.</span></span>

-   [<span data-ttu-id="c533e-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c533e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c533e-109">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c533e-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c533e-110">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="c533e-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c533e-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c533e-111">Element Information</span></span>



| <span data-ttu-id="c533e-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="c533e-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="c533e-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c533e-113">Element Type</span></span> <br/>   | <span data-ttu-id="c533e-114">Característica</span><span class="sxs-lookup"><span data-stu-id="c533e-114">Feature</span></span><br/> |
| <span data-ttu-id="c533e-115">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="c533e-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c533e-116">Página</span><span class="sxs-lookup"><span data-stu-id="c533e-116">Page</span></span><br/>    |
| <span data-ttu-id="c533e-117">Notas</span><span class="sxs-lookup"><span data-stu-id="c533e-117">Notes</span></span> <br/>          | <span data-ttu-id="c533e-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c533e-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c533e-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c533e-119">Structural Content</span></span>

<span data-ttu-id="c533e-120">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="c533e-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="c533e-121">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="c533e-121">Structure Variables</span></span>

<span data-ttu-id="c533e-122">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="c533e-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c533e-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="c533e-123">Name</span></span>                               | <span data-ttu-id="c533e-124">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c533e-124">Data type</span></span>         | <span data-ttu-id="c533e-125">Unidad</span><span class="sxs-lookup"><span data-stu-id="c533e-125">Unit</span></span>                  | <span data-ttu-id="c533e-126">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="c533e-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c533e-127">Resumen</span><span class="sxs-lookup"><span data-stu-id="c533e-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c533e-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c533e-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c533e-129">string</span><span class="sxs-lookup"><span data-stu-id="c533e-129">string</span></span><br/> | <span data-ttu-id="c533e-130">caracteres</span><span class="sxs-lookup"><span data-stu-id="c533e-130">characters</span></span><br/> | <span data-ttu-id="c533e-131">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c533e-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c533e-132">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c533e-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c533e-133">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="c533e-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c533e-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c533e-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c533e-135">string</span><span class="sxs-lookup"><span data-stu-id="c533e-135">string</span></span><br/> | <span data-ttu-id="c533e-136">N/D</span><span class="sxs-lookup"><span data-stu-id="c533e-136">n/a</span></span><br/>        | <span data-ttu-id="c533e-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="c533e-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c533e-138">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="c533e-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c533e-139">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="c533e-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c533e-140">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c533e-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c533e-141">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="c533e-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Automatic handling of TrueType font-->
  <psf:Option name="psk:Automatic" />
  <!--TrueType font is downloaded as outline font-->
  <psf:Option name="psk:DownloadAsOutlineFont" />
  <!--TrueType font is downloaded as raster font-->
  <psf:Option name="psk:DownloadAsRasterFont" />
  <!--TrueType font is downloaded as native true type font-->
  <psf:Option name="psk:DownloadAsNativeTrueTypeFont" />
  <!--TrueType font is rendered as a bitmap-->
  <psf:Option name="psk:RenderAsBitmap" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="c533e-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c533e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c533e-143">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c533e-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




