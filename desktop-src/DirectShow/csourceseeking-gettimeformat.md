---
description: 'El método GetTimeFormat recupera el formato de hora actual. Este método implementa el método IMediaSeeking:: GetTimeFormat.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Método CSourceSeeking. GetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660778"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="3c8af-104">CSourceSeeking. GetTimeFormat, método</span><span class="sxs-lookup"><span data-stu-id="3c8af-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="3c8af-105">El `GetTimeFormat` método recupera el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="3c8af-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="3c8af-106">Este método implementa el método [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="3c8af-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8af-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c8af-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3c8af-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c8af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8af-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="3c8af-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8af-110">Puntero a una variable que recibe un GUID con formato de hora.</span><span class="sxs-lookup"><span data-stu-id="3c8af-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="3c8af-111">Consulte [**GUID de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3c8af-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c8af-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c8af-112">Return value</span></span>

<span data-ttu-id="3c8af-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3c8af-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="3c8af-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3c8af-114">Return code</span></span>                                                                               | <span data-ttu-id="3c8af-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c8af-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="3c8af-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3c8af-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3c8af-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="3c8af-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="3c8af-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3c8af-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3c8af-119">Valor de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="3c8af-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c8af-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c8af-120">Remarks</span></span>

<span data-ttu-id="3c8af-121">El único formato de hora admitido por la clase base es el \_ formato \_ de hora \_ tiempo medio (100-nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="3c8af-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8af-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c8af-122">Requirements</span></span>



| <span data-ttu-id="3c8af-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c8af-123">Requirement</span></span> | <span data-ttu-id="3c8af-124">Value</span><span class="sxs-lookup"><span data-stu-id="3c8af-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8af-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c8af-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3c8af-126"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c8af-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c8af-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c8af-127">Library</span></span><br/> | <dl> <span data-ttu-id="3c8af-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3c8af-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c8af-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c8af-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8af-130">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="3c8af-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




