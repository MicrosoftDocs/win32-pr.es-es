---
description: Código de ejemplo que muestra cómo crear un archivo temporal para la manipulación de datos mediante las funciones GetTempFileName y GetTempPath.
ms.assetid: 6254c67d-5d34-499d-b1a4-8cac526dd294
title: Crear y usar un archivo temporal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca18b7b72aab7c53bea95c38147af66f2b7fef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686746"
---
# <a name="creating-and-using-a-temporary-file"></a><span data-ttu-id="98fa7-103">Crear y usar un archivo temporal</span><span class="sxs-lookup"><span data-stu-id="98fa7-103">Creating and Using a Temporary File</span></span>

<span data-ttu-id="98fa7-104">Las aplicaciones pueden obtener nombres de archivo y ruta de acceso únicos para los archivos temporales mediante las funciones [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) y [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) .</span><span class="sxs-lookup"><span data-stu-id="98fa7-104">Applications can obtain unique file and path names for temporary files by using the [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) and [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) functions.</span></span> <span data-ttu-id="98fa7-105">La función **GetTempFileName** genera un nombre de archivo único y la función **GetTempPath** recupera la ruta de acceso a un directorio en el que se deben crear los archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="98fa7-105">The **GetTempFileName** function generates a unique file name, and the **GetTempPath** function retrieves the path to a directory where temporary files should be created.</span></span>

<span data-ttu-id="98fa7-106">En el procedimiento siguiente se describe cómo una aplicación crea un archivo temporal para la manipulación de datos.</span><span class="sxs-lookup"><span data-stu-id="98fa7-106">The following procedure describes how an application creates a temporary file for data manipulation purposes.</span></span>

<span data-ttu-id="98fa7-107">**Para crear y usar un archivo temporal**</span><span class="sxs-lookup"><span data-stu-id="98fa7-107">**To create and use a temporary file**</span></span>

1.  <span data-ttu-id="98fa7-108">La aplicación abre el archivo de texto de origen proporcionado por el usuario mediante [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span><span class="sxs-lookup"><span data-stu-id="98fa7-108">The application opens the user-provided source text file by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span>
2.  <span data-ttu-id="98fa7-109">La aplicación recupera una ruta de acceso y un nombre de archivo temporales mediante las funciones [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) y [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) y, a continuación, usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para crear el archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="98fa7-109">The application retrieves a temporary file path and file name by using the [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) and [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) functions, and then uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to create the temporary file.</span></span>
3.  <span data-ttu-id="98fa7-110">La aplicación Lee bloques de datos de texto en un búfer, convierte el contenido del búfer en mayúsculas mediante la función [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) y escribe el búfer convertido en el archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="98fa7-110">The application reads blocks of text data into a buffer, converts the buffer contents to uppercase using the [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) function, and writes the converted buffer to the temporary file.</span></span>
4.  <span data-ttu-id="98fa7-111">Cuando todo el archivo de código fuente se escribe en el archivo temporal, la aplicación cierra ambos archivos y cambia el nombre del archivo temporal a "allcaps.txt" mediante la función [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) .</span><span class="sxs-lookup"><span data-stu-id="98fa7-111">When all of the source file is written to the temporary file, the application closes both files, and renames the temporary file to "allcaps.txt" by using the [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) function.</span></span>

<span data-ttu-id="98fa7-112">En cada uno de los pasos anteriores se comprueba que la operación se ha realizado correctamente antes de pasar al paso siguiente y se muestra una descripción del error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="98fa7-112">Each of the previous steps is checked for success before moving to the next step, and a failure description is displayed if an error occurs.</span></span> <span data-ttu-id="98fa7-113">La aplicación finalizará inmediatamente después de mostrar el mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="98fa7-113">The application will terminate immediately after displaying the error message.</span></span>

<span data-ttu-id="98fa7-114">Tenga en cuenta que la manipulación del archivo de texto se ha elegido solo para facilitar la demostración y se puede reemplazar por cualquier procedimiento de manipulación de datos deseado requerido.</span><span class="sxs-lookup"><span data-stu-id="98fa7-114">Note that text file manipulation was chosen for ease of demonstration only and can be replaced with any desired data manipulation procedure required.</span></span> <span data-ttu-id="98fa7-115">El archivo de datos puede tener cualquier tipo de datos, no solo texto.</span><span class="sxs-lookup"><span data-stu-id="98fa7-115">The data file can be of any data type, not only text.</span></span>

<span data-ttu-id="98fa7-116">La función [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) recupera una cadena de ruta de acceso completa de una variable de entorno, pero no comprueba de antemano la existencia de la ruta de acceso o los derechos de acceso adecuados a esa ruta de acceso, que es responsabilidad del desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98fa7-116">The [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) function retrieves a fully qualified path string from an environment variable but does not check in advance for the existence of the path or adequate access rights to that path, which is the responsibility of the application developer.</span></span> <span data-ttu-id="98fa7-117">Para obtener más información, vea [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha).</span><span class="sxs-lookup"><span data-stu-id="98fa7-117">For more information, see [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha).</span></span> <span data-ttu-id="98fa7-118">En el ejemplo siguiente, se considera un error como una condición de terminal y la aplicación se cierra después de enviar un mensaje descriptivo a la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="98fa7-118">In the following example, an error is regarded as a terminal condition and the application exits after sending a descriptive message to standard output.</span></span> <span data-ttu-id="98fa7-119">Sin embargo, existen muchas otras opciones, como pedir al usuario un directorio temporal o simplemente intentar usar el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="98fa7-119">However, many other options exist, such as prompting the user for a temporary directory or simply attempting to use the current directory.</span></span>

> [!Note]  
> <span data-ttu-id="98fa7-120">La función [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) no requiere que se use la función [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) .</span><span class="sxs-lookup"><span data-stu-id="98fa7-120">The [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) function does not require that the [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) function be used.</span></span>

 

<span data-ttu-id="98fa7-121">En el siguiente ejemplo de C++ se muestra cómo crear un archivo temporal para la manipulación de datos.</span><span class="sxs-lookup"><span data-stu-id="98fa7-121">The following C++ example shows how to create a temporary file for data manipulation purposes.</span></span>


```C++
//
//  This application opens a file specified by the user and uses
//  a temporary file to convert the file to upper case letters.
//  Note that the given source file is assumed to be an ASCII text file
//  and the new file created is overwritten each time the application is
//  run.
//

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 1024

void PrintError(LPCTSTR errDesc);

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile     = INVALID_HANDLE_VALUE;
    HANDLE hTempFile = INVALID_HANDLE_VALUE; 

    BOOL fSuccess  = FALSE;
    DWORD dwRetVal = 0;
    UINT uRetVal   = 0;

    DWORD dwBytesRead    = 0;
    DWORD dwBytesWritten = 0; 

    TCHAR szTempFileName[MAX_PATH];  
    TCHAR lpTempPathBuffer[MAX_PATH];
    char  chBuffer[BUFSIZE]; 

    LPCTSTR errMsg;

    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <file>\n"), argv[0]);
        return -1;
    }

    //  Opens the existing file. 
    hFile = CreateFile(argv[1],               // file name 
                       GENERIC_READ,          // open for reading 
                       0,                     // do not share 
                       NULL,                  // default security 
                       OPEN_EXISTING,         // existing file only 
                       FILE_ATTRIBUTE_NORMAL, // normal file 
                       NULL);                 // no template 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("First CreateFile failed"));
        return (1);
    } 

     //  Gets the temp path env string (no guarantee it's a valid path).
    dwRetVal = GetTempPath(MAX_PATH,          // length of the buffer
                           lpTempPathBuffer); // buffer for path 
    if (dwRetVal > MAX_PATH || (dwRetVal == 0))
    {
        PrintError(TEXT("GetTempPath failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (2);
    }

    //  Generates a temporary file name. 
    uRetVal = GetTempFileName(lpTempPathBuffer, // directory for tmp files
                              TEXT("DEMO"),     // temp file name prefix 
                              0,                // create unique name 
                              szTempFileName);  // buffer for name 
    if (uRetVal == 0)
    {
        PrintError(TEXT("GetTempFileName failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (3);
    }

    //  Creates the new file to write to for the upper-case version.
    hTempFile = CreateFile((LPTSTR) szTempFileName, // file name 
                           GENERIC_WRITE,        // open for write 
                           0,                    // do not share 
                           NULL,                 // default security 
                           CREATE_ALWAYS,        // overwrite existing
                           FILE_ATTRIBUTE_NORMAL,// normal file 
                           NULL);                // no template 
    if (hTempFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("Second CreateFile failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (4);
    } 

    //  Reads BUFSIZE blocks to the buffer and converts all characters in 
    //  the buffer to upper case, then writes the buffer to the temporary 
    //  file. 
    do 
    {
        if (ReadFile(hFile, chBuffer, BUFSIZE, &dwBytesRead, NULL)) 
        {
            //  Replaces lower case letters with upper case
            //  in place (using the same buffer). The return
            //  value is the number of replacements performed,
            //  which we aren't interested in for this demo.
            CharUpperBuffA(chBuffer, dwBytesRead); 

            fSuccess = WriteFile(hTempFile, 
                                 chBuffer, 
                                 dwBytesRead,
                                 &dwBytesWritten, 
                                 NULL); 
            if (!fSuccess) 
            {
                PrintError(TEXT("WriteFile failed"));
                return (5);
            }
        } 
        else
        {
            PrintError(TEXT("ReadFile failed"));
            return (6);
        }
    //  Continues until the whole file is processed.
    } while (dwBytesRead == BUFSIZE); 

    //  The handles to the files are no longer needed, so
    //  they are closed prior to moving the new file.
    if (!CloseHandle(hFile)) 
    {
       PrintError(TEXT("CloseHandle(hFile) failed"));
       return (7);
    }
    
    if (!CloseHandle(hTempFile)) 
    {
       PrintError(TEXT("CloseHandle(hTempFile) failed"));
       return (8);
    }

    //  Moves the temporary file to the new text file, allowing for differnt
    //  drive letters or volume names.
    fSuccess = MoveFileEx(szTempFileName, 
                          TEXT("AllCaps.txt"), 
                          MOVEFILE_REPLACE_EXISTING | MOVEFILE_COPY_ALLOWED);
    if (!fSuccess)
    { 
        PrintError(TEXT("MoveFileEx failed"));
        return (9);
    }
    else 
        _tprintf(TEXT("All-caps version of %s written to AllCaps.txt\n"), argv[1]);
    return (0);
}

//  ErrorMessage support function.
//  Retrieves the system error message for the GetLastError() code.
//  Note: caller must use LocalFree() on the returned LPCTSTR buffer.
LPCTSTR ErrorMessage(DWORD error) 
{ 
    LPVOID lpMsgBuf;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER 
                   | FORMAT_MESSAGE_FROM_SYSTEM 
                   | FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL,
                  error,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR) &lpMsgBuf,
                  0,
                  NULL);

    return((LPCTSTR)lpMsgBuf);
}

//  PrintError support function.
//  Simple wrapper function for error output.
void PrintError(LPCTSTR errDesc)
{
        LPCTSTR errMsg = ErrorMessage(GetLastError());
        _tprintf(TEXT("\n** ERROR ** %s: %s\n"), errDesc, errMsg);
        LocalFree((LPVOID)errMsg);
}
```



 

 
