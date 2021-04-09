---
title: Código de notificación de TBN_RESET (commctrl. h)
description: Notifica a la ventana primaria de la barra de herramientas que el usuario ha restablecido el contenido del cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- TBN_RESET controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079713"
---
# <a name="tbn_reset-notification-code"></a><span data-ttu-id="685a1-105">Código de notificación de restablecimiento de TBN \_</span><span class="sxs-lookup"><span data-stu-id="685a1-105">TBN\_RESET notification code</span></span>

<span data-ttu-id="685a1-106">Notifica a la ventana primaria de la barra de herramientas que el usuario ha restablecido el contenido del cuadro de diálogo Personalizar barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="685a1-106">Notifies the toolbar's parent window that the user has reset the content of the Customize Toolbar dialog box.</span></span> <span data-ttu-id="685a1-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="685a1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="685a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="685a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="685a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="685a1-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="685a1-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685a1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="685a1-111">Return value</span></span>

<span data-ttu-id="685a1-112">Vuelva TBNRF \_ ENDCUSTOMIZE para cerrar el cuadro de diálogo Personalizar barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="685a1-112">Return TBNRF\_ENDCUSTOMIZE to close the Customize Toolbar dialog box.</span></span> <span data-ttu-id="685a1-113">Se omiten todos los demás valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="685a1-113">All other return values are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="685a1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="685a1-114">Requirements</span></span>



| <span data-ttu-id="685a1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="685a1-115">Requirement</span></span> | <span data-ttu-id="685a1-116">Value</span><span class="sxs-lookup"><span data-stu-id="685a1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="685a1-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="685a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="685a1-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="685a1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="685a1-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="685a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="685a1-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="685a1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="685a1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="685a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="685a1-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="685a1-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





