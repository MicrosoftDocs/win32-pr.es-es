---
description: Este tema no es actual. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbf1233e172a81053baee0abe1e21d79064045a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997702"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="91e4b-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="91e4b-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="91e4b-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="91e4b-105">This topic is not current.</span></span> <span data-ttu-id="91e4b-106">Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="91e4b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="91e4b-107">Especifica una referencia de URI relativa a un perfil DEERK que define el espacio de colores que SE DEBE usar para la combinación.</span><span class="sxs-lookup"><span data-stu-id="91e4b-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="91e4b-108">es <Uri> un nombre de elemento absoluto relativo a la raíz del \_ paquete.</span><span class="sxs-lookup"><span data-stu-id="91e4b-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="91e4b-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="91e4b-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="91e4b-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="91e4b-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="91e4b-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="91e4b-111">Element Information</span></span>



| <span data-ttu-id="91e4b-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="91e4b-112">Name</span></span> | <span data-ttu-id="91e4b-113">Value</span><span class="sxs-lookup"><span data-stu-id="91e4b-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91e4b-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="91e4b-114">Element Type</span></span> <br/>   | <span data-ttu-id="91e4b-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="91e4b-115">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="91e4b-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="91e4b-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="91e4b-117">Página</span><span class="sxs-lookup"><span data-stu-id="91e4b-117">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="91e4b-118">Notas</span><span class="sxs-lookup"><span data-stu-id="91e4b-118">Notes</span></span> <br/>          | <span data-ttu-id="91e4b-119">Esto solo se aplica a los documentos XPS y no se debe usar en PrintTickets arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="91e4b-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="91e4b-120">Vinculado al elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="91e4b-120">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="91e4b-121">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="91e4b-121">Structure Content</span></span>

<span data-ttu-id="91e4b-122">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="91e4b-122">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlendColorSpaceICCProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="91e4b-123">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="91e4b-123">Structure Properties</span></span>

<span data-ttu-id="91e4b-124">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="91e4b-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="91e4b-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="91e4b-125">Property</span></span>                | <span data-ttu-id="91e4b-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="91e4b-126">xsi:type</span></span>           | <span data-ttu-id="91e4b-127">Value</span><span class="sxs-lookup"><span data-stu-id="91e4b-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="91e4b-128">DataType</span><span class="sxs-lookup"><span data-stu-id="91e4b-128">DataType</span></span><br/>     | <span data-ttu-id="91e4b-129">string</span><span class="sxs-lookup"><span data-stu-id="91e4b-129">string</span></span><br/>  | <span data-ttu-id="91e4b-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="91e4b-130">xs:string</span></span><br/>       |
| <span data-ttu-id="91e4b-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="91e4b-131">DefaultValue</span></span><br/> | <span data-ttu-id="91e4b-132">string</span><span class="sxs-lookup"><span data-stu-id="91e4b-132">string</span></span><br/>  | <span data-ttu-id="91e4b-133">no definido</span><span class="sxs-lookup"><span data-stu-id="91e4b-133">undefined</span></span><br/>       |
| <span data-ttu-id="91e4b-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="91e4b-134">MaxLength</span></span><br/>    | <span data-ttu-id="91e4b-135">integer</span><span class="sxs-lookup"><span data-stu-id="91e4b-135">integer</span></span><br/> | <span data-ttu-id="91e4b-136">no definido</span><span class="sxs-lookup"><span data-stu-id="91e4b-136">undefined</span></span><br/>       |
| <span data-ttu-id="91e4b-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="91e4b-137">MinLength</span></span><br/>    | <span data-ttu-id="91e4b-138">integer</span><span class="sxs-lookup"><span data-stu-id="91e4b-138">integer</span></span><br/> | <span data-ttu-id="91e4b-139">1</span><span class="sxs-lookup"><span data-stu-id="91e4b-139">1</span></span><br/>               |
| <span data-ttu-id="91e4b-140">Mandatory</span><span class="sxs-lookup"><span data-stu-id="91e4b-140">Mandatory</span></span><br/>    | <span data-ttu-id="91e4b-141">string</span><span class="sxs-lookup"><span data-stu-id="91e4b-141">string</span></span><br/>  | <span data-ttu-id="91e4b-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="91e4b-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="91e4b-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="91e4b-143">UnitType</span></span><br/>     | <span data-ttu-id="91e4b-144">string</span><span class="sxs-lookup"><span data-stu-id="91e4b-144">string</span></span><br/>  | <span data-ttu-id="91e4b-145">caracteres</span><span class="sxs-lookup"><span data-stu-id="91e4b-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="91e4b-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91e4b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91e4b-147">Especificación de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="91e4b-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




