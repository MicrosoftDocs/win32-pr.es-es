---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cb8440af2b35bbe8f3f4a82a567beee43d1d44
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707600"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="40ba6-104">PageMediaSizePSWidthOffset</span><span class="sxs-lookup"><span data-stu-id="40ba6-104">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="40ba6-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="40ba6-105">This topic is not current.</span></span> <span data-ttu-id="40ba6-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="40ba6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="40ba6-107">Especifica el desplazamiento perpendicular a la dirección de la orientación de la fuente (referencia a la [especificación de formato de archivo de descripción de impresora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="40ba6-107">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="40ba6-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="40ba6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="40ba6-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="40ba6-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="40ba6-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="40ba6-110">Element Information</span></span>



| <span data-ttu-id="40ba6-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="40ba6-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="40ba6-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="40ba6-112">Element Type</span></span> <br/>   | <span data-ttu-id="40ba6-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="40ba6-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="40ba6-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="40ba6-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="40ba6-115">Página</span><span class="sxs-lookup"><span data-stu-id="40ba6-115">Page</span></span><br/>                                             |
| <span data-ttu-id="40ba6-116">Notas</span><span class="sxs-lookup"><span data-stu-id="40ba6-116">Notes</span></span> <br/>          | <span data-ttu-id="40ba6-117">Vinculado al elemento PageMediaSize, opción CustomPS</span><span class="sxs-lookup"><span data-stu-id="40ba6-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="40ba6-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="40ba6-118">Structure Content</span></span>

<span data-ttu-id="40ba6-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="40ba6-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="40ba6-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="40ba6-120">Structure Properties</span></span>

<span data-ttu-id="40ba6-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="40ba6-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="40ba6-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40ba6-122">Property</span></span>                | <span data-ttu-id="40ba6-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="40ba6-123">xsi:type</span></span>           | <span data-ttu-id="40ba6-124">Value</span><span class="sxs-lookup"><span data-stu-id="40ba6-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="40ba6-125">DataType</span><span class="sxs-lookup"><span data-stu-id="40ba6-125">DataType</span></span><br/>     | <span data-ttu-id="40ba6-126">string</span><span class="sxs-lookup"><span data-stu-id="40ba6-126">string</span></span><br/>  | <span data-ttu-id="40ba6-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="40ba6-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="40ba6-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="40ba6-128">DefaultValue</span></span><br/> | <span data-ttu-id="40ba6-129">integer</span><span class="sxs-lookup"><span data-stu-id="40ba6-129">integer</span></span><br/> | <span data-ttu-id="40ba6-130">no definido</span><span class="sxs-lookup"><span data-stu-id="40ba6-130">undefined</span></span><br/>       |
| <span data-ttu-id="40ba6-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="40ba6-131">MaxValue</span></span><br/>     | <span data-ttu-id="40ba6-132">integer</span><span class="sxs-lookup"><span data-stu-id="40ba6-132">integer</span></span><br/> | <span data-ttu-id="40ba6-133">no definido</span><span class="sxs-lookup"><span data-stu-id="40ba6-133">undefined</span></span><br/>       |
| <span data-ttu-id="40ba6-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="40ba6-134">MinValue</span></span><br/>     | <span data-ttu-id="40ba6-135">integer</span><span class="sxs-lookup"><span data-stu-id="40ba6-135">integer</span></span><br/> | <span data-ttu-id="40ba6-136">no definido</span><span class="sxs-lookup"><span data-stu-id="40ba6-136">undefined</span></span><br/>       |
| <span data-ttu-id="40ba6-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="40ba6-137">Mandatory</span></span><br/>    | <span data-ttu-id="40ba6-138">string</span><span class="sxs-lookup"><span data-stu-id="40ba6-138">string</span></span><br/>  | <span data-ttu-id="40ba6-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="40ba6-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="40ba6-140">Múltiple</span><span class="sxs-lookup"><span data-stu-id="40ba6-140">Multiple</span></span><br/>     | <span data-ttu-id="40ba6-141">integer</span><span class="sxs-lookup"><span data-stu-id="40ba6-141">integer</span></span><br/> | <span data-ttu-id="40ba6-142">1</span><span class="sxs-lookup"><span data-stu-id="40ba6-142">1</span></span><br/>               |
| <span data-ttu-id="40ba6-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="40ba6-143">UnitType</span></span><br/>     | <span data-ttu-id="40ba6-144">string</span><span class="sxs-lookup"><span data-stu-id="40ba6-144">string</span></span><br/>  | <span data-ttu-id="40ba6-145">microns</span><span class="sxs-lookup"><span data-stu-id="40ba6-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="40ba6-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40ba6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ba6-147">Especificación de formato de archivo de descripción de impresora PostScript</span><span class="sxs-lookup"><span data-stu-id="40ba6-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="40ba6-148">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="40ba6-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




