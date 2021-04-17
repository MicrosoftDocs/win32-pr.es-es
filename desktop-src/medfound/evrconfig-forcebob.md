---
description: Fuerza al representador de vídeo mejorado (EVR) a usar el desentrelazado de Bob.
ms.assetid: 56f808b3-c2eb-46e4-84a1-c478a5db78e7
title: EVRConfig_ForceBob atributo (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afeeb1e7fb57f956d378e71ac4452ea2e4f168be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705410"
---
# <a name="evrconfig_forcebob-attribute"></a><span data-ttu-id="39c38-103">\_Atributo ForceBob de EVRConfig</span><span class="sxs-lookup"><span data-stu-id="39c38-103">EVRConfig\_ForceBob attribute</span></span>

<span data-ttu-id="39c38-104">Fuerza al representador de vídeo mejorado (EVR) a usar el desentrelazado de Bob.</span><span class="sxs-lookup"><span data-stu-id="39c38-104">Forces the Enhanced Video Renderer (EVR) to use bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="39c38-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="39c38-105">Data type</span></span>

<span data-ttu-id="39c38-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="39c38-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="39c38-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="39c38-107">Get/set</span></span>

<span data-ttu-id="39c38-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="39c38-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="39c38-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="39c38-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="39c38-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39c38-110">Remarks</span></span>

<span data-ttu-id="39c38-111">Este atributo se puede establecer en el receptor de medios EVR.</span><span class="sxs-lookup"><span data-stu-id="39c38-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="39c38-112">Para establecer el atributo, utilice **QueryInterface** para consultar el receptor de medios EVR de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="39c38-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="39c38-113">Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoMixPrefs \_ FORCEBOB** en EVR.</span><span class="sxs-lookup"><span data-stu-id="39c38-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_ForceBob** flag on the EVR.</span></span> <span data-ttu-id="39c38-114">Consulte [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) para obtener una descripción de esta marca.</span><span class="sxs-lookup"><span data-stu-id="39c38-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="39c38-115">La constante GUID para este atributo se exporta desde strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="39c38-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c38-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c38-116">Requirements</span></span>



| <span data-ttu-id="39c38-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c38-117">Requirement</span></span> | <span data-ttu-id="39c38-118">Value</span><span class="sxs-lookup"><span data-stu-id="39c38-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39c38-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39c38-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39c38-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="39c38-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="39c38-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39c38-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39c38-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="39c38-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="39c38-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39c38-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c38-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c38-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c38-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="39c38-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c38-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39c38-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="39c38-127">Atributos EVR</span><span class="sxs-lookup"><span data-stu-id="39c38-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="39c38-128">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="39c38-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




