---
description: Contiene el número de elementos de la colección.
ms.assetid: 383382d5-7e3f-4b27-bebf-6b79dbe677b8
title: Propiedad FolderItems. Count (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 814a8248a54c5b58624a721f006bc8d4f974ba92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984182"
---
# <a name="folderitemscount-property"></a><span data-ttu-id="31a47-103">FolderItems. Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="31a47-103">FolderItems.Count property</span></span>

<span data-ttu-id="31a47-104">Contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="31a47-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="31a47-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="31a47-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a47-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31a47-106">Syntax</span></span>


```JScript
iCount = FolderItems.Count
```



## <a name="property-value"></a><span data-ttu-id="31a47-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="31a47-107">Property value</span></span>

<span data-ttu-id="31a47-108">Un **entero** que contiene un valor para la propiedad **Count** .</span><span class="sxs-lookup"><span data-stu-id="31a47-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="31a47-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="31a47-109">Examples</span></span>

<span data-ttu-id="31a47-110">En el ejemplo siguiente se usa **Count** para recuperar el recuento de elementos de la carpeta Windows.</span><span class="sxs-lookup"><span data-stu-id="31a47-110">The following example uses **Count** to retrieve the count of items in the Windows folder.</span></span> <span data-ttu-id="31a47-111">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="31a47-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="31a47-112">JScript.net</span><span class="sxs-lookup"><span data-stu-id="31a47-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var nCount;
                
                nCount = objFolderItems.Count;
                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="31a47-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="31a47-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="31a47-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="31a47-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="31a47-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31a47-115">Requirements</span></span>



| <span data-ttu-id="31a47-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="31a47-116">Requirement</span></span> | <span data-ttu-id="31a47-117">Value</span><span class="sxs-lookup"><span data-stu-id="31a47-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a47-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31a47-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31a47-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="31a47-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="31a47-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31a47-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31a47-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="31a47-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="31a47-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31a47-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a47-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="31a47-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="31a47-124">IDL</span><span class="sxs-lookup"><span data-stu-id="31a47-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31a47-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31a47-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="31a47-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31a47-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31a47-127"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="31a47-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




