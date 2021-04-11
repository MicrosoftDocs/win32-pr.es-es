---
description: La función EndPagePrinter notifica al administrador de trabajos de impresión que la aplicación está al final de una página en un trabajo de impresión.
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: Función EndPagePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 45e8ce005953e07f10ec621660ed38e68d50c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156444"
---
# <a name="endpageprinter-function"></a><span data-ttu-id="4a98c-103">EndPagePrinter función)</span><span class="sxs-lookup"><span data-stu-id="4a98c-103">EndPagePrinter function</span></span>

<span data-ttu-id="4a98c-104">La función **EndPagePrinter** notifica al administrador de trabajos de impresión que la aplicación está al final de una página en un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="4a98c-104">The **EndPagePrinter** function notifies the print spooler that the application is at the end of a page in a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a98c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a98c-105">Syntax</span></span>


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="4a98c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a98c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a98c-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4a98c-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a98c-108">Identificador de la impresora para la que se va a concluir la página.</span><span class="sxs-lookup"><span data-stu-id="4a98c-108">Handle to the printer for which the page will be concluded.</span></span> <span data-ttu-id="4a98c-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="4a98c-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a98c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a98c-110">Return value</span></span>

<span data-ttu-id="4a98c-111">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4a98c-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4a98c-112">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="4a98c-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a98c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a98c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a98c-114">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="4a98c-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4a98c-115">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4a98c-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4a98c-116">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="4a98c-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4a98c-117">La secuencia de un trabajo de impresión es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="4a98c-117">The sequence for a print job is as follows:</span></span>

1.  <span data-ttu-id="4a98c-118">Para iniciar un trabajo de impresión, llame a [**StartDocPrinter**](startdocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4a98c-118">To begin a print job, call [**StartDocPrinter**](startdocprinter.md).</span></span>
2.  <span data-ttu-id="4a98c-119">Para comenzar cada página, llame a [**StartPagePrinter**](startpageprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4a98c-119">To begin each page, call [**StartPagePrinter**](startpageprinter.md).</span></span>
3.  <span data-ttu-id="4a98c-120">Para escribir datos en una página, llame a [**WritePrinter**](writeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4a98c-120">To write data to a page, call [**WritePrinter**](writeprinter.md).</span></span>
4.  <span data-ttu-id="4a98c-121">Para finalizar cada página, llame a **EndPagePrinter**.</span><span class="sxs-lookup"><span data-stu-id="4a98c-121">To end each page, call **EndPagePrinter**.</span></span>
5.  <span data-ttu-id="4a98c-122">Repita 2, 3 y 4 para tantas páginas como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4a98c-122">Repeat 2, 3, and 4 for as many pages as necessary.</span></span>
6.  <span data-ttu-id="4a98c-123">Para finalizar el trabajo de impresión, llame a [**EndDocPrinter**](enddocprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4a98c-123">To end the print job, call [**EndDocPrinter**](enddocprinter.md).</span></span>

<span data-ttu-id="4a98c-124">Cuando una página de un archivo en cola supera aproximadamente 350 MB, puede no imprimirse y no enviar un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="4a98c-124">When a page in a spooled file exceeds approximately 350 MB, it can fail to print and not send an error message.</span></span> <span data-ttu-id="4a98c-125">Por ejemplo, esto puede ocurrir cuando se imprimen archivos EMF de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="4a98c-125">For example, this can occur when printing large EMF files.</span></span> <span data-ttu-id="4a98c-126">El límite de tamaño de página depende de muchos factores, como la cantidad de memoria virtual disponible, la cantidad de memoria asignada mediante la llamada a procesos y la cantidad de fragmentación en el montón del proceso.</span><span class="sxs-lookup"><span data-stu-id="4a98c-126">The page size limit depends on many factors including the amount of virtual memory available, the amount of memory allocated by calling processes, and the amount of fragmentation in the process heap.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a98c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a98c-127">Requirements</span></span>



| <span data-ttu-id="4a98c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a98c-128">Requirement</span></span> | <span data-ttu-id="4a98c-129">Value</span><span class="sxs-lookup"><span data-stu-id="4a98c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a98c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a98c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4a98c-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4a98c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4a98c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a98c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4a98c-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4a98c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4a98c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a98c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a98c-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a98c-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4a98c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a98c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a98c-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a98c-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4a98c-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a98c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a98c-139"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a98c-139"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="4a98c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a98c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a98c-141">Impresión</span><span class="sxs-lookup"><span data-stu-id="4a98c-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4a98c-142">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="4a98c-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4a98c-143">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="4a98c-143">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="4a98c-144">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="4a98c-144">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="4a98c-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4a98c-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="4a98c-146">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="4a98c-146">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="4a98c-147">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="4a98c-147">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="4a98c-148">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="4a98c-148">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




