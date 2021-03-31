---
title: Código de notificación de TBN_MAPACCELERATOR (commctrl. h)
description: Solicita el índice del botón en la barra de herramientas correspondiente al carácter acelerador especificado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995923"
---
# <a name="tbn_mapaccelerator-notification-code"></a><span data-ttu-id="22c7c-105">Código de notificación de MAPACCELERATOR de TBN \_</span><span class="sxs-lookup"><span data-stu-id="22c7c-105">TBN\_MAPACCELERATOR notification code</span></span>

<span data-ttu-id="22c7c-106">Solicita el índice del botón en la barra de herramientas correspondiente al carácter acelerador especificado.</span><span class="sxs-lookup"><span data-stu-id="22c7c-106">Requests the index of the button in the toolbar corresponding to the specified accelerator character.</span></span> <span data-ttu-id="22c7c-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="22c7c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="22c7c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22c7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c7c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22c7c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22c7c-110">Puntero a una estructura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) que contiene el carácter de tecla de aceleración y que recibe el índice del botón correspondiente.</span><span class="sxs-lookup"><span data-stu-id="22c7c-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains the accelerator key character and that receives the index of the corresponding button.</span></span> <span data-ttu-id="22c7c-111">El campo **dwItemNext** es-1 si el acelerador no se corresponde con un comando.</span><span class="sxs-lookup"><span data-stu-id="22c7c-111">The **dwItemNext** field is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c7c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22c7c-112">Return value</span></span>

<span data-ttu-id="22c7c-113">TRUE si **NMCHAR. dwItemNext** está establecido en un valor.</span><span class="sxs-lookup"><span data-stu-id="22c7c-113">TRUE if **NMCHAR.dwItemNext** is set to a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c7c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c7c-114">Requirements</span></span>



| <span data-ttu-id="22c7c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c7c-115">Requirement</span></span> | <span data-ttu-id="22c7c-116">Value</span><span class="sxs-lookup"><span data-stu-id="22c7c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22c7c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22c7c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="22c7c-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22c7c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22c7c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22c7c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="22c7c-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="22c7c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22c7c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22c7c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="22c7c-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22c7c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





