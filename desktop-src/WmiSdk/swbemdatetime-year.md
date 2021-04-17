---
description: Obtiene o establece un valor que representa el componente de año del valor de fecha y hora.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. Year (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706840"
---
# <a name="swbemdatetimeyear-property"></a><span data-ttu-id="eda25-103">Propiedad SWbemDateTime. Year</span><span class="sxs-lookup"><span data-stu-id="eda25-103">SWbemDateTime.Year property</span></span>

<span data-ttu-id="eda25-104">La propiedad **Year** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente de año del valor [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="eda25-104">The **Year** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the year component of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="eda25-105">El valor debe estar en el intervalo de 0000-9999 o se devuelve el error wbemErrValueOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="eda25-105">The value must be in the range of 0000 - 9999 or the error wbemErrValueOutOfRange is returned.</span></span>

<span data-ttu-id="eda25-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eda25-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="eda25-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="eda25-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eda25-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eda25-108">Syntax</span></span>


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a><span data-ttu-id="eda25-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eda25-109">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="eda25-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="eda25-110">Error codes</span></span>

<span data-ttu-id="eda25-111">Después de obtener o establecer la propiedad **Year** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="eda25-111">After you get or set the **Year** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="eda25-112">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="eda25-112">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="eda25-113">El valor no estaba comprendido en el intervalo de 0000 a 9999.</span><span class="sxs-lookup"><span data-stu-id="eda25-113">The value was not in the range of 0000 through 9999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="eda25-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="eda25-114">Examples</span></span>

<span data-ttu-id="eda25-115">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="eda25-115">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="eda25-116">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="eda25-116">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eda25-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eda25-117">Requirements</span></span>



| <span data-ttu-id="eda25-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eda25-118">Requirement</span></span> | <span data-ttu-id="eda25-119">Value</span><span class="sxs-lookup"><span data-stu-id="eda25-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eda25-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eda25-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eda25-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eda25-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eda25-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eda25-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eda25-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eda25-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eda25-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eda25-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eda25-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eda25-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eda25-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eda25-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="eda25-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eda25-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eda25-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eda25-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eda25-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eda25-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eda25-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="eda25-130">CLSID</span></span><br/>                    | <span data-ttu-id="eda25-131">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="eda25-131">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="eda25-132">IID</span><span class="sxs-lookup"><span data-stu-id="eda25-132">IID</span></span><br/>                      | <span data-ttu-id="eda25-133">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="eda25-133">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="eda25-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="eda25-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda25-135">**SWbemDateTime.YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="eda25-135">**SWbemDateTime.YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
</dt> <dt>

[<span data-ttu-id="eda25-136">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="eda25-136">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="eda25-137">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="eda25-137">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

