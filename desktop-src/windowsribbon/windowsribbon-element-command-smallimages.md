---
title: Command. SmallImages (propiedad)
description: Representa un contenedor de imágenes; en este caso, imágenes pequeñas.
ms.assetid: 15c00e61-543a-4cc8-b329-516985d02359
keywords:
- Command. SmallImages (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Command.SmallImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18556cf519c21b01c3e80b63cbfc9cdf9d7d153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492515"
---
# <a name="commandsmallimages-property"></a><span data-ttu-id="d163c-104">Command. SmallImages (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d163c-104">Command.SmallImages property</span></span>

<span data-ttu-id="d163c-105">Representa un contenedor de imágenes; en este caso, imágenes pequeñas.</span><span class="sxs-lookup"><span data-stu-id="d163c-105">Represents a container of images; in this case, small images.</span></span>

## <a name="usage"></a><span data-ttu-id="d163c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="d163c-106">Usage</span></span>

``` syntax
<Command.SmallImages>
  child elements
</Command.SmallImages>
```

## <a name="attributes"></a><span data-ttu-id="d163c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d163c-107">Attributes</span></span>

<span data-ttu-id="d163c-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="d163c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d163c-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d163c-109">Child elements</span></span>



| <span data-ttu-id="d163c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="d163c-110">Element</span></span>                                                 | <span data-ttu-id="d163c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d163c-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d163c-112">**Imagen**</span><span class="sxs-lookup"><span data-stu-id="d163c-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="d163c-113">Puede producirse una o varias veces</span><span class="sxs-lookup"><span data-stu-id="d163c-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d163c-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d163c-114">Parent elements</span></span>



| <span data-ttu-id="d163c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="d163c-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="d163c-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="d163c-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d163c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d163c-117">Remarks</span></span>

<span data-ttu-id="d163c-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d163c-118">Optional.</span></span>

<span data-ttu-id="d163c-119">Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="d163c-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="d163c-120">Los recursos de imagen deben cumplir el formato de gráficos de mapa de bits estándar (BMP) usado en Windows.</span><span class="sxs-lookup"><span data-stu-id="d163c-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="d163c-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d163c-121">Examples</span></span>

<span data-ttu-id="d163c-122">En el ejemplo siguiente se muestra el marcado básico para [**splitButton**](windowsribbon-element-splitbutton.md) con un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="d163c-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="d163c-123">En esta sección de código se muestran las declaraciones de comandos [**splitButton**](windowsribbon-element-splitbutton.md) y [**MenuGroup**](windowsribbon-element-menugroup.md) con un recurso de imagen grande y pequeño.</span><span class="sxs-lookup"><span data-stu-id="d163c-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="d163c-124">También se declara un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario para el elemento **splitButton** .</span><span class="sxs-lookup"><span data-stu-id="d163c-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a><span data-ttu-id="d163c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d163c-125">Requirements</span></span>



| <span data-ttu-id="d163c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d163c-126">Requirement</span></span> | <span data-ttu-id="d163c-127">Value</span><span class="sxs-lookup"><span data-stu-id="d163c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d163c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d163c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d163c-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d163c-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d163c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d163c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d163c-131">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d163c-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d163c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d163c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d163c-133">Especificar recursos de imagen de cinta</span><span class="sxs-lookup"><span data-stu-id="d163c-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="d163c-134">UI \_ PKEY \_ SmallImage</span><span class="sxs-lookup"><span data-stu-id="d163c-134">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> </dl>

 

 





