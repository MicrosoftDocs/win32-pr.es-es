---
description: Método de destructor.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: CBaseAllocator. ~ CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660117"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="a5dca-103">CBaseAllocator. ~ CBaseAllocator (destructor)</span><span class="sxs-lookup"><span data-stu-id="a5dca-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="a5dca-104">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="a5dca-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5dca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5dca-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="a5dca-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5dca-106">Remarks</span></span>

<span data-ttu-id="a5dca-107">Llame siempre al método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) antes de destruir el objeto.</span><span class="sxs-lookup"><span data-stu-id="a5dca-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="a5dca-108">El destructor de clase base no puede llamar a **commit**, porque ese método llama al método virtual puro [**CBaseAllocator:: Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="a5dca-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="a5dca-109">Las clases derivadas deben invalidar este destructor y llamar a **commit**.</span><span class="sxs-lookup"><span data-stu-id="a5dca-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5dca-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5dca-110">Requirements</span></span>



| <span data-ttu-id="a5dca-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5dca-111">Requirement</span></span> | <span data-ttu-id="a5dca-112">Value</span><span class="sxs-lookup"><span data-stu-id="a5dca-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5dca-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5dca-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a5dca-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5dca-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a5dca-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5dca-115">Library</span></span><br/> | <dl> <span data-ttu-id="a5dca-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a5dca-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5dca-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5dca-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5dca-118">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="a5dca-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




