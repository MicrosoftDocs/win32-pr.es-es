---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 52f02fc1-56fb-404d-8939-df3a4b21570d
title: PageOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f004329c217d4aab6ddc3c1d166037e7c7b5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104424171"
---
# <a name="pageorientation"></a><span data-ttu-id="c31b0-104">PageOrientation</span><span class="sxs-lookup"><span data-stu-id="c31b0-104">PageOrientation</span></span>

<span data-ttu-id="c31b0-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="c31b0-105">This topic is not current.</span></span> <span data-ttu-id="c31b0-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c31b0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c31b0-107">Describe la orientación de la hoja de medios físicos.</span><span class="sxs-lookup"><span data-stu-id="c31b0-107">Describes the orientation of the physical media sheet.</span></span>



| <span data-ttu-id="c31b0-108">Opción</span><span class="sxs-lookup"><span data-stu-id="c31b0-108">Option</span></span>                       | <span data-ttu-id="c31b0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="c31b0-109">Definition</span></span>                                                                                              |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c31b0-110">Horizontal</span><span class="sxs-lookup"><span data-stu-id="c31b0-110">Landscape</span></span> <br/>        | <span data-ttu-id="c31b0-111">El contenido se gira en la página 90?? grados CCW en relación con la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="c31b0-111">Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.</span></span><br/>  |
| <span data-ttu-id="c31b0-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="c31b0-112">Portrait</span></span> <br/>         | <span data-ttu-id="c31b0-113">Orientación estándar.</span><span class="sxs-lookup"><span data-stu-id="c31b0-113">Standard Orientation.</span></span><br/>                                                                        |
| <span data-ttu-id="c31b0-114">ReverseLandscape</span><span class="sxs-lookup"><span data-stu-id="c31b0-114">ReverseLandscape</span></span> <br/> | <span data-ttu-id="c31b0-115">El contenido se gira en la página 270?? grados CCW en relación con la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="c31b0-115">Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation.</span></span><br/> |
| <span data-ttu-id="c31b0-116">ReversePortrait</span><span class="sxs-lookup"><span data-stu-id="c31b0-116">ReversePortrait</span></span> <br/>  | <span data-ttu-id="c31b0-117">El contenido se gira en la página 180?? grados en relación con la orientación estándar (vertical).</span><span class="sxs-lookup"><span data-stu-id="c31b0-117">Content is rotated on the page 180??degrees relative to standard (portrait) orientation.</span></span><br/>     |



 

-   [<span data-ttu-id="c31b0-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c31b0-118">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c31b0-119">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c31b0-119">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c31b0-120">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="c31b0-120">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c31b0-121">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c31b0-121">Element Information</span></span>



| <span data-ttu-id="c31b0-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="c31b0-122">Name</span></span>                       |                                                                                                                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c31b0-123">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c31b0-123">Element Type</span></span> <br/>   | <span data-ttu-id="c31b0-124">Característica</span><span class="sxs-lookup"><span data-stu-id="c31b0-124">Feature</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="c31b0-125">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="c31b0-125">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c31b0-126">Página</span><span class="sxs-lookup"><span data-stu-id="c31b0-126">Page</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="c31b0-127">Notas</span><span class="sxs-lookup"><span data-stu-id="c31b0-127">Notes</span></span> <br/>          | <span data-ttu-id="c31b0-128">Si un dispositivo de impresora solo puede admitir una dirección horizontal y esta dirección se conoce como "horizontal inversa", la orientación de la página se considerará "horizontal".</span><span class="sxs-lookup"><span data-stu-id="c31b0-128">If a Printer Device can only support one landscape direction and this direction is referred to as "Reverse Landscape", then the page orientation will still be considered to be "Landscape".</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c31b0-129">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="c31b0-129">Structural Content</span></span>

<span data-ttu-id="c31b0-130">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="c31b0-130">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
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

## <a name="structure-variables"></a><span data-ttu-id="c31b0-131">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="c31b0-131">Structure Variables</span></span>

<span data-ttu-id="c31b0-132">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="c31b0-132">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c31b0-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="c31b0-133">Name</span></span>                               | <span data-ttu-id="c31b0-134">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c31b0-134">Data type</span></span>         | <span data-ttu-id="c31b0-135">Unidad</span><span class="sxs-lookup"><span data-stu-id="c31b0-135">Unit</span></span>                  | <span data-ttu-id="c31b0-136">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="c31b0-136">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c31b0-137">Resumen</span><span class="sxs-lookup"><span data-stu-id="c31b0-137">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c31b0-138">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c31b0-138">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c31b0-139">string</span><span class="sxs-lookup"><span data-stu-id="c31b0-139">string</span></span><br/> | <span data-ttu-id="c31b0-140">caracteres</span><span class="sxs-lookup"><span data-stu-id="c31b0-140">characters</span></span><br/> | <span data-ttu-id="c31b0-141">Nombre completo válido, tal y como se define en los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c31b0-141">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c31b0-142">Si no se especifica ningún espacio de nombres, se presupone el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c31b0-142">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c31b0-143">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="c31b0-143">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c31b0-144">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c31b0-144">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c31b0-145">string</span><span class="sxs-lookup"><span data-stu-id="c31b0-145">string</span></span><br/> | <span data-ttu-id="c31b0-146">N/D</span><span class="sxs-lookup"><span data-stu-id="c31b0-146">n/a</span></span><br/>        | <span data-ttu-id="c31b0-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="c31b0-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c31b0-148">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="c31b0-148">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c31b0-149">Contenido de lenguaje de marcado extensible (XML)</span><span class="sxs-lookup"><span data-stu-id="c31b0-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c31b0-150">Las palabras clave del esquema de impresión público se definen en el https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="c31b0-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c31b0-151">El contenido de lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="c31b0-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOrientation">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Content is rotated on the page 90??degrees CCW relative to standard (portrait) orientation.??-->
  <psf:Option name="psk:Landscape" />
  <!-- Standard Orientation-->
  <psf:Option name="psk:Portrait" />
  <!-- Content is rotated on the page 270??degrees CCW relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReverseLandscape" />
  <!-- Content is rotated on the page 180??degrees relative to standard (portrait) orientation??-->
  <psf:Option name="psk:ReversePortrait" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="c31b0-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c31b0-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c31b0-153">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="c31b0-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




