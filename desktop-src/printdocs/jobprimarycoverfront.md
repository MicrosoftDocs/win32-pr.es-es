---
description: Obtenga información sobre el elemento JobPrimaryCoverFront, que describe la hoja de cobertura frontal. Todo el trabajo tendrá una sola hoja principal.
ms.assetid: 270b16f6-677c-430a-aa69-1b5c6dfd3ba4
title: JobPrimaryCoverFront
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c60aef4a70404ce6777b9bfe2848fddffa4e89d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408678"
---
# <a name="jobprimarycoverfront"></a><span data-ttu-id="f1416-104">JobPrimaryCoverFront</span><span class="sxs-lookup"><span data-stu-id="f1416-104">JobPrimaryCoverFront</span></span>

<span data-ttu-id="f1416-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="f1416-105">This topic is not current.</span></span> <span data-ttu-id="f1416-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f1416-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f1416-107">Describe la hoja de cobertura frontal (inicial).</span><span class="sxs-lookup"><span data-stu-id="f1416-107">Describes the front (beginning) cover sheet.</span></span> <span data-ttu-id="f1416-108">Todo el trabajo tendrá una sola hoja principal.</span><span class="sxs-lookup"><span data-stu-id="f1416-108">The entire job will have a single primary sheet.</span></span> <span data-ttu-id="f1416-109">La hoja de cobertura se debe imprimir en PageMediaSize y PageMediaType usados para la primera página del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f1416-109">The cover sheet should be printed on the PageMediaSize and PageMediaType used for the first page of the job.</span></span> <span data-ttu-id="f1416-110">La hoja de cobertura debe integrarse en las opciones de procesamiento (por ejemplo, JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously), tal como se indica en la opción especificada.</span><span class="sxs-lookup"><span data-stu-id="f1416-110">The cover sheet should be integrated into processing options (such as JobDuplexAllDocumentsContiguously, JobNUpAllDocumentsContiguously) as indicated by the Option specified.</span></span>

-   [<span data-ttu-id="f1416-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f1416-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f1416-112">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="f1416-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f1416-113">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f1416-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f1416-114">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f1416-114">Element Information</span></span>



| <span data-ttu-id="f1416-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="f1416-115">Name</span></span> | <span data-ttu-id="f1416-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f1416-116">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1416-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f1416-117">Element Type</span></span> <br/>   | <span data-ttu-id="f1416-118">Característica</span><span class="sxs-lookup"><span data-stu-id="f1416-118">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f1416-119">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="f1416-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f1416-120">Trabajo</span><span class="sxs-lookup"><span data-stu-id="f1416-120">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f1416-121">Notas</span><span class="sxs-lookup"><span data-stu-id="f1416-121">Notes</span></span> <br/>          | <span data-ttu-id="f1416-122">Los consumidores compatibles con XPS DEBEN exigir que una referencia de URI a un recurso, como una imagen o un perfil de color en un documento De capacidades de impresión o PrintTicket, haga referencia a un nombre de elemento (un URI relativo a la raíz del paquete) dentro del mismo paquete de documento XPS que contiene el PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="f1416-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="f1416-123">Un consumidor XPS compatible NO DEBE usar un URI que no sea compatible con la sintaxis de nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="f1416-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="f1416-124">Esta configuración es específica de XPS.</span><span class="sxs-lookup"><span data-stu-id="f1416-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="f1416-125">Los URI a los que se hace referencia en un documento De capacidades de impresión o PrintTicket NO SE DEBEN resolver como direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="f1416-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="f1416-126">Esto no es seguro, ya que es posible que no se resuelvan según lo previsto y pueden crear riesgos de seguridad perjudiciales para el controlador y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f1416-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="f1416-127">Contenido estructural</span><span class="sxs-lookup"><span data-stu-id="f1416-127">Structural Content</span></span>

<span data-ttu-id="f1416-128">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="f1416-128">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the front cover sheet. -->
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="f1416-129">Variables de estructura</span><span class="sxs-lookup"><span data-stu-id="f1416-129">Structure Variables</span></span>

<span data-ttu-id="f1416-130">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="f1416-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f1416-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="f1416-131">Name</span></span>                               | <span data-ttu-id="f1416-132">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f1416-132">Data type</span></span>         | <span data-ttu-id="f1416-133">Unidad</span><span class="sxs-lookup"><span data-stu-id="f1416-133">Unit</span></span>           | <span data-ttu-id="f1416-134">Valores admitidos</span><span class="sxs-lookup"><span data-stu-id="f1416-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f1416-135">Resumen</span><span class="sxs-lookup"><span data-stu-id="f1416-135">Summary</span></span>                                                                      |
|------------------------------------|-------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f1416-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f1416-136">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f1416-137">string</span><span class="sxs-lookup"><span data-stu-id="f1416-137">string</span></span><br/> | <span data-ttu-id="f1416-138">N/D</span><span class="sxs-lookup"><span data-stu-id="f1416-138">n/a</span></span><br/> | <span data-ttu-id="f1416-139">Nombre completo válido tal y como lo definen los [espacios de nombres en XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="f1416-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f1416-140">Si no se especifica ningún espacio de nombres, se asume el espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f1416-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f1416-141">Nombre de la opción.</span><span class="sxs-lookup"><span data-stu-id="f1416-141">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f1416-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f1416-142">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f1416-143">string</span><span class="sxs-lookup"><span data-stu-id="f1416-143">string</span></span><br/> | <span data-ttu-id="f1416-144">N/D</span><span class="sxs-lookup"><span data-stu-id="f1416-144">n/a</span></span><br/> | <span data-ttu-id="f1416-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="f1416-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f1416-146">Define una opción que, cuando se selecciona, deshabilitaría esta característica.</span><span class="sxs-lookup"><span data-stu-id="f1416-146">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f1416-147">lenguaje de marcado extensible (XML) Content</span><span class="sxs-lookup"><span data-stu-id="f1416-147">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f1416-148">Las palabras clave públicas del esquema de impresión se definen en el espacio de https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords nombres .</span><span class="sxs-lookup"><span data-stu-id="f1416-148">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f1416-149">El contenido lenguaje de marcado extensible público (XML) de esta palabra clave se define a continuación:</span><span class="sxs-lookup"><span data-stu-id="f1416-149">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPrimaryCoverFront">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the back side 
       of the cover sheet.  If a JobPrimaryCoverFrontSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" may be printed on either side 
       of the cover sheet.  If a JobCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverFrontSource" should be printed on the front side 
       of the cover sheet.  If a JobCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverFrontSource">
      <psf:ParameterRef name="psk:JobPrimaryCoverFrontSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="f1416-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1416-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1416-151">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="f1416-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




