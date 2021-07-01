---
description: Busque información sobre el parámetro DocumentBindingGutter. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45839aa07d740d8498e477809b45aa823460b23f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118470"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="54e42-105">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="54e42-105">DocumentBindingGutter</span></span>

<span data-ttu-id="54e42-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="54e42-106">This topic is not current.</span></span> <span data-ttu-id="54e42-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="54e42-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="54e42-108">Especifica el ancho del medianía de enlace.</span><span class="sxs-lookup"><span data-stu-id="54e42-108">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="54e42-109">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="54e42-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="54e42-110">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="54e42-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="54e42-111">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="54e42-111">Element Information</span></span>



| <span data-ttu-id="54e42-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="54e42-112">Name</span></span> | <span data-ttu-id="54e42-113">Valor</span><span class="sxs-lookup"><span data-stu-id="54e42-113">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="54e42-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="54e42-114">Element Type</span></span> <br/>   | <span data-ttu-id="54e42-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="54e42-115">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="54e42-116">Prefijo de ámbito</span><span class="sxs-lookup"><span data-stu-id="54e42-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="54e42-117">Documento</span><span class="sxs-lookup"><span data-stu-id="54e42-117">Document</span></span><br/>                          |
| <span data-ttu-id="54e42-118">Notas</span><span class="sxs-lookup"><span data-stu-id="54e42-118">Notes</span></span> <br/>          | <span data-ttu-id="54e42-119">Vinculado al elemento DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="54e42-119">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="54e42-120">Contenido de la estructura</span><span class="sxs-lookup"><span data-stu-id="54e42-120">Structure Content</span></span>

<span data-ttu-id="54e42-121">La estructura XML de este elemento es:</span><span class="sxs-lookup"><span data-stu-id="54e42-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBindingGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="54e42-122">Propiedades de estructura</span><span class="sxs-lookup"><span data-stu-id="54e42-122">Structure Properties</span></span>

<span data-ttu-id="54e42-123">En la tabla siguiente se describen las características de las variables definidas en la estructura XML.</span><span class="sxs-lookup"><span data-stu-id="54e42-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="54e42-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54e42-124">Property</span></span>                | <span data-ttu-id="54e42-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="54e42-125">xsi:type</span></span>           | <span data-ttu-id="54e42-126">Valor</span><span class="sxs-lookup"><span data-stu-id="54e42-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="54e42-127">DataType</span><span class="sxs-lookup"><span data-stu-id="54e42-127">DataType</span></span><br/>     | <span data-ttu-id="54e42-128">string</span><span class="sxs-lookup"><span data-stu-id="54e42-128">string</span></span><br/>  | <span data-ttu-id="54e42-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="54e42-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="54e42-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="54e42-130">DefaultValue</span></span><br/> | <span data-ttu-id="54e42-131">integer</span><span class="sxs-lookup"><span data-stu-id="54e42-131">integer</span></span><br/> | <span data-ttu-id="54e42-132">no definido</span><span class="sxs-lookup"><span data-stu-id="54e42-132">undefined</span></span><br/>       |
| <span data-ttu-id="54e42-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="54e42-133">MaxValue</span></span><br/>     | <span data-ttu-id="54e42-134">integer</span><span class="sxs-lookup"><span data-stu-id="54e42-134">integer</span></span><br/> | <span data-ttu-id="54e42-135">no definido</span><span class="sxs-lookup"><span data-stu-id="54e42-135">undefined</span></span><br/>       |
| <span data-ttu-id="54e42-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="54e42-136">MinValue</span></span><br/>     | <span data-ttu-id="54e42-137">integer</span><span class="sxs-lookup"><span data-stu-id="54e42-137">integer</span></span><br/> | <span data-ttu-id="54e42-138">no definido</span><span class="sxs-lookup"><span data-stu-id="54e42-138">undefined</span></span><br/>       |
| <span data-ttu-id="54e42-139">Mandatory</span><span class="sxs-lookup"><span data-stu-id="54e42-139">Mandatory</span></span><br/>    | <span data-ttu-id="54e42-140">String</span><span class="sxs-lookup"><span data-stu-id="54e42-140">String</span></span><br/>  | <span data-ttu-id="54e42-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="54e42-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="54e42-142">Múltiple</span><span class="sxs-lookup"><span data-stu-id="54e42-142">Multiple</span></span><br/>     | <span data-ttu-id="54e42-143">integer</span><span class="sxs-lookup"><span data-stu-id="54e42-143">integer</span></span><br/> | <span data-ttu-id="54e42-144">1</span><span class="sxs-lookup"><span data-stu-id="54e42-144">1</span></span><br/>               |
| <span data-ttu-id="54e42-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="54e42-145">UnitType</span></span><br/>     | <span data-ttu-id="54e42-146">string</span><span class="sxs-lookup"><span data-stu-id="54e42-146">string</span></span><br/>  | <span data-ttu-id="54e42-147">Micras</span><span class="sxs-lookup"><span data-stu-id="54e42-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="54e42-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54e42-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54e42-149">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="54e42-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




