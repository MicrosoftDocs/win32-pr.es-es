---
title: CDN_SELCHANGE de notificación (Commdlg.h)
description: Enviado por un cuadro de diálogo Abrir o Guardar como de estilo explorador cuando cambia la selección en el cuadro de lista que muestra el contenido de la carpeta o directorio abierto actualmente.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE cuadros de diálogo de código de notificación
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a5c7aed47d02fb7c7fcf2232b144e7a99e7c46
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590762"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="74b09-104">Código de notificación \_ SELCHANGE de CDN</span><span class="sxs-lookup"><span data-stu-id="74b09-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="74b09-105">\[A partir de Windows Vista, **los** cuadros **de** diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo de elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="74b09-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="74b09-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]</span><span class="sxs-lookup"><span data-stu-id="74b09-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="74b09-107">Enviado por un  cuadro de diálogo Abrir o Guardar **como** de estilo explorador cuando cambia la selección en el cuadro de lista que muestra el contenido de la carpeta o directorio abierto actualmente.</span><span class="sxs-lookup"><span data-stu-id="74b09-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="74b09-108">El [*procedimiento de enlace OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) recibe este mensaje en forma de mensaje WM [**\_ NOTIFY.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="74b09-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="74b09-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74b09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74b09-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74b09-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74b09-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="74b09-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74b09-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74b09-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74b09-113">Puntero a una [**estructura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="74b09-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="74b09-114">La **estructura OFNOTIFY contiene** una estructura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) **cuyo** miembro de código indica el mensaje de **notificación \_ SELCHANGE de CDN.**</span><span class="sxs-lookup"><span data-stu-id="74b09-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74b09-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74b09-115">Return value</span></span>

<span data-ttu-id="74b09-116">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="74b09-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="74b09-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74b09-117">Remarks</span></span>

<span data-ttu-id="74b09-118">El sistema envía esta notificación solo si el cuadro de diálogo se creó con el **valor OFN \_ EXPLORER.**</span><span class="sxs-lookup"><span data-stu-id="74b09-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="74b09-119">Para obtener el nombre del archivo o carpeta recién seleccionados, el procedimiento de enlace puede enviar el mensaje [**\_ GETFILEPATH**](cdm-getfilepath.md) o [**\_ CDM GETSPEC**](cdm-getspec.md) de CDM al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="74b09-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="74b09-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b09-120">Requirements</span></span>



| <span data-ttu-id="74b09-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="74b09-121">Requirement</span></span> | <span data-ttu-id="74b09-122">Value</span><span class="sxs-lookup"><span data-stu-id="74b09-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b09-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74b09-123">Minimum supported client</span></span><br/> | <span data-ttu-id="74b09-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="74b09-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="74b09-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74b09-125">Minimum supported server</span></span><br/> | <span data-ttu-id="74b09-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74b09-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74b09-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74b09-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="74b09-128"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="74b09-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74b09-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="74b09-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="74b09-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="74b09-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74b09-131">**GETFILEPATH de CDM \_**</span><span class="sxs-lookup"><span data-stu-id="74b09-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="74b09-132">**GETSPEC de CDM \_**</span><span class="sxs-lookup"><span data-stu-id="74b09-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="74b09-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="74b09-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="74b09-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="74b09-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="74b09-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="74b09-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="74b09-136">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="74b09-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="74b09-137">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="74b09-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="74b09-138">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="74b09-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

