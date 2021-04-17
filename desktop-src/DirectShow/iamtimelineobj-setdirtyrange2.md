---
description: Sin implementar.
ms.assetid: 14ff2979-134f-45e4-98e1-1a119e1ffee2
title: 'IAMTimelineObj:: SetDirtyRange2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7ce2511a4b94f656197cef1bcb2c3cdfb4b4df61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680729"
---
# <a name="iamtimelineobjsetdirtyrange2-method"></a><span data-ttu-id="720b7-103">IAMTimelineObj:: SetDirtyRange2 (método)</span><span class="sxs-lookup"><span data-stu-id="720b7-103">IAMTimelineObj::SetDirtyRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="720b7-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="720b7-104">\[Deprecated.</span></span> <span data-ttu-id="720b7-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="720b7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="720b7-106">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="720b7-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="720b7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="720b7-107">Syntax</span></span>


```C++
HRESULT SetDirtyRange2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="720b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="720b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="720b7-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="720b7-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="720b7-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="720b7-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="720b7-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="720b7-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="720b7-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="720b7-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="720b7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="720b7-113">Return value</span></span>

<span data-ttu-id="720b7-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="720b7-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="720b7-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="720b7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="720b7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="720b7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="720b7-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="720b7-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="720b7-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="720b7-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="720b7-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="720b7-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="720b7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="720b7-120">Requirements</span></span>



| <span data-ttu-id="720b7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="720b7-121">Requirement</span></span> | <span data-ttu-id="720b7-122">Value</span><span class="sxs-lookup"><span data-stu-id="720b7-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="720b7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="720b7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="720b7-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="720b7-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="720b7-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="720b7-125">Library</span></span><br/> | <dl> <span data-ttu-id="720b7-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="720b7-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="720b7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="720b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="720b7-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="720b7-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




