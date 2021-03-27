---
description: Muestra el cuadro de diálogo cerrar Windows. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar apagar.
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: Método IShellDispatch. ShutdownWindows (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c111e1b740857337953cdcdf81735a8c0568ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997288"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="11af6-104">IShellDispatch. ShutdownWindows, método</span><span class="sxs-lookup"><span data-stu-id="11af6-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="11af6-105">Muestra el cuadro de diálogo **cerrar Windows** .</span><span class="sxs-lookup"><span data-stu-id="11af6-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="11af6-106">Esto es lo mismo que hacer clic en el menú **Inicio** y seleccionar **apagar**.</span><span class="sxs-lookup"><span data-stu-id="11af6-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11af6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11af6-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="11af6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11af6-108">Parameters</span></span>

<span data-ttu-id="11af6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="11af6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11af6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11af6-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="11af6-111">JScript</span><span class="sxs-lookup"><span data-stu-id="11af6-111">JScript</span></span>

<span data-ttu-id="11af6-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="11af6-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="11af6-113">VB</span><span class="sxs-lookup"><span data-stu-id="11af6-113">VB</span></span>

<span data-ttu-id="11af6-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="11af6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11af6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11af6-115">Remarks</span></span>

<span data-ttu-id="11af6-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. ShutdownWindows**](shell-shutdownwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="11af6-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="11af6-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="11af6-117">Examples</span></span>

<span data-ttu-id="11af6-118">En el ejemplo siguiente se muestra el uso de **ShutdownWindows** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="11af6-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="11af6-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="11af6-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="11af6-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="11af6-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="11af6-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="11af6-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="11af6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11af6-122">Requirements</span></span>



| <span data-ttu-id="11af6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="11af6-123">Requirement</span></span> | <span data-ttu-id="11af6-124">Value</span><span class="sxs-lookup"><span data-stu-id="11af6-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11af6-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11af6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="11af6-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="11af6-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="11af6-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11af6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="11af6-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11af6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="11af6-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11af6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="11af6-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11af6-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="11af6-131">IDL</span><span class="sxs-lookup"><span data-stu-id="11af6-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11af6-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11af6-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="11af6-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11af6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11af6-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="11af6-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




