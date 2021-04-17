---
title: Mensaje de WM_CAP_SET_SEQUENCE_SETUP (VFW. h)
description: El mensaje de configuración de la secuencia de definición de Cap de WM \_ \_ \_ \_ establece los parámetros de configuración que se usan con la captura de streaming. Puede enviar este mensaje explícitamente o mediante la macro capCaptureSetSetup.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- Mensaje de WM_CAP_SET_SEQUENCE_SETUP de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535338"
---
# <a name="wm_cap_set_sequence_setup-message"></a><span data-ttu-id="02595-105">\_Mensaje de \_ instalación de secuencia de conjunto de Cap de \_ WM \_</span><span class="sxs-lookup"><span data-stu-id="02595-105">WM\_CAP\_SET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="02595-106">El mensaje de configuración de la secuencia de definición de Cap de WM establece los parámetros de configuración que se usan con la captura de streaming. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="02595-106">The **WM\_CAP\_SET\_SEQUENCE\_SETUP** message sets the configuration parameters used with streaming capture.</span></span> <span data-ttu-id="02595-107">Puede enviar este mensaje explícitamente o mediante la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) .</span><span class="sxs-lookup"><span data-stu-id="02595-107">You can send this message explicitly or by using the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro.</span></span>


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a><span data-ttu-id="02595-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02595-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02595-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="02595-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="02595-110">Tamaño, en bytes, de la estructura a la que hace referencia **s**.</span><span class="sxs-lookup"><span data-stu-id="02595-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="02595-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span><span class="sxs-lookup"><span data-stu-id="02595-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span></span>
</dt> <dd>

<span data-ttu-id="02595-112">Puntero a una estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="02595-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02595-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02595-113">Return Value</span></span>

<span data-ttu-id="02595-114">Devuelve **true** si es correcto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="02595-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="02595-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02595-115">Remarks</span></span>

<span data-ttu-id="02595-116">Para obtener información sobre los parámetros que se usan para controlar la captura de streaming, consulte la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="02595-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="02595-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02595-117">Requirements</span></span>



| <span data-ttu-id="02595-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="02595-118">Requirement</span></span> | <span data-ttu-id="02595-119">Value</span><span class="sxs-lookup"><span data-stu-id="02595-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="02595-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02595-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02595-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="02595-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="02595-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02595-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02595-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="02595-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="02595-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02595-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="02595-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="02595-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02595-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="02595-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02595-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="02595-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="02595-128">Mensajes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="02595-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





