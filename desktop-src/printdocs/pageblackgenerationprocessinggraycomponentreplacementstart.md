---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dedf425cd31dd83bce877358c456d1cd16183fa
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698014"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="5a1f1-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="5a1f1-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="5a1f1-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="5a1f1-105">This topic is not current.</span></span> <span data-ttu-id="5a1f1-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5a1f1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a1f1-107">Describe el punto del intervalo "resaltar a la sombra" donde debe iniciarse GCR (100% de la sombra más oscura).</span><span class="sxs-lookup"><span data-stu-id="5a1f1-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="5a1f1-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5a1f1-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5a1f1-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5a1f1-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5a1f1-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5a1f1-110">Element Information</span></span>



| <span data-ttu-id="5a1f1-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="5a1f1-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="5a1f1-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5a1f1-112">Element Type</span></span> <br/>   | <span data-ttu-id="5a1f1-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5a1f1-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="5a1f1-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="5a1f1-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5a1f1-115">Página</span><span class="sxs-lookup"><span data-stu-id="5a1f1-115">Page</span></span><br/>                                            |
| <span data-ttu-id="5a1f1-116">Notas</span><span class="sxs-lookup"><span data-stu-id="5a1f1-116">Notes</span></span> <br/>          | <span data-ttu-id="5a1f1-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="5a1f1-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="5a1f1-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="5a1f1-118">Structure Content</span></span>

<span data-ttu-id="5a1f1-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="5a1f1-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="5a1f1-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="5a1f1-120">Structure Properties</span></span>

<span data-ttu-id="5a1f1-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="5a1f1-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5a1f1-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a1f1-122">Property</span></span>                | <span data-ttu-id="5a1f1-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5a1f1-123">xsi:type</span></span>           | <span data-ttu-id="5a1f1-124">Value</span><span class="sxs-lookup"><span data-stu-id="5a1f1-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="5a1f1-125">DataType</span><span class="sxs-lookup"><span data-stu-id="5a1f1-125">DataType</span></span><br/>     | <span data-ttu-id="5a1f1-126">string</span><span class="sxs-lookup"><span data-stu-id="5a1f1-126">string</span></span><br/>  | <span data-ttu-id="5a1f1-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a1f1-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="5a1f1-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5a1f1-128">DefaultValue</span></span><br/> | <span data-ttu-id="5a1f1-129">string</span><span class="sxs-lookup"><span data-stu-id="5a1f1-129">string</span></span><br/>  | <span data-ttu-id="5a1f1-130">no definido</span><span class="sxs-lookup"><span data-stu-id="5a1f1-130">undefined</span></span><br/>       |
| <span data-ttu-id="5a1f1-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5a1f1-131">MaxValue</span></span><br/>     | <span data-ttu-id="5a1f1-132">integer</span><span class="sxs-lookup"><span data-stu-id="5a1f1-132">integer</span></span><br/> | <span data-ttu-id="5a1f1-133">100</span><span class="sxs-lookup"><span data-stu-id="5a1f1-133">100</span></span><br/>             |
| <span data-ttu-id="5a1f1-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="5a1f1-134">MinValue</span></span><br/>     | <span data-ttu-id="5a1f1-135">integer</span><span class="sxs-lookup"><span data-stu-id="5a1f1-135">integer</span></span><br/> | <span data-ttu-id="5a1f1-136">0</span><span class="sxs-lookup"><span data-stu-id="5a1f1-136">0</span></span><br/>               |
| <span data-ttu-id="5a1f1-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="5a1f1-137">Multiple</span></span><br/>     | <span data-ttu-id="5a1f1-138">integer</span><span class="sxs-lookup"><span data-stu-id="5a1f1-138">integer</span></span><br/> | <span data-ttu-id="5a1f1-139">1</span><span class="sxs-lookup"><span data-stu-id="5a1f1-139">1</span></span><br/>               |
| <span data-ttu-id="5a1f1-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="5a1f1-140">Mandatory</span></span><br/>    | <span data-ttu-id="5a1f1-141">string</span><span class="sxs-lookup"><span data-stu-id="5a1f1-141">string</span></span><br/>  | <span data-ttu-id="5a1f1-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="5a1f1-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="5a1f1-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="5a1f1-143">UnitType</span></span><br/>     | <span data-ttu-id="5a1f1-144">string</span><span class="sxs-lookup"><span data-stu-id="5a1f1-144">string</span></span><br/>  | <span data-ttu-id="5a1f1-145">percent</span><span class="sxs-lookup"><span data-stu-id="5a1f1-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="5a1f1-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a1f1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a1f1-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="5a1f1-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




