---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c0d55c2150f5a2299672ebf95d6656b238acc1
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361976"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="9e32f-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="9e32f-104">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="9e32f-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="9e32f-105">This topic is not current.</span></span> <span data-ttu-id="9e32f-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9e32f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9e32f-107">Especifica el porcentaje de reemplazo del componente gris que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="9e32f-107">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="9e32f-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9e32f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9e32f-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="9e32f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="9e32f-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="9e32f-110">Element Information</span></span>



| <span data-ttu-id="9e32f-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="9e32f-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="9e32f-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9e32f-112">Element Type</span></span> <br/>   | <span data-ttu-id="9e32f-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9e32f-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="9e32f-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="9e32f-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9e32f-115">Página</span><span class="sxs-lookup"><span data-stu-id="9e32f-115">Page</span></span><br/>                                            |
| <span data-ttu-id="9e32f-116">Notas</span><span class="sxs-lookup"><span data-stu-id="9e32f-116">Notes</span></span> <br/>          | <span data-ttu-id="9e32f-117">Vinculado al elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="9e32f-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="9e32f-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="9e32f-118">Structure Content</span></span>

<span data-ttu-id="9e32f-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="9e32f-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="9e32f-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="9e32f-120">Structure Properties</span></span>

<span data-ttu-id="9e32f-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="9e32f-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9e32f-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9e32f-122">Property</span></span>                | <span data-ttu-id="9e32f-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="9e32f-123">xsi:type</span></span>           | <span data-ttu-id="9e32f-124">Value</span><span class="sxs-lookup"><span data-stu-id="9e32f-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="9e32f-125">DataType</span><span class="sxs-lookup"><span data-stu-id="9e32f-125">DataType</span></span><br/>     | <span data-ttu-id="9e32f-126">string</span><span class="sxs-lookup"><span data-stu-id="9e32f-126">string</span></span><br/>  | <span data-ttu-id="9e32f-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9e32f-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="9e32f-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="9e32f-128">DefaultValue</span></span><br/> | <span data-ttu-id="9e32f-129">string</span><span class="sxs-lookup"><span data-stu-id="9e32f-129">string</span></span><br/>  | <span data-ttu-id="9e32f-130">no definido</span><span class="sxs-lookup"><span data-stu-id="9e32f-130">undefined</span></span><br/>       |
| <span data-ttu-id="9e32f-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="9e32f-131">MaxValue</span></span><br/>     | <span data-ttu-id="9e32f-132">integer</span><span class="sxs-lookup"><span data-stu-id="9e32f-132">integer</span></span><br/> | <span data-ttu-id="9e32f-133">100</span><span class="sxs-lookup"><span data-stu-id="9e32f-133">100</span></span><br/>             |
| <span data-ttu-id="9e32f-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="9e32f-134">MinValue</span></span><br/>     | <span data-ttu-id="9e32f-135">integer</span><span class="sxs-lookup"><span data-stu-id="9e32f-135">integer</span></span><br/> | <span data-ttu-id="9e32f-136">0</span><span class="sxs-lookup"><span data-stu-id="9e32f-136">0</span></span><br/>               |
| <span data-ttu-id="9e32f-137">Múltiple</span><span class="sxs-lookup"><span data-stu-id="9e32f-137">Multiple</span></span><br/>     | <span data-ttu-id="9e32f-138">integer</span><span class="sxs-lookup"><span data-stu-id="9e32f-138">integer</span></span><br/> | <span data-ttu-id="9e32f-139">1</span><span class="sxs-lookup"><span data-stu-id="9e32f-139">1</span></span><br/>               |
| <span data-ttu-id="9e32f-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="9e32f-140">Mandatory</span></span><br/>    | <span data-ttu-id="9e32f-141">string</span><span class="sxs-lookup"><span data-stu-id="9e32f-141">string</span></span><br/>  | <span data-ttu-id="9e32f-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="9e32f-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="9e32f-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="9e32f-143">UnitType</span></span><br/>     | <span data-ttu-id="9e32f-144">string</span><span class="sxs-lookup"><span data-stu-id="9e32f-144">string</span></span><br/>  | <span data-ttu-id="9e32f-145">percent</span><span class="sxs-lookup"><span data-stu-id="9e32f-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="9e32f-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e32f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e32f-147">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="9e32f-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




