---
description: Obtenga información sobre el método de constructor CMediaPosition. CMediaPosition (Ctlutil. h). Este método usa los parámetros ' pName ', ' pUnk ' y ' PHR '.
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Constructor CMediaPosition. CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105670269"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>Constructor CMediaPosition. CMediaPosition (Ctlutil. h): parámetros pName, pUnk, PHR

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre del objeto, para la depuración. Asigne este parámetro en la memoria estática.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto, o **null** si no se agrega el objeto.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** .

</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | Ctlutil. h (incluir streams. h) |
| Biblioteca| Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




