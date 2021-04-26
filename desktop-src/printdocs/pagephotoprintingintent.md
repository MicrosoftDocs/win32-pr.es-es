---
description: Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: f9a00828-52df-449e-914b-4c6cd7c29f3a
title: PagePhotoPrintingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d56a0b46c73bb3afdcefe96dc2131c861d5419
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997982"
---
# <a name="pagephotoprintingintent"></a><span data-ttu-id="bc611-104">PagePhotoPrintingIntent</span><span class="sxs-lookup"><span data-stu-id="bc611-104">PagePhotoPrintingIntent</span></span>

<span data-ttu-id="bc611-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="bc611-105">This topic is not current.</span></span> <span data-ttu-id="bc611-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bc611-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bc611-107">Indica una intención de alto nivel al controlador para la población de la configuración de impresión de fotos.</span><span class="sxs-lookup"><span data-stu-id="bc611-107">Indicates a high-level intent to the driver for population of photo printing settings.</span></span> <span data-ttu-id="bc611-108">Esta configuración trata con la calidad de salida esperada que un usuario puede especificar al imprimir fotos.</span><span class="sxs-lookup"><span data-stu-id="bc611-108">These settings deal with the expected output quality a user may specify when printing photos.</span></span>

-   [<span data-ttu-id="bc611-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bc611-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="bc611-110">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="bc611-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="bc611-111">Contenido XML</span><span class="sxs-lookup"><span data-stu-id="bc611-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="bc611-112">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="bc611-112">Element Information</span></span>



| <span data-ttu-id="bc611-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc611-113">Name</span></span> | <span data-ttu-id="bc611-114">Value</span><span class="sxs-lookup"><span data-stu-id="bc611-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="bc611-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="bc611-115">Element Type</span></span> <br/>   | <span data-ttu-id="bc611-116">Característica</span><span class="sxs-lookup"><span data-stu-id="bc611-116">Feature</span></span><br/> |
| <span data-ttu-id="bc611-117">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="bc611-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="bc611-118">Página</span><span class="sxs-lookup"><span data-stu-id="bc611-118">Page</span></span><br/>    |
| <span data-ttu-id="bc611-119">Notas</span><span class="sxs-lookup"><span data-stu-id="bc611-119">Notes</span></span> <br/>          | <span data-ttu-id="bc611-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bc611-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="bc611-121">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="bc611-121">Structural Content</span></span>

<span data-ttu-id="bc611-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="bc611-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">  
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
    <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
  </psf:Property>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="bc611-123">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="bc611-123">Structure Variables</span></span>

<span data-ttu-id="bc611-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="bc611-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="bc611-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc611-125">Name</span></span>                               | <span data-ttu-id="bc611-126">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bc611-126">Data type</span></span>         | <span data-ttu-id="bc611-127">Unidad</span><span class="sxs-lookup"><span data-stu-id="bc611-127">Unit</span></span>                  | <span data-ttu-id="bc611-128">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="bc611-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="bc611-129">Resumen</span><span class="sxs-lookup"><span data-stu-id="bc611-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bc611-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="bc611-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="bc611-131">string</span><span class="sxs-lookup"><span data-stu-id="bc611-131">string</span></span><br/> | <span data-ttu-id="bc611-132">caracteres</span><span class="sxs-lookup"><span data-stu-id="bc611-132">characters</span></span><br/> | <span data-ttu-id="bc611-133">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="bc611-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="bc611-134">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bc611-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="bc611-135">Nombre de la opción</span><span class="sxs-lookup"><span data-stu-id="bc611-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="bc611-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="bc611-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="bc611-137">string</span><span class="sxs-lookup"><span data-stu-id="bc611-137">string</span></span><br/> | <span data-ttu-id="bc611-138">N/D</span><span class="sxs-lookup"><span data-stu-id="bc611-138">n/a</span></span><br/>        | <span data-ttu-id="bc611-139">True, False</span><span class="sxs-lookup"><span data-stu-id="bc611-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="bc611-140">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="bc611-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="bc611-141">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="bc611-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="bc611-142">Las palabras clave del esquema de impresión público se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="bc611-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="bc611-143">El contenido lenguaje de marcado extensible público (XML) para esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="bc611-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PagePhotoPrintingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- No Photoprinting Intent (Allows the application to specify no intent resolution.  (PrintTicket settings should not be altered) -->
  <psf:Option name="psk:None" />
  <!-- Best Quality Photoprinting (Provided mostly for marketing reasons; utilizes the highest capabilities of the device) -->
  <psf:Option name="psk:PhotoBest" />
  <!-- Draft Quality Photoprinting (Quick, low ink volume print for proofing purposes) -->
  <psf:Option name="psk:PhotoDraft" />
  <!-- Standard Quality Photoprinting (OEM suggested settings for standard photo-printing) -->
  <psf:Option name="psk:PhotoStandard" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="bc611-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc611-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc611-145">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="bc611-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




