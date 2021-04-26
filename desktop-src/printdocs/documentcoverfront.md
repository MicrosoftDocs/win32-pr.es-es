---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 25dbd083-5815-4b25-bfdc-4d14f96d2b45
title: DocumentCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd89bea06d3004b435cb55ff51612b1b91380c7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996272"
---
# <a name="documentcoverfront"></a><span data-ttu-id="3f5a2-104">DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="3f5a2-104">DocumentCoverFront</span></span>

<span data-ttu-id="3f5a2-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-105">This topic is not current.</span></span> <span data-ttu-id="3f5a2-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3f5a2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3f5a2-107">Describe la hoja de cobertura frontal (inicial).</span><span class="sxs-lookup"><span data-stu-id="3f5a2-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="3f5a2-108">Cada documento tendrá una hoja independiente.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-108">Each document will have a separate sheet.</span></span> <span data-ttu-id="3f5a2-109">La hoja de cobertura debe imprimirse en pageMediaSize y PageMediaType usados para la primera página del documento.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the document.</span></span> <span data-ttu-id="3f5a2-110">La hoja de cobertura debe integrarse en las opciones de procesamiento (como DocumentDuplex o DocumentNUp), tal como se indica en la opción especificada.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-110">The cover sheet should be integrated into processing options (such as DocumentDuplex, DocumentNUp) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="3f5a2-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3f5a2-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3f5a2-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="3f5a2-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3f5a2-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="3f5a2-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3f5a2-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="3f5a2-114">Element Information</span></span>



| <span data-ttu-id="3f5a2-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f5a2-115">Name</span></span> | <span data-ttu-id="3f5a2-116">Value</span><span class="sxs-lookup"><span data-stu-id="3f5a2-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f5a2-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3f5a2-117">Element Type</span></span> <br/>   | <span data-ttu-id="3f5a2-118">Característica</span><span class="sxs-lookup"><span data-stu-id="3f5a2-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3f5a2-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="3f5a2-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3f5a2-120">Documento</span><span class="sxs-lookup"><span data-stu-id="3f5a2-120">Document</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3f5a2-121">Notas</span><span class="sxs-lookup"><span data-stu-id="3f5a2-121">Notes</span></span> <br/>          | <span data-ttu-id="3f5a2-122">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso como una imagen o un perfil de color en un documento de capacidades de impresión o PrintTicket DEBE hacer referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="3f5a2-123">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="3f5a2-124">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="3f5a2-125">Los URI a los que se hace referencia en un documento de capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="3f5a2-126">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y puedan crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="3f5a2-127">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="3f5a2-127">Structural Content</span></span>

<span data-ttu-id="3f5a2-128">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="3f5a2-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS specific part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="3f5a2-129">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="3f5a2-129">Structure Variables</span></span>

<span data-ttu-id="3f5a2-130">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3f5a2-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f5a2-131">Name</span></span>                               | <span data-ttu-id="3f5a2-132">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3f5a2-132">Data type</span></span>         | <span data-ttu-id="3f5a2-133">Unidad</span><span class="sxs-lookup"><span data-stu-id="3f5a2-133">Unit</span></span>                  | <span data-ttu-id="3f5a2-134">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="3f5a2-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3f5a2-135">Resumen</span><span class="sxs-lookup"><span data-stu-id="3f5a2-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3f5a2-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="3f5a2-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3f5a2-137">string</span><span class="sxs-lookup"><span data-stu-id="3f5a2-137">string</span></span><br/> | <span data-ttu-id="3f5a2-138">caracteres</span><span class="sxs-lookup"><span data-stu-id="3f5a2-138">characters</span></span><br/> | <span data-ttu-id="3f5a2-139">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="3f5a2-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3f5a2-140">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3f5a2-141">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3f5a2-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3f5a2-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3f5a2-143">string</span><span class="sxs-lookup"><span data-stu-id="3f5a2-143">string</span></span><br/> | <span data-ttu-id="3f5a2-144">N/D</span><span class="sxs-lookup"><span data-stu-id="3f5a2-144">n/a</span></span><br/>        | <span data-ttu-id="3f5a2-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3f5a2-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="3f5a2-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3f5a2-147">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="3f5a2-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3f5a2-148">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="3f5a2-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3f5a2-149">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="3f5a2-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:DocumentCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="3f5a2-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3f5a2-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f5a2-151">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="3f5a2-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




