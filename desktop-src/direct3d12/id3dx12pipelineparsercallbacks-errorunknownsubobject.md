---
title: Método ID3DX12PipelineParserCallbacks ErrorUnknownSubobject (D3DX12. h)
description: Llama a la devolución de llamada de error de subobjeto desconocido de un objeto que implementa esta interfaz.
ms.assetid: 612D7C44-4DC5-4DEA-B369-09C27123D45E
keywords:
- Método ErrorUnknownSubobject
- Método ErrorUnknownSubobject, interfaz ID3DX12PipelineParserCallbacks
- Interfaz ID3DX12PipelineParserCallbacks, método ErrorUnknownSubobject
topic_type:
- apiref
api_name:
- ID3DX12PipelineParserCallbacks.ErrorUnknownSubobject
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e294e3face085c5298f3cc624d7c0ef70dcf865
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718347"
---
# <a name="id3dx12pipelineparsercallbackserrorunknownsubobject-method"></a>ID3DX12PipelineParserCallbacks:: ErrorUnknownSubobject (método)

Llama a la devolución de llamada de error de subobjeto desconocido de un objeto que implementa esta interfaz.

## <a name="syntax"></a>Sintaxis


```C++
void ErrorUnknownSubobject(
   
        UINT
           UnknownTypeValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UnknownTypeValue* 
</dt> <dd>

Tipo: **uint**

Tipo de subobjeto no reconocido del subobjeto intentado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No devuelve nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces auxiliares de Direct3D 12](helper-interfaces-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





