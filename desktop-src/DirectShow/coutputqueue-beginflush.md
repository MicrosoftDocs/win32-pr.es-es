---
description: 'Método COutputQueue.BeginFlush: el método BeginFlush comienza una operación de vaciado.'
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Método COutputQueue.BeginFlush (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7b002c03ee0bfb95733ac9af0f6e88444cc6a42bec2af7d9a40a307d83d2fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909655"
---
# <a name="coutputqueuebeginflush-method"></a>Método COutputQueue.BeginFlush

El `BeginFlush` método comienza una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
void BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método establece la variable [**miembro COutputQueue::m \_ bFlushing**](coutputqueue-m-bflushing.md) en **TRUE.** Si el objeto usa un subproceso, el subproceso llama al método [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) para liberar los ejemplos pendientes. De lo contrario, el objeto **llama a FreeSamples** durante [**el método COutputQueue::EndFlush.**](coutputqueue-endflush.md) Este método también establece la variable [**miembro COutputQueue::m \_ hr**](coutputqueue-m-hr.md) en S FALSE, lo que hace que el objeto descarte \_ todos los ejemplos nuevos.

El objeto pasa la notificación de vaciado de bajada llamando al [**método IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




