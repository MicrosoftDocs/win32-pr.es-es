---
description: La función MsiGetPatchFileList y la propiedad PatchFiles del objeto de instalador toman una lista de Windows Installer revisiones (archivos. msp) y devuelven una lista de archivos que las revisiones pueden actualizar.
ms.assetid: cc2eb506-c1fc-4125-b98c-12221b918e23
title: Enumerar los archivos que se pueden actualizar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c15872cce902f5a9059d4256e9e5c30ecff213f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687824"
---
# <a name="listing-the-files-that-can-be-updated"></a><span data-ttu-id="4729a-103">Enumerar los archivos que se pueden actualizar</span><span class="sxs-lookup"><span data-stu-id="4729a-103">Listing the Files that can be Updated</span></span>

<span data-ttu-id="4729a-104">La función [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) y la propiedad [**PatchFiles**](installer-patchfiles.md) del [**objeto de instalador**](installer-object.md) toman una lista de Windows Installer revisiones (archivos. msp) y devuelven una lista de archivos que las revisiones pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="4729a-104">The [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) function and [**PatchFiles**](installer-patchfiles.md) property of the [**Installer Object**](installer-object.md) take a list of Windows Installer patches (.msp files) and return a list of files that can be updated by the patches.</span></span> <span data-ttu-id="4729a-105">La función [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) y la propiedad [**PatchFiles**](installer-patchfiles.md) están disponibles a partir de Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="4729a-105">The [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) function and [**PatchFiles**](installer-patchfiles.md) property are available beginning with Windows Installer 4.0.</span></span>

## <a name="listing-files-that-can-be-updated"></a><span data-ttu-id="4729a-106">Enumerar archivos que se pueden actualizar</span><span class="sxs-lookup"><span data-stu-id="4729a-106">Listing Files that can be Updated</span></span>

<span data-ttu-id="4729a-107">En el ejemplo siguiente se muestra cómo extraer la información de aplicabilidad de una lista de revisiones de Windows Installer (archivos. msp) mediante [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span><span class="sxs-lookup"><span data-stu-id="4729a-107">The following example shows you how to extract the applicability information for a list of Windows Installer patches (.msp files) using [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="4729a-108">La función **MsiGetPatchFileList** proporciona el código de producto para el destino de las revisiones y una lista de archivos. MSP delimitados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="4729a-108">The **MsiGetPatchFileList** function is provided the product code for the target of the patches and a list of .msp files delimited by semicolons.</span></span> <span data-ttu-id="4729a-109">En este ejemplo se requiere Windows Installer 4,0 que se ejecute en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4729a-109">This example requires Windows Installer 4.0 running on Windows Vista.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")
#pragma comment(lib, "shell32.lib")

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles);

int __cdecl main()
{
    UINT uiRet = ERROR_SUCCESS;
    int argc;
    WCHAR** argv = CommandLineToArgvW(GetCommandLine(), &argc);
    
    MSIHANDLE *phFileListRec = NULL;
    DWORD dwcFiles = 0;
    WCHAR* szProductCode = argv[1];
    WCHAR* szPatchFileList = argv[2];
    if(ERROR_SUCCESS != (uiRet = MsiGetPatchFileList(szProductCode, szPatchFileList, &dwcFiles, &phFileListRec)))
    {
        printf("MsiGetPatchFileListW(%S, ...) Failed with:%d", szProductCode, uiRet);
        return uiRet;
    }
    
    DWORD cchBuf = 1;
    DWORD cchBufSize = 1;
    WCHAR* szBuf = new WCHAR[cchBufSize];
    if (!szBuf)
    {
        printf("Failed to allocate memory");
        CloseMsiHandles(phFileListRec, dwcFiles);
        return ERROR_OUTOFMEMORY;
    }
    memset(szBuf, 0, sizeof(WCHAR)*cchBufSize);
    
    for(unsigned int i = 0; i < dwcFiles; i++)
    {
        cchBuf = cchBufSize;
        while(ERROR_MORE_DATA == (uiRet = MsiRecordGetString(phFileListRec[i], 0, szBuf, &cchBuf)))
        {
            if (szBuf)
                delete[] szBuf;
            cchBufSize = ++cchBuf;
            szBuf = new WCHAR[cchBufSize];
            if (!szBuf)
            {
                printf("Failed to allocate memory");
                CloseMsiHandles(phFileListRec, dwcFiles);
                return ERROR_OUTOFMEMORY;
            }
        }
        
        if(uiRet != ERROR_SUCCESS)
        {
            printf("MsiRecordGetString(phFileListRec[%d] with %d", i, uiRet);
            CloseMsiHandles(phFileListRec, dwcFiles);
            if (szBuf)
                delete[] szBuf;
            return uiRet;
        }
        else
        {
            printf("File %d:%S\n", i, szBuf);
        }            
    }

    CloseMsiHandles(phFileListRec, dwcFiles);
    if (szBuf)
        delete[] szBuf;
    return 0;
}

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles)
{
    if (!phFileListRec)
        return;
    
    for (unsigned int i = 0; i < dwcFiles; i++)
    {
        if (phFileListRec[i])
            MsiCloseHandle(phFileListRec[i]);
    }    
}
//
```



<span data-ttu-id="4729a-110">En el ejemplo siguiente se muestra cómo extraer la información de aplicabilidad de una lista de revisiones de Windows Installer (archivos. msp) mediante la propiedad [**PatchFiles**](installer-patchfiles.md) del [**objeto Installer**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="4729a-110">The following example shows you how to extract the applicability information for a list of Windows Installer patches (.msp files) using [**PatchFiles**](installer-patchfiles.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="4729a-111">La propiedad **PatchFiles** proporciona el código de producto para el destino de las revisiones y una lista de archivos. MSP delimitados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="4729a-111">The **PatchFiles** property is provided the product code for the target of the patches and a list of .msp files delimited by semicolons.</span></span> <span data-ttu-id="4729a-112">En este ejemplo se requiere Windows Installer 4,0 que se ejecute en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4729a-112">This example requires Windows Installer 4.0 running on Windows Vista.</span></span>


```VB
Dim FileList
Dim installer : Set installer = Nothing
Dim argCount:argCount = Wscript.Arguments.Count

Set installer = Wscript.CreateObject("WindowsInstaller.Installer")

If (argCount > 0) Then
    sProdCode = Wscript.Arguments(0)
    sPatchPckgPath = Wscript.Arguments(1)
    Set FileList = installer.PatchFiles (sProdCode, sPatchPckgPath)
    For each File in FileList
           Wscript.Echo "Affected file: " & File
    Next
Else
    Usage
End If

Sub Usage
    Wscript.Echo "Windows Installer utility to list files updated by a patch for an installed product" &_
    vbNewLine & " 1st argument is the product code (GUID) of an installed product" &_
    vbNewLine & " 2nd argument is the list of patches" &_
    vbNewLine &_
    vbNewLine & "Copyright (C) Microsoft. All rights reserved."
    Wscript.Quit 1
End Sub
```



 

 



