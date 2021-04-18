---
description: El método StreamTime recupera la hora de la secuencia actual.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Método CBaseFilter. StreamTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661099"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="87869-103">CBaseFilter. StreamTime, método</span><span class="sxs-lookup"><span data-stu-id="87869-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="87869-104">El método **StreamTime** recupera la hora de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="87869-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="87869-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87869-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="87869-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87869-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87869-107">*rtStream* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="87869-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="87869-108">Referencia a un objeto [**CRefTime**](creftime.md) que recibe la hora de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="87869-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87869-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87869-109">Return value</span></span>

<span data-ttu-id="87869-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87869-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="87869-111">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="87869-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="87869-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="87869-112">Return code</span></span>                                                                                      | <span data-ttu-id="87869-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="87869-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="87869-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="87869-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="87869-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="87869-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="87869-116"><dt>**VFW \_ E \_ sin \_ reloj**</dt></span><span class="sxs-lookup"><span data-stu-id="87869-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="87869-117">No hay ningún reloj de referencia disponible.</span><span class="sxs-lookup"><span data-stu-id="87869-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87869-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87869-118">Remarks</span></span>

<span data-ttu-id="87869-119">La hora de la secuencia se define como la hora de referencia actual (indicada por el reloj de referencia) menos la hora de inicio (especificada por [**CBaseFilter:: m \_ tStart**](cbasefilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="87869-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="87869-120">La *marca de tiempo* de un ejemplo multimedia especifica el tiempo de flujo en el que se debe representar.</span><span class="sxs-lookup"><span data-stu-id="87869-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="87869-121">Si aún no se ha representado una muestra con una marca de tiempo menor que la hora actual de la secuencia, se retrasa.</span><span class="sxs-lookup"><span data-stu-id="87869-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="87869-122">Este método obtiene el tiempo de flujo llamando a [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obtener el tiempo de referencia actual y restar la hora de inicio inicial.</span><span class="sxs-lookup"><span data-stu-id="87869-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="87869-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87869-123">Requirements</span></span>



| <span data-ttu-id="87869-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="87869-124">Requirement</span></span> | <span data-ttu-id="87869-125">Value</span><span class="sxs-lookup"><span data-stu-id="87869-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87869-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87869-126">Header</span></span><br/>  | <dl> <span data-ttu-id="87869-127"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87869-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87869-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87869-128">Library</span></span><br/> | <dl> <span data-ttu-id="87869-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="87869-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87869-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="87869-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87869-131">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="87869-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="87869-132">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="87869-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




