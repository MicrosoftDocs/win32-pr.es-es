---
title: CDN_INCLUDEITEM de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como para determinar si el cuadro de diálogo debe mostrar un elemento en la lista de elementos de una carpeta de shell.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- CDN_INCLUDEITEM de diálogo del código de notificación
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f25ea90f8eb37c829cdc86e89f6d7e8cad2312
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549260"
---
# <a name="cdn_includeitem-notification-code"></a><span data-ttu-id="c1e1d-104">Código de notificación INCLUDEITEM de CDN \_</span><span class="sxs-lookup"><span data-stu-id="c1e1d-104">CDN\_INCLUDEITEM notification code</span></span>

<span data-ttu-id="c1e1d-105">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c1e1d-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="c1e1d-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="c1e1d-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="c1e1d-107">Enviado por **un cuadro de** diálogo Abrir o Guardar como para determinar si el cuadro de diálogo debe mostrar un elemento en la lista de elementos de una carpeta de shell. </span><span class="sxs-lookup"><span data-stu-id="c1e1d-107">Sent by an **Open** or **Save As** dialog box to determine whether the dialog box should display an item in a shell folder's item list.</span></span> <span data-ttu-id="c1e1d-108">Cuando el usuario abre una carpeta, el cuadro de diálogo envía una notificación **\_ INCLUDEITEM** de CDN para cada elemento de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-108">When the user opens a folder, the dialog box sends a **CDN\_INCLUDEITEM** notification for each item in the folder.</span></span> <span data-ttu-id="c1e1d-109">El cuadro de diálogo envía esta notificación solo si se estableció la marca **OFN \_ ENABLEINCLUDENOTIFY** cuando se creó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-109">The dialog box sends this notification only if the **OFN\_ENABLEINCLUDENOTIFY** flag was set when the dialog box was created.</span></span>

<span data-ttu-id="c1e1d-110">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="c1e1d-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a><span data-ttu-id="c1e1d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1e1d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e1d-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1e1d-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1e1d-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1e1d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1e1d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1e1d-115">Puntero a una [**estructura OFNOTIFYEX.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)</span><span class="sxs-lookup"><span data-stu-id="c1e1d-115">A pointer to an [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure.</span></span>

<span data-ttu-id="c1e1d-116">La [**estructura OFNOTIFYEX contiene**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación \_ INCLUDEITEM de CDN.**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-116">The [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INCLUDEITEM** notification message.</span></span>

<span data-ttu-id="c1e1d-117">El **miembro psf** de la [**estructura OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) es un puntero a una interfaz para la carpeta cuyos elementos se enumeran.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-117">The **psf** member of the [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) structure is a pointer to an interface for the folder whose items are being enumerated.</span></span> <span data-ttu-id="c1e1d-118">El **miembro pidl** es un puntero a una lista de identificadores de elemento que identifica el elemento relativo a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-118">The **pidl** member is a pointer to an item identifier list that identifies the item relative to the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e1d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1e1d-119">Return value</span></span>

<span data-ttu-id="c1e1d-120">Si el [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) devuelve cero, el cuadro de diálogo excluye el elemento de la lista de elementos.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-120">If the [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure returns zero, the dialog box excludes the item from the list of items.</span></span>

<span data-ttu-id="c1e1d-121">Para incluir el elemento, devuelva un valor distinto de cero del procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-121">To include the item, return a nonzero value from the hook procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e1d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1e1d-122">Remarks</span></span>

<span data-ttu-id="c1e1d-123">El cuadro de diálogo siempre incluye elementos que tienen los atributos **SFGAO \_ FILESYSTEM** y **SFGAO \_ FILESYSANCESTOR,** independientemente del valor devuelto por **\_ CDN INCLUDEITEM**.</span><span class="sxs-lookup"><span data-stu-id="c1e1d-123">The dialog box always includes items that have both the **SFGAO\_FILESYSTEM** and **SFGAO\_FILESYSANCESTOR** attributes, regardless of the value returned by **CDN\_INCLUDEITEM**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e1d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1e1d-124">Requirements</span></span>



| <span data-ttu-id="c1e1d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1e1d-125">Requirement</span></span> | <span data-ttu-id="c1e1d-126">Value</span><span class="sxs-lookup"><span data-stu-id="c1e1d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e1d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1e1d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e1d-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c1e1d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c1e1d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1e1d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e1d-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c1e1d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1e1d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1e1d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e1d-132"><dt>Commdlg.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1e1d-132"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e1d-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c1e1d-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1e1d-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1e1d-135">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-135">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="c1e1d-136">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-136">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="c1e1d-137">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="c1e1d-137">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="c1e1d-138">**OFNOTIFYEX**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-138">**OFNOTIFYEX**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

<span data-ttu-id="c1e1d-139">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="c1e1d-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1e1d-140">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="c1e1d-140">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

