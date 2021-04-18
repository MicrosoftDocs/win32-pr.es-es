---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a605bd22424de61eebfaf48b18acf8e57eab523
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717427"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="91e2f-104">DocumentCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="91e2f-104">DocumentCoverBackSource</span></span>

<span data-ttu-id="91e2f-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="91e2f-105">This topic is not current.</span></span> <span data-ttu-id="91e2f-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="91e2f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="91e2f-107">Especifica el origen de una hoja de portada personalizada.</span><span class="sxs-lookup"><span data-stu-id="91e2f-107">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="91e2f-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="91e2f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="91e2f-109">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="91e2f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="91e2f-110">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="91e2f-110">Element Information</span></span>



| <span data-ttu-id="91e2f-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="91e2f-111">Name</span></span>                       |                                                |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="91e2f-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="91e2f-112">Element Type</span></span> <br/>   | <span data-ttu-id="91e2f-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="91e2f-113">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="91e2f-114">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="91e2f-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="91e2f-115">Documento</span><span class="sxs-lookup"><span data-stu-id="91e2f-115">Document</span></span><br/>                            |
| <span data-ttu-id="91e2f-116">Notas</span><span class="sxs-lookup"><span data-stu-id="91e2f-116">Notes</span></span> <br/>          | <span data-ttu-id="91e2f-117">Vinculado al elemento DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="91e2f-117">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="91e2f-118">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="91e2f-118">Structure Content</span></span>

<span data-ttu-id="91e2f-119">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="91e2f-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverBackSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="91e2f-120">Propiedades de la estructura</span><span class="sxs-lookup"><span data-stu-id="91e2f-120">Structure Properties</span></span>

<span data-ttu-id="91e2f-121">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="91e2f-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="91e2f-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="91e2f-122">Property</span></span>                | <span data-ttu-id="91e2f-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="91e2f-123">xsi:type</span></span>           | <span data-ttu-id="91e2f-124">Value</span><span class="sxs-lookup"><span data-stu-id="91e2f-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="91e2f-125">DataType</span><span class="sxs-lookup"><span data-stu-id="91e2f-125">DataType</span></span><br/>     | <span data-ttu-id="91e2f-126">string</span><span class="sxs-lookup"><span data-stu-id="91e2f-126">string</span></span><br/>  | <span data-ttu-id="91e2f-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="91e2f-127">xs:string</span></span><br/>       |
| <span data-ttu-id="91e2f-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="91e2f-128">DefaultValue</span></span><br/> | <span data-ttu-id="91e2f-129">string</span><span class="sxs-lookup"><span data-stu-id="91e2f-129">string</span></span><br/>  | <span data-ttu-id="91e2f-130">no definido</span><span class="sxs-lookup"><span data-stu-id="91e2f-130">undefined</span></span><br/>       |
| <span data-ttu-id="91e2f-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="91e2f-131">MaxLength</span></span><br/>    | <span data-ttu-id="91e2f-132">integer</span><span class="sxs-lookup"><span data-stu-id="91e2f-132">integer</span></span><br/> | <span data-ttu-id="91e2f-133">no definido</span><span class="sxs-lookup"><span data-stu-id="91e2f-133">undefined</span></span><br/>       |
| <span data-ttu-id="91e2f-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="91e2f-134">MinLength</span></span><br/>    | <span data-ttu-id="91e2f-135">integer</span><span class="sxs-lookup"><span data-stu-id="91e2f-135">integer</span></span><br/> | <span data-ttu-id="91e2f-136">1</span><span class="sxs-lookup"><span data-stu-id="91e2f-136">1</span></span><br/>               |
| <span data-ttu-id="91e2f-137">Mandatory</span><span class="sxs-lookup"><span data-stu-id="91e2f-137">Mandatory</span></span><br/>    | <span data-ttu-id="91e2f-138">string</span><span class="sxs-lookup"><span data-stu-id="91e2f-138">string</span></span><br/>  | <span data-ttu-id="91e2f-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="91e2f-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="91e2f-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="91e2f-140">UnitType</span></span><br/>     | <span data-ttu-id="91e2f-141">string</span><span class="sxs-lookup"><span data-stu-id="91e2f-141">string</span></span><br/>  | <span data-ttu-id="91e2f-142">caracteres</span><span class="sxs-lookup"><span data-stu-id="91e2f-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="91e2f-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91e2f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91e2f-144">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="91e2f-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




