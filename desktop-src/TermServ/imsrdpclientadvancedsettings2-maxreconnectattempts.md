---
title: Propiedad MaxReconnectAttempts de IMsRdpClientAdvancedSettings2
description: Especifica el número de veces que se intentará volver a conectar durante la reconexión automática.
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad MaxReconnectAttempts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322796a2d6ca6a13476dad58af8c385b8bdfa1fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686070"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a>IMsRdpClientAdvancedSettings2:: MaxReconnectAttempts (propiedad)

Especifica el número de veces que se intentará volver a conectar durante la reconexión automática.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a>Valor de propiedad

El nuevo número de reintentos. Los valores válidos son de 0 a 200, ambos incluidos.

## <a name="error-codes"></a>Códigos de error

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

No se puede establecer esta propiedad cuando el control está conectado.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 se define como 9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





