---
description: Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar. Este elemento se usa solo para implementaciones de dispositivos (hosts).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a35d6449d4e8bba0ecf79e7dc87b00dee894b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912218"
---
# <a name="thismodelmetadata-element"></a><span data-ttu-id="69d48-104">elemento thisModelMetadata</span><span class="sxs-lookup"><span data-stu-id="69d48-104">thisModelMetadata element</span></span>

<span data-ttu-id="69d48-105">Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="69d48-105">Defines the manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="69d48-106">Este elemento se usa solo para implementaciones de dispositivos (hosts).</span><span class="sxs-lookup"><span data-stu-id="69d48-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="69d48-107">Uso</span><span class="sxs-lookup"><span data-stu-id="69d48-107">Usage</span></span>

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a><span data-ttu-id="69d48-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="69d48-108">Attributes</span></span>

<span data-ttu-id="69d48-109">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="69d48-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="69d48-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="69d48-110">Child elements</span></span>



| <span data-ttu-id="69d48-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="69d48-111">Element</span></span>                                                     | <span data-ttu-id="69d48-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="69d48-112">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d48-113">**fabricante**</span><span class="sxs-lookup"><span data-stu-id="69d48-113">**manufacturer**</span></span>](manufacturer.md)<br/>             | <span data-ttu-id="69d48-114">Nombre del fabricante.</span><span class="sxs-lookup"><span data-stu-id="69d48-114">Name of the manufacturer.</span></span> <span data-ttu-id="69d48-115">Al menos uno de los [**fabricantes**](manufacturer.md) o [**manufacturerLS**](manufacturerls.md) debe estar presente en los metadatos.</span><span class="sxs-lookup"><span data-stu-id="69d48-115">At least one of [**manufacturer**](manufacturer.md) or [**manufacturerLS**](manufacturerls.md) must be present in the metadata.</span></span><br/> <br/> |
| [<span data-ttu-id="69d48-116">**manufacturerLS**</span><span class="sxs-lookup"><span data-stu-id="69d48-116">**manufacturerLS**</span></span>](manufacturerls.md)<br/>         | <span data-ttu-id="69d48-117">Versión localizada del nombre del fabricante.</span><span class="sxs-lookup"><span data-stu-id="69d48-117">Localized version of the manufacturer name.</span></span><br/> <br/>                                                                                                                 |
| [<span data-ttu-id="69d48-118">**manufacturerURL**</span><span class="sxs-lookup"><span data-stu-id="69d48-118">**manufacturerURL**</span></span>](manufacturerurl.md)<br/>       | <span data-ttu-id="69d48-119">Dirección URL del fabricante.</span><span class="sxs-lookup"><span data-stu-id="69d48-119">Manufacturer URL address.</span></span><br/> <br/>                                                                                                                                   |
| [<span data-ttu-id="69d48-120">**modelName**</span><span class="sxs-lookup"><span data-stu-id="69d48-120">**modelName**</span></span>](modelname.md)<br/>                   | <span data-ttu-id="69d48-121">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69d48-121">Name of the device.</span></span> <span data-ttu-id="69d48-122">Debe haber al menos una de [**modelName**](modelname.md) o [**modelNameLS**](modelnamels.md) en los metadatos.</span><span class="sxs-lookup"><span data-stu-id="69d48-122">At least one of [**modelName**](modelname.md) or [**modelNameLS**](modelnamels.md) must be present in the metadata.</span></span><br/> <br/>                   |
| [<span data-ttu-id="69d48-123">**modelNameLS**</span><span class="sxs-lookup"><span data-stu-id="69d48-123">**modelNameLS**</span></span>](modelnamels.md)<br/>               | <span data-ttu-id="69d48-124">Versión localizada del nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69d48-124">Localized version of the device name.</span></span><br/> <br/>                                                                                                                       |
| [<span data-ttu-id="69d48-125">**modelNumber**</span><span class="sxs-lookup"><span data-stu-id="69d48-125">**modelNumber**</span></span>](modelnumber.md)<br/>               | <span data-ttu-id="69d48-126">Número de modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69d48-126">Model number of the device.</span></span><br/> <br/>                                                                                                                                 |
| [<span data-ttu-id="69d48-127">**modelURL**</span><span class="sxs-lookup"><span data-stu-id="69d48-127">**modelURL**</span></span>](modelurl.md)<br/>                     | <span data-ttu-id="69d48-128">Dirección URL del modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69d48-128">URL address for the device model.</span></span><br/> <br/>                                                                                                                           |
| [<span data-ttu-id="69d48-129">**PnPXDeviceCategory**</span><span class="sxs-lookup"><span data-stu-id="69d48-129">**PnPXDeviceCategory**</span></span>](pnpxdevicecategory.md)<br/> | <span data-ttu-id="69d48-130">Categoría PnP-X a la que pertenece el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69d48-130">PnP-X category to which the device belongs.</span></span> <br/> <br/>                                                                                                                |
| [<span data-ttu-id="69d48-131">**presentationURL**</span><span class="sxs-lookup"><span data-stu-id="69d48-131">**presentationURL**</span></span>](presentationurl.md)<br/>       | <span data-ttu-id="69d48-132">Dirección URL de los datos de presentación del modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69d48-132">URL address of the device model's presentation data.</span></span><br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a><span data-ttu-id="69d48-133">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="69d48-133">Child element sequence</span></span>

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a><span data-ttu-id="69d48-134">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="69d48-134">Parent elements</span></span>



| <span data-ttu-id="69d48-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="69d48-135">Element</span></span>                                     | <span data-ttu-id="69d48-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="69d48-136">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d48-137">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="69d48-137">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="69d48-138">Elemento raíz de un archivo de script XML del generador de código de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="69d48-138">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="69d48-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69d48-139">Remarks</span></span>

<span data-ttu-id="69d48-140">Los metadatos del fabricante coinciden con la sección de metadatos del fabricante que se describe en el perfil del dispositivo (consulte el perfil del dispositivo para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="69d48-140">The manufacturer metadata matches the manufacturer metadata section described in the device profile (consult the device profile for details).</span></span> <span data-ttu-id="69d48-141">Se debe proporcionar el nombre del fabricante o al menos una versión localizada del nombre del fabricante.</span><span class="sxs-lookup"><span data-stu-id="69d48-141">The manufacturer name or at least one localized version of the manufacturer name must be provided.</span></span> <span data-ttu-id="69d48-142">Se debe proporcionar el nombre del modelo o al menos una versión localizada del nombre del modelo.</span><span class="sxs-lookup"><span data-stu-id="69d48-142">The model name or at least one localized version of the model name must be provided.</span></span>

<span data-ttu-id="69d48-143">El elemento [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) se usa posteriormente para generar una constante de C que contiene esta información.</span><span class="sxs-lookup"><span data-stu-id="69d48-143">The [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md) element is subsequently used to generate a C constant containing this information.</span></span>

<span data-ttu-id="69d48-144">Si hay un elemento [**PnPXDeviceCategory**](pnpxdevicecategory.md) , al menos un elemento [**hospedado**](hosted.md) debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId**](pnpxcompatibleid.md) .</span><span class="sxs-lookup"><span data-stu-id="69d48-144">If a [**PnPXDeviceCategory**](pnpxdevicecategory.md) element is present, then at least one [**hosted**](hosted.md) element must contain both [**PnPXHardwareId**](pnpxhardwareid.md) and [**PnPXCompatibleId**](pnpxcompatibleid.md) elements.</span></span> <span data-ttu-id="69d48-145">Del mismo modo, si los elementos **PnPXHardwareId** y **PnPXCompatibleId** están presentes en un elemento **hospedado** , un elemento **PnPXDeviceCategory** debe estar presente dentro del elemento **thisModelMetadata** .</span><span class="sxs-lookup"><span data-stu-id="69d48-145">Similarly, if **PnPXHardwareId** and **PnPXCompatibleId** elements are present in a **hosted** element, a **PnPXDeviceCategory** element must be present inside the **thisModelMetadata** element.</span></span>

## <a name="element-information"></a><span data-ttu-id="69d48-146">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="69d48-146">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="69d48-147">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69d48-147">Minimum supported system</span></span><br/> | <span data-ttu-id="69d48-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69d48-148">Windows Vista</span></span> |
| <span data-ttu-id="69d48-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="69d48-149">Can be empty</span></span>                        | <span data-ttu-id="69d48-150">No</span><span class="sxs-lookup"><span data-stu-id="69d48-150">No</span></span>            |



 

 




