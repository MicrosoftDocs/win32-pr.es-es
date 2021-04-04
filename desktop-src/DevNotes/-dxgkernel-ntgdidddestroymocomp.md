---
description: Notifica al controlador que este objeto de compensación de movimiento ya no se usará. Ahora, el controlador debe realizar cualquier limpieza necesaria.
ms.assetid: 1d86a564-efe1-4971-99ec-2c9a6aa59c89
title: Función NtGdiDdDestroyMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: b7bc5915fe43bd4d48495b2b1beda8ee38f05fe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907123"
---
# <a name="ntgdidddestroymocomp-function"></a>NtGdiDdDestroyMoComp función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Notifica al controlador que este objeto de compensación de movimiento ya no se usará. Ahora, el controlador debe realizar cualquier limpieza necesaria.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdDestroyMoComp(
  _In_    HANDLE                hMoComp,
  _Inout_ PDD_DESTROYMOCOMPDATA puBeginFrameData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMoComp* \[ de\]
</dt> <dd>

Identificador de una [**estructura \_ \_ local DD MOTIONCOMP**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contiene una descripción del objeto de compensación de movimiento que se va a destruir.

</dd> <dt>

*puBeginFrameData* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**DD \_ DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) que contiene la información necesaria para finalizar la compensación de movimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdDestroyMoComp** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_controlador DDHAL \_ controlado**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función. De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED del controlador DDHAL \_**</dt> </dl> | El controlador no tiene ningún comentario en la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.<br/> |



 

## <a name="remarks"></a>Observaciones

Para obtener más información, vea el kit de desarrollo de controladores (DDK) de Microsoft DirectX video Acceleration.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de nivel inferior de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
