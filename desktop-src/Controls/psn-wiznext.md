---
title: Código de notificación de PSN_WIZNEXT (Prsht. h)
description: Notifica a una página que el usuario ha haga clic en el botón siguiente en un asistente. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 145591b725548ffc4175541fd37db8f285533590
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658256"
---
# <a name="psn_wiznext-notification-code"></a><span data-ttu-id="19755-105">Código de notificación de WIZNEXT de PSN \_</span><span class="sxs-lookup"><span data-stu-id="19755-105">PSN\_WIZNEXT notification code</span></span>

<span data-ttu-id="19755-106">Notifica a una página que el usuario ha haga clic en el botón **siguiente** en un asistente.</span><span class="sxs-lookup"><span data-stu-id="19755-106">Notifies a page that the user has clicked the **Next** button in a wizard.</span></span> <span data-ttu-id="19755-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="19755-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="19755-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19755-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19755-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19755-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19755-110">Puntero a una estructura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contiene información sobre el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="19755-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="19755-111">Esta estructura contiene una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como su primer miembro, **HDR**. El miembro **hwndFrom** de esta estructura **NMHDR** contiene el identificador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="19755-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="19755-112">El miembro **lParam** de la estructura **PSHNOTIFY** no contiene ninguna información.</span><span class="sxs-lookup"><span data-stu-id="19755-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19755-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19755-113">Return value</span></span>

<span data-ttu-id="19755-114">Devuelve 0 para permitir que el asistente vaya a la página siguiente.</span><span class="sxs-lookup"><span data-stu-id="19755-114">Return 0 to allow the wizard to go to the next page.</span></span> <span data-ttu-id="19755-115">Devuelve-1 para evitar que el asistente cambie las páginas.</span><span class="sxs-lookup"><span data-stu-id="19755-115">Return -1 to prevent the wizard from changing pages.</span></span> <span data-ttu-id="19755-116">Para mostrar una página determinada, devuelva su identificador de recurso de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="19755-116">To display a particular page, return its dialog resource identifier.</span></span> <span data-ttu-id="19755-117">Si el cuadro de diálogo se ha especificado con la marca [**PSP \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , esta notificación devuelve el puntero a la plantilla de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="19755-117">If the dialog was specified with the [**PSP\_DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) flag, this notification returns the pointer to the dialog template.</span></span>

## <a name="remarks"></a><span data-ttu-id="19755-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19755-118">Remarks</span></span>

<span data-ttu-id="19755-119">Para establecer el valor devuelto, el procedimiento de cuadro de diálogo de la página debe llamar a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con el valor de **DWL \_ MSGRESULT** y devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="19755-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the **DWL\_MSGRESULT** value and return **TRUE**.</span></span> <span data-ttu-id="19755-120">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="19755-120">For example:</span></span>

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> <span data-ttu-id="19755-121">La hoja de propiedades está en proceso de manipular la lista de páginas cuando \_ se envía el código de notificación WIZNEXT de PSN.</span><span class="sxs-lookup"><span data-stu-id="19755-121">The property sheet is in the process of manipulating the list of pages when the PSN\_WIZNEXT notification code is sent.</span></span> <span data-ttu-id="19755-122">Puede Agregar, insertar o quitar páginas en respuesta a estos códigos de notificación, pero debe tener cuidado especial si inserta o quita páginas antes de la página actual.</span><span class="sxs-lookup"><span data-stu-id="19755-122">You can add, insert, or remove pages in response to these notification codes, but special care must be taken if you insert or remove pages before the current page.</span></span>

 

<span data-ttu-id="19755-123">Si inserta o quita páginas antes de la página actual, debe devolver (a **DWL \_ MSGRESULT**) un valor distinto de cero para especificar la nueva página deseada.</span><span class="sxs-lookup"><span data-stu-id="19755-123">If you insert or remove pages before the current page, you must return (through **DWL\_MSGRESULT**) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="19755-124">Tenga en cuenta, sin embargo, que si inserta o quita una página que se encuentra antes de la página actual (que tiene un índice más pequeño que la página actual), [PSN \_ KILLACTIVE](psn-killactive.md) podría enviarse a una página equivocada.</span><span class="sxs-lookup"><span data-stu-id="19755-124">Note, however, that if you insert or remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

<span data-ttu-id="19755-125">Por esta razón, se recomienda que los asistentes que agregan y quitan páginas dinámicamente en respuesta a PSN \_ WIZNEXT y [PSN \_ WIZBACK](psn-wizback.md) lo hagan solo en las páginas al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="19755-125">For this reason, it is recommended that wizards that add and remove pages dynamically in response to PSN\_WIZNEXT and [PSN\_WIZBACK](psn-wizback.md) do so only to pages at the end of the list.</span></span> <span data-ttu-id="19755-126">Si desea que el asistente Quite las páginas con precisión, mantenga las páginas dinámicas al final de la lista y vuelva a las páginas permanentes antes de eliminarlas.</span><span class="sxs-lookup"><span data-stu-id="19755-126">If you want your wizard to remove pages accurately, keep the dynamic pages at the end of the list and jump back to permanent pages before deleting them.</span></span>

<span data-ttu-id="19755-127">Por ejemplo, supongamos que un asistente está formado por una página de introducción, una serie de páginas dinámicas y una página de finalización, y desea eliminar las páginas dinámicas cuando el usuario llega a la página de finalización.</span><span class="sxs-lookup"><span data-stu-id="19755-127">For example, suppose a wizard consists of an introductory page, a series of dynamic pages, and a completion page, and you want to delete the dynamic pages when the user reaches the completion page.</span></span>

1.  <span data-ttu-id="19755-128">El asistente comenzaría con dos páginas: "introducción" y "finalización".</span><span class="sxs-lookup"><span data-stu-id="19755-128">The wizard would begin with two pages, "Introduction" and "Completion."</span></span> <span data-ttu-id="19755-129">El usuario comienza en la página "introducción".</span><span class="sxs-lookup"><span data-stu-id="19755-129">The user begins on the "Introduction" page.</span></span>
    1.  <span data-ttu-id="19755-130">Introducción (el usuario está aquí)</span><span class="sxs-lookup"><span data-stu-id="19755-130">Introduction (User is here)</span></span>
    2.  <span data-ttu-id="19755-131">Completion</span><span class="sxs-lookup"><span data-stu-id="19755-131">Completion</span></span>
2.  <span data-ttu-id="19755-132">Cuando el usuario sale de la "introducción", el asistente agrega las páginas dinámicas y coloca al usuario en la primera página dinámica devolviendo (a **DWL \_ MSGRESULT**) el identificador del cuadro de diálogo de la página "dinámica 1".</span><span class="sxs-lookup"><span data-stu-id="19755-132">When the user navigates away from "Introduction," the wizard adds the dynamic pages and places the user at the first dynamic page by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Dynamic 1."</span></span> <span data-ttu-id="19755-133">En este ejemplo, hay tres páginas dinámicas.</span><span class="sxs-lookup"><span data-stu-id="19755-133">In this example, there are three dynamic pages.</span></span>
    1.  <span data-ttu-id="19755-134">Introducción</span><span class="sxs-lookup"><span data-stu-id="19755-134">Introduction</span></span>
    2.  <span data-ttu-id="19755-135">Completion</span><span class="sxs-lookup"><span data-stu-id="19755-135">Completion</span></span>
    3.  <span data-ttu-id="19755-136">Dinámica 1 (el usuario está aquí)</span><span class="sxs-lookup"><span data-stu-id="19755-136">Dynamic 1 (User is here)</span></span>
    4.  <span data-ttu-id="19755-137">Dinámica 2</span><span class="sxs-lookup"><span data-stu-id="19755-137">Dynamic 2</span></span>
    5.  <span data-ttu-id="19755-138">Dinámica 3</span><span class="sxs-lookup"><span data-stu-id="19755-138">Dynamic 3</span></span>
3.  <span data-ttu-id="19755-139">Una vez que el usuario navega por las páginas dinámicas a "Dynamic 3" y, a continuación, navega a la página siguiente, la aplicación debe poner al usuario en la página "completada".</span><span class="sxs-lookup"><span data-stu-id="19755-139">After the user navigates through the dynamic pages to "Dynamic 3" and then navigates to the next page, the application should place the user at the page "Completion."</span></span> <span data-ttu-id="19755-140">De nuevo, esto se hace devolviendo (hasta **DWL \_ MSGRESULT**) el identificador del cuadro de diálogo de la página "finalización".</span><span class="sxs-lookup"><span data-stu-id="19755-140">Again, this is done by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Completion."</span></span>
    1.  <span data-ttu-id="19755-141">Introducción</span><span class="sxs-lookup"><span data-stu-id="19755-141">Introduction</span></span>
    2.  <span data-ttu-id="19755-142">Finalización (el usuario está aquí)</span><span class="sxs-lookup"><span data-stu-id="19755-142">Completion (User is here)</span></span>
    3.  <span data-ttu-id="19755-143">Dinámica 1</span><span class="sxs-lookup"><span data-stu-id="19755-143">Dynamic 1</span></span>
    4.  <span data-ttu-id="19755-144">Dinámica 2</span><span class="sxs-lookup"><span data-stu-id="19755-144">Dynamic 2</span></span>
    5.  <span data-ttu-id="19755-145">Dinámica 3</span><span class="sxs-lookup"><span data-stu-id="19755-145">Dynamic 3</span></span>
4.  <span data-ttu-id="19755-146">A continuación, la aplicación puede quitar las tres páginas dinámicas (numeradas de tres a cinco) sin ningún riesgo.</span><span class="sxs-lookup"><span data-stu-id="19755-146">The application can then remove the three dynamic pages (numbered three through five) safely.</span></span>
    1.  <span data-ttu-id="19755-147">Introducción</span><span class="sxs-lookup"><span data-stu-id="19755-147">Introduction</span></span>
    2.  <span data-ttu-id="19755-148">Finalización (el usuario está aquí)</span><span class="sxs-lookup"><span data-stu-id="19755-148">Completion (User is here)</span></span>

<span data-ttu-id="19755-149">Tenga en cuenta que esta técnica solo es necesaria si el asistente quita las páginas dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="19755-149">Note that this technique is necessary only if your wizard removes pages dynamically.</span></span> <span data-ttu-id="19755-150">Si el asistente solo agrega páginas dinámicamente, este proceso no es necesario.</span><span class="sxs-lookup"><span data-stu-id="19755-150">If your wizard only adds pages dynamically, this process is not necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="19755-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19755-151">Requirements</span></span>



| <span data-ttu-id="19755-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="19755-152">Requirement</span></span> | <span data-ttu-id="19755-153">Value</span><span class="sxs-lookup"><span data-stu-id="19755-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19755-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19755-154">Minimum supported client</span></span><br/> | <span data-ttu-id="19755-155">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19755-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19755-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19755-156">Minimum supported server</span></span><br/> | <span data-ttu-id="19755-157">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="19755-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="19755-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19755-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="19755-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="19755-159"><dt>Prsht.h</dt></span></span> </dl> |



 

