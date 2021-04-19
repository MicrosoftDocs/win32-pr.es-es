---
title: CDM_GETFOLDERPATH mensaje (Commdlg.h)
description: Recupera la ruta de acceso de la carpeta o directorio abierto actualmente para un cuadro de diálogo Abrir o Guardar como de estilo explorador.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH diálogo de mensaje
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd6a824892b1a3a31339e36e6a783bb00c08534
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590942"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="746c0-104">Mensaje \_ GETFOLDERPATH de CDM</span><span class="sxs-lookup"><span data-stu-id="746c0-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="746c0-105">\[A partir de Windows Vista, **los** cuadros **de** diálogo Abrir y Guardar como comunes se han reemplazado por el cuadro [de diálogo de elemento común](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="746c0-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="746c0-106">Se recomienda usar Common Item Dialog API en lugar de estos cuadros de diálogo de la biblioteca de cuadros de diálogo común.\]</span><span class="sxs-lookup"><span data-stu-id="746c0-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="746c0-107">Recupera la ruta de acceso de la carpeta  o directorio abierto actualmente para un cuadro de diálogo Abrir o Guardar **como** de estilo explorador.</span><span class="sxs-lookup"><span data-stu-id="746c0-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="746c0-108">El cuadro de diálogo se debe haber creado con la **marca OFN \_ EXPLORER;** de lo contrario, se produce un error en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="746c0-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="746c0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="746c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="746c0-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="746c0-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="746c0-111">Tamaño, en caracteres, del búfer *lParam.*</span><span class="sxs-lookup"><span data-stu-id="746c0-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="746c0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="746c0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="746c0-113">Puntero al búfer que recibe la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="746c0-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="746c0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="746c0-114">Return value</span></span>

<span data-ttu-id="746c0-115">Si el mensaje se realiza correctamente, el valor devuelto es el tamaño, en caracteres, de la cadena de ruta de acceso, incluido el carácter nulo final.</span><span class="sxs-lookup"><span data-stu-id="746c0-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="746c0-116">Este es el número de bytes o caracteres copiados en el búfer o el tamaño de búfer necesario si el búfer es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="746c0-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="746c0-117">Si se produce un error, el valor devuelto es menor que cero.</span><span class="sxs-lookup"><span data-stu-id="746c0-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="746c0-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="746c0-118">Remarks</span></span>

<span data-ttu-id="746c0-119">La macro correspondiente es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="746c0-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="746c0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="746c0-120">Requirements</span></span>



| <span data-ttu-id="746c0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="746c0-121">Requirement</span></span> | <span data-ttu-id="746c0-122">Value</span><span class="sxs-lookup"><span data-stu-id="746c0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="746c0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="746c0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="746c0-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="746c0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="746c0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="746c0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="746c0-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="746c0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="746c0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="746c0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="746c0-128"><dt>Commdlg.h (incluye Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="746c0-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="746c0-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="746c0-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="746c0-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="746c0-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="746c0-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="746c0-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="746c0-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="746c0-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="746c0-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="746c0-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="746c0-134">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="746c0-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="746c0-135">Biblioteca común de cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="746c0-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

