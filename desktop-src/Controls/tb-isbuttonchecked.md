---
title: Mensaje de TB_ISBUTTONCHECKED (commctrl. h)
description: Determina si el botón especificado de una barra de herramientas está activado.
ms.assetid: ce576951-8db6-4854-8457-211ece018ce8
keywords:
- TB_ISBUTTONCHECKED controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ISBUTTONCHECKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb9bc573478ea55ce8e0bda48ff16679b135fc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533976"
---
# <a name="tb_isbuttonchecked-message"></a><span data-ttu-id="aa075-104">\_Mensaje ISBUTTONCHECKED TB</span><span class="sxs-lookup"><span data-stu-id="aa075-104">TB\_ISBUTTONCHECKED message</span></span>

<span data-ttu-id="aa075-105">Determina si el botón especificado de una barra de herramientas está activado.</span><span class="sxs-lookup"><span data-stu-id="aa075-105">Determines whether the specified button in a toolbar is checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa075-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa075-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa075-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa075-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa075-108">Identificador de comando del botón.</span><span class="sxs-lookup"><span data-stu-id="aa075-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="aa075-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa075-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="aa075-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="aa075-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa075-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa075-111">Return value</span></span>

<span data-ttu-id="aa075-112">Devuelve un valor distinto de cero si el botón está activado o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aa075-112">Returns nonzero if the button is checked, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa075-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa075-113">Requirements</span></span>



| <span data-ttu-id="aa075-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa075-114">Requirement</span></span> | <span data-ttu-id="aa075-115">Value</span><span class="sxs-lookup"><span data-stu-id="aa075-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa075-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa075-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa075-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aa075-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa075-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa075-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa075-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa075-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa075-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa075-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa075-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa075-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





