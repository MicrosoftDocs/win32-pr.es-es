---
title: CDN_SHAREVIOLATION de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando el usuario hace clic en el botón Aceptar y se produce una infracción de uso compartido de red para el archivo seleccionado.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- CDN_SHAREVIOLATION cuadro de diálogo de código de notificación
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e79d9c48d3e80d14d83de07c03f7db119ea8e78
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590702"
---
# <a name="cdn_shareviolation-notification-code"></a><span data-ttu-id="b49d8-104">Código de notificación \_ DE SHAREVIOLATION de CDN</span><span class="sxs-lookup"><span data-stu-id="b49d8-104">CDN\_SHAREVIOLATION notification code</span></span>

<span data-ttu-id="b49d8-105">\[A partir de Windows Vista, **los** cuadros de **diálogo** Abrir y Guardar como comunes se han reemplazado por el [cuadro de diálogo Elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="b49d8-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="b49d8-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca común de cuadros de diálogo.\]</span><span class="sxs-lookup"><span data-stu-id="b49d8-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="b49d8-107">Enviado por un  cuadro de diálogo Abrir o Guardar  **como** de estilo explorador cuando el usuario hace clic en el botón Aceptar y se produce una infracción de uso compartido de red para el archivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="b49d8-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **OK** button and a network sharing violation occurs for the selected file.</span></span>

<span data-ttu-id="b49d8-108">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="b49d8-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="b49d8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b49d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b49d8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b49d8-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b49d8-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b49d8-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b49d8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b49d8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b49d8-113">Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="b49d8-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="b49d8-114">El **miembro pszFile** de esta estructura es un puntero al nombre del archivo que tenía la infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b49d8-114">The **pszFile** member of this structure is a pointer to the name of the file that had the sharing violation.</span></span> <span data-ttu-id="b49d8-115">La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de notificación **\_ SHAREVIOLATION de CDN.**</span><span class="sxs-lookup"><span data-stu-id="b49d8-115">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SHAREVIOLATION** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b49d8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b49d8-116">Return value</span></span>

<span data-ttu-id="b49d8-117">El valor devuelto indica cómo el cuadro de diálogo debe controlar la infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b49d8-117">The return value indicates how the dialog box should handle the sharing violation.</span></span>

<span data-ttu-id="b49d8-118">Si el procedimiento de enlace devuelve cero, el cuadro de diálogo muestra el mensaje de advertencia estándar para una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b49d8-118">If the hook procedure returns zero, the dialog box displays the standard warning message for a sharing violation.</span></span>

<span data-ttu-id="b49d8-119">Para evitar la presentación del mensaje de advertencia estándar, devuelva un valor distinto de cero del procedimiento de enlace y llame a la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer uno de los siguientes valores **\_ msgRESULT de DWL.**</span><span class="sxs-lookup"><span data-stu-id="b49d8-119">To prevent the display of the standard warning message, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set one of the following **DWL\_MSGRESULT** values.</span></span>



| <span data-ttu-id="b49d8-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b49d8-120">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="b49d8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b49d8-121">Description</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b49d8-122"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b49d8-122"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b49d8-123">Hace que el cuadro de diálogo devuelva el nombre de archivo sin advertir al usuario sobre la infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b49d8-123">Causes the dialog box to return the file name without warning the user about the sharing violation.</span></span><br/>  |
| <dl> <span data-ttu-id="b49d8-124"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b49d8-124"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="b49d8-125">Hace que el cuadro de diálogo rechace el nombre de archivo sin advertir al usuario sobre la infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b49d8-125">Causes the dialog box to reject the file name without warning the user about the sharing violation.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b49d8-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b49d8-126">Remarks</span></span>

<span data-ttu-id="b49d8-127">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="b49d8-127">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="b49d8-128">El sistema envía esta notificación solo si no se especificó el valor **OFN \_ SHAREAWARE** cuando se creó el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b49d8-128">The system sends this notification only if the **OFN\_SHAREAWARE** value was not specified when the dialog box was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="b49d8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b49d8-129">Requirements</span></span>



| <span data-ttu-id="b49d8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b49d8-130">Requirement</span></span> | <span data-ttu-id="b49d8-131">Value</span><span class="sxs-lookup"><span data-stu-id="b49d8-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b49d8-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b49d8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b49d8-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b49d8-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b49d8-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b49d8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b49d8-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b49d8-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b49d8-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b49d8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b49d8-137"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b49d8-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b49d8-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b49d8-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="b49d8-139">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b49d8-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b49d8-140">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b49d8-140">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b49d8-141">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="b49d8-141">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b49d8-142">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="b49d8-142">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="b49d8-143">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b49d8-143">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="b49d8-144">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b49d8-144">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="b49d8-145">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="b49d8-145">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="b49d8-146">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="b49d8-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b49d8-147">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="b49d8-147">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

