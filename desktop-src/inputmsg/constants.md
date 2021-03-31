---
title: Constantes
description: En los temas de esta sección se proporcionan las especificaciones de referencia para los mensajes de entrada de puntero y las constantes de notificaciones.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 26fbcc479a339cee67e578803c6feed228736a90
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077660"
---
# <a name="constants"></a><span data-ttu-id="ccb25-103">Constantes</span><span class="sxs-lookup"><span data-stu-id="ccb25-103">Constants</span></span>

<span data-ttu-id="ccb25-104">En los temas de esta sección se proporcionan las especificaciones de referencia para [los mensajes de entrada de puntero y](messages-and-notifications-portal.md) las constantes de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ccb25-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) constants.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ccb25-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ccb25-105">In this section</span></span>



| <span data-ttu-id="ccb25-106">Tema</span><span class="sxs-lookup"><span data-stu-id="ccb25-106">Topic</span></span>                                                                             | <span data-ttu-id="ccb25-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccb25-107">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccb25-108">**Estado de la tecla modificadora**</span><span class="sxs-lookup"><span data-stu-id="ccb25-108">**Modifier Key State**</span></span>](modifier-key-states-constants.md)<br/>            | <span data-ttu-id="ccb25-109">Indica qué teclas modificadoras de teclado se presionaron en el momento en que se generó la entrada.</span><span class="sxs-lookup"><span data-stu-id="ccb25-109">Indicates which keyboard modifier keys were pressed at the time input was being generated.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="ccb25-110">**Marcas de lápiz**</span><span class="sxs-lookup"><span data-stu-id="ccb25-110">**Pen Flags**</span></span>](pen-flags-constants.md)<br/>                               | <span data-ttu-id="ccb25-111">Valores que pueden aparecer en el campo **penFlags** de la estructura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ccb25-111">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                         |
| [<span data-ttu-id="ccb25-112">**Máscara de lápiz**</span><span class="sxs-lookup"><span data-stu-id="ccb25-112">**Pen Mask**</span></span>](pen-mask-constants.md)<br/>                                 | <span data-ttu-id="ccb25-113">Valores que pueden aparecer en el campo **penMask** de la estructura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ccb25-113">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                          |
| [<span data-ttu-id="ccb25-114">**Cambio de puntero de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="ccb25-114">**Pointer Device Change**</span></span>](pointer-device-change-constants.md)<br/>       | <span data-ttu-id="ccb25-115">Valores que se pueden pasar en el parámetro *wParam* del mensaje de [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="ccb25-115">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span><br/>                                                                    |
| [<span data-ttu-id="ccb25-116">**Marcas de puntero**</span><span class="sxs-lookup"><span data-stu-id="ccb25-116">**Pointer Flags**</span></span>](pointer-flags-contants.md)<br/>                        | <span data-ttu-id="ccb25-117">Valores que pueden aparecer en el campo **pointerFlags** de la estructura [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ccb25-117">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                              |
| [<span data-ttu-id="ccb25-118">**Marcas de mensajes de puntero**</span><span class="sxs-lookup"><span data-stu-id="ccb25-118">**Pointer Message Flags**</span></span>](pointer-message-flags.md)<br/>                 | <span data-ttu-id="ccb25-119">Valores que se usan en varias macros de puntero (vea [macros](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="ccb25-119">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="ccb25-120">**Marcas táctiles**</span><span class="sxs-lookup"><span data-stu-id="ccb25-120">**Touch Flags**</span></span>](touch-flags-constants.md)<br/>                           | <span data-ttu-id="ccb25-121">Valores que pueden aparecer en el campo **touchFlags** de la estructura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ccb25-121">Values that can appear in the **touchFlags** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                   |
| [<span data-ttu-id="ccb25-122">**Ventana de prueba de posicionamiento táctil**</span><span class="sxs-lookup"><span data-stu-id="ccb25-122">**Touch Hit Testing Window**</span></span>](touch-hit-testing-window-constants.md)<br/> | <span data-ttu-id="ccb25-123">Indica cómo las ventanas que se registran mediante la función [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) procesan los mensajes para la prueba de posicionamiento táctil.</span><span class="sxs-lookup"><span data-stu-id="ccb25-123">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span><br/> |
| [<span data-ttu-id="ccb25-124">**Máscara táctil**</span><span class="sxs-lookup"><span data-stu-id="ccb25-124">**Touch Mask**</span></span>](touch-mask-constants.md)<br/>                             | <span data-ttu-id="ccb25-125">Valores que pueden aparecer en el campo **touchMask** de la estructura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ccb25-125">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="ccb25-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ccb25-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccb25-127">Referencia de mensajes de entrada de puntero</span><span class="sxs-lookup"><span data-stu-id="ccb25-127">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

