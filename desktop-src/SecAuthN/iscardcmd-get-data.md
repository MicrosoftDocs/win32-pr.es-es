---
description: Recupera el campo de datos de la unidad de datos de protocolo de aplicación (APDU), colocándolo en un objeto de búfer de bytes.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'Método ISCardCmd:: get_Data (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546987"
---
# <a name="iscardcmdget_data-method"></a>ISCardCmd:: get \_ Data (método)

\[El método **obtener \_ datos** está disponible para su uso en los sistemas operativos especificados en la sección requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Get \_ Data** recupera el campo de datos de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU), colocándolo en un objeto de búfer de bytes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppData* \[ enuncia\]
</dt> <dd>

Puntero al objeto de búfer de bytes (**IStream**) que contiene el campo de datos APDU en la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *ppData* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *ppData*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                        |



 

## <a name="remarks"></a>Observaciones

Para establecer el campo de datos de APDU, llame a [**Put \_ Data**](iscardcmd-put-data.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar el campo de datos de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU). En el ejemplo se da por supuesto que pIByteData es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



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
| IID<br/>                      | IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**colocar \_ datos**](iscardcmd-put-data.md)
</dt> </dl>

 

 
