---
description: Especifica si está habilitado el protocolo de multidifusión de difusión de transmisión multimedia (MSB) en el origen de red.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: Propiedad MFNETSOURCE_ENABLE_MSB (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b2a49876cf504bfc4e086ab1e064e6835283a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687054"
---
# <a name="mfnetsource_enable_msb-property"></a><span data-ttu-id="a9292-103">MFNETSOURCE \_ Habilitar la \_ propiedad MSB</span><span class="sxs-lookup"><span data-stu-id="a9292-103">MFNETSOURCE\_ENABLE\_MSB property</span></span>

<span data-ttu-id="a9292-104">Especifica si está habilitado el protocolo de multidifusión de difusión de transmisión multimedia (MSB) en el origen de red.</span><span class="sxs-lookup"><span data-stu-id="a9292-104">Specifies whether the Media Stream Broadcast (MSB) multicast protocol is enabled in the network source.</span></span>



<span data-ttu-id="a9292-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a9292-105">Data type</span></span>

<span data-ttu-id="a9292-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a9292-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a9292-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a9292-107">PROPVARIANT member</span></span>

<span data-ttu-id="a9292-108">**LONG**</span><span class="sxs-lookup"><span data-stu-id="a9292-108">**LONG**</span></span>

<span data-ttu-id="a9292-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a9292-109">VT\_I4</span></span>

<span data-ttu-id="a9292-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="a9292-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a9292-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9292-111">Remarks</span></span>

<span data-ttu-id="a9292-112">La constante **MFNETSOURCE \_ enable \_ MSB** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a9292-112">The constant **MFNETSOURCE\_ENABLE\_MSB** defines the GUID for this property key.</span></span> <span data-ttu-id="a9292-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="a9292-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a9292-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="a9292-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a9292-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="a9292-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a9292-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a9292-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9292-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9292-117">Requirements</span></span>



| <span data-ttu-id="a9292-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9292-118">Requirement</span></span> | <span data-ttu-id="a9292-119">Value</span><span class="sxs-lookup"><span data-stu-id="a9292-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9292-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9292-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a9292-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9292-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a9292-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9292-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a9292-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9292-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a9292-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9292-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9292-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9292-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9292-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9292-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9292-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9292-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a9292-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9292-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a9292-129">Protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="a9292-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




