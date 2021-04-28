---
description: 'Método IShellDispatch4.WindowsSecurity: muestra el Seguridad de Windows diálogo.'
title: Método IShellDispatch4.WindowsSecurity (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 2d7e8cfbd1e7a2a2392b78487c6a58b62de6df6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116813"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="ad9ce-103">Método IShellDispatch4.WindowsSecurity</span><span class="sxs-lookup"><span data-stu-id="ad9ce-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="ad9ce-104">Muestra el **cuadro Seguridad de Windows** de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ad9ce-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad9ce-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="ad9ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad9ce-106">Parameters</span></span>

<span data-ttu-id="ad9ce-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ad9ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad9ce-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad9ce-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ad9ce-109">JScript</span><span class="sxs-lookup"><span data-stu-id="ad9ce-109">JScript</span></span>

<span data-ttu-id="ad9ce-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ad9ce-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="ad9ce-111">VB</span><span class="sxs-lookup"><span data-stu-id="ad9ce-111">VB</span></span>

<span data-ttu-id="ad9ce-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ad9ce-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad9ce-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad9ce-113">Remarks</span></span>

<span data-ttu-id="ad9ce-114">Este método muestra el cuadro de diálogo que se muestra después de presionar CTRL+ALT+SUPR o usar la opción de seguridad en el **menú** Inicio.</span><span class="sxs-lookup"><span data-stu-id="ad9ce-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="ad9ce-115">Este método solo se puede usar cuando se conecta mediante una sesión de terminal a Microsoft Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="ad9ce-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ad9ce-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ad9ce-116">Examples</span></span>

<span data-ttu-id="ad9ce-117">En los ejemplos siguientes se muestra el uso de **WindowsSecurity** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ad9ce-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ad9ce-118">Jscript:</span><span class="sxs-lookup"><span data-stu-id="ad9ce-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="ad9ce-119">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="ad9ce-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ad9ce-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ad9ce-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ad9ce-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad9ce-121">Requirements</span></span>



| <span data-ttu-id="ad9ce-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad9ce-122">Requirement</span></span> | <span data-ttu-id="ad9ce-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ad9ce-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9ce-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad9ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ad9ce-125">Solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="ad9ce-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ad9ce-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad9ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ad9ce-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad9ce-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ad9ce-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad9ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad9ce-129"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ad9ce-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ad9ce-130">Idl</span><span class="sxs-lookup"><span data-stu-id="ad9ce-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ad9ce-131"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ad9ce-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ad9ce-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad9ce-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad9ce-133"><dt>Shell32.dll (versión 6.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ad9ce-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




