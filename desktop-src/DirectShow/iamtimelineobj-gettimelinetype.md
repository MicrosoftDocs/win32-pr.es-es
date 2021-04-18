---
description: El método GetTimelineType recupera el tipo del objeto.
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: 'IAMTimelineObj:: GetTimelineType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76b9c2a847cc0d0150b21062810290aaaab702cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689933"
---
# <a name="iamtimelineobjgettimelinetype-method"></a><span data-ttu-id="26780-103">IAMTimelineObj:: GetTimelineType (método)</span><span class="sxs-lookup"><span data-stu-id="26780-103">IAMTimelineObj::GetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="26780-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="26780-104">\[Deprecated.</span></span> <span data-ttu-id="26780-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="26780-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="26780-106">El `GetTimelineType` método recupera el tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="26780-106">The `GetTimelineType` method retrieves the object's type.</span></span>

## <a name="syntax"></a><span data-ttu-id="26780-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26780-107">Syntax</span></span>


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="26780-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26780-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26780-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="26780-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="26780-110">Recibe un miembro del tipo enumerado de [**\_ \_ tipo principal**](timeline-major-type.md) de la escala de tiempo, que indica el tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="26780-110">Receives a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, indicating the type of object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26780-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26780-111">Return value</span></span>

<span data-ttu-id="26780-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="26780-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26780-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26780-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26780-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26780-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26780-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="26780-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="26780-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="26780-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="26780-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="26780-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26780-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26780-118">Requirements</span></span>



| <span data-ttu-id="26780-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="26780-119">Requirement</span></span> | <span data-ttu-id="26780-120">Value</span><span class="sxs-lookup"><span data-stu-id="26780-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26780-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26780-121">Header</span></span><br/>  | <dl> <span data-ttu-id="26780-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="26780-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="26780-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26780-123">Library</span></span><br/> | <dl> <span data-ttu-id="26780-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26780-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26780-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="26780-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26780-126">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="26780-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="26780-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="26780-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




