---
description: 'El método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin:: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Método CTransformInputPin. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680337"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="4a3e9-104">CTransformInputPin. EndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="4a3e9-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="4a3e9-105">El `EndOfStream` método notifica al pin que no se espera ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="4a3e9-106">Este método implementa el método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="4a3e9-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a3e9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a3e9-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="4a3e9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a3e9-108">Parameters</span></span>

<span data-ttu-id="4a3e9-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a3e9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a3e9-110">Return value</span></span>

<span data-ttu-id="4a3e9-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a3e9-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4a3e9-112">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="4a3e9-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4a3e9-113">Return code</span></span>                                                                                           | <span data-ttu-id="4a3e9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a3e9-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="4a3e9-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4a3e9-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="4a3e9-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="4a3e9-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4a3e9-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="4a3e9-118">El PIN se está vaciando actualmente.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="4a3e9-119"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="4a3e9-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="4a3e9-120">El PIN de salida no está conectado.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="4a3e9-121"><dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a3e9-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="4a3e9-122">Se produjo un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="4a3e9-123"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a3e9-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="4a3e9-124">El PIN está detenido.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="4a3e9-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a3e9-125">Remarks</span></span>

<span data-ttu-id="4a3e9-126">Este método llama al método [**CTransformFilter:: EndOfStream**](ctransformfilter-endofstream.md) del filtro para proporcionar la notificación de final de secuencia de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="4a3e9-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a3e9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a3e9-127">Requirements</span></span>



| <span data-ttu-id="4a3e9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a3e9-128">Requirement</span></span> | <span data-ttu-id="4a3e9-129">Value</span><span class="sxs-lookup"><span data-stu-id="4a3e9-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a3e9-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a3e9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4a3e9-131"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a3e9-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4a3e9-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a3e9-132">Library</span></span><br/> | <dl> <span data-ttu-id="4a3e9-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4a3e9-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




