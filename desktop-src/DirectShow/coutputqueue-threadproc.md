---
description: El método ThreadProc recupera ejemplos de la cola y los entrega al pin de entrada.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Método COutputQueue. ThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670405"
---
# <a name="coutputqueuethreadproc-method"></a>COutputQueue. ThreadProc (método)

El `ThreadProc` método recupera ejemplos de la cola y los entrega al pin de entrada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="remarks"></a>Observaciones

El método [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md) llama a este método, que implementa el bucle de subproceso principal. Dentro del bucle, el método realiza los pasos siguientes:

1.  Recupera un ejemplo para la cola.
2.  Si el ejemplo es un mensaje de control, el subproceso ejecuta la acción de control. De lo contrario, coloca el ejemplo en la matriz [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) .
3.  Cuando la matriz está llena (o si [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) es **false**), el subproceso llama al método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) para proporcionar los ejemplos.
4.  Si no hay ningún ejemplo en cola, el subproceso espera en el semáforo [**COutputQueue:: m \_ hSem**](coutputqueue-m-hsem.md) .

El subproceso finaliza cuando la variable miembro [**COutputQueue:: m \_ BTerminate**](coutputqueue-m-bterminate.md) es **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




