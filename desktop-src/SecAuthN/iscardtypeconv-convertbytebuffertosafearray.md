---
description: Convierte un búfer universal de bytes (objeto IStream) en un SAFEARRAY de char sin signo (byte).
ms.assetid: b8d052e8-2f36-42cf-b88c-ace215a2fc68
title: 'ISCardTypeConv:: ConvertByteBufferToSafeArray (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb6f646df60ab505c41c45bea34fd2d59aa3bb4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814734"
---
# <a name="iscardtypeconvconvertbytebuffertosafearray-method"></a>ISCardTypeConv:: ConvertByteBufferToSafeArray (método)

\[El método **ConvertByteBufferToSafeArray** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ConvertByteBufferToSafeArray** convierte un búfer universal de bytes (objeto **IStream** ) en un SafeArray de char sin signo (byte).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertByteBufferToSafeArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPSAFEARRAY  *ppbyArray
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbyBuffer* \[ de\]
</dt> <dd>

Puntero al objeto **IStream** que se va a convertir.

</dd> <dt>

*ppbyArray* \[ enuncia\]
</dt> <dd>

Puntero a la matriz SAFEARRAY que se va a devolver.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Memoria asignada correctamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Hay un problema con uno o varios de los parámetros pasados a la función.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Un parámetro de tipo de puntero era incorrecto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria libre para satisfacer la solicitud.<br/>                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores devueltos de tarjeta inteligente](authentication-return-values.md)
</dt> </dl>

 

 
