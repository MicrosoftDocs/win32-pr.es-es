---
title: PSM_GETRESULT mensaje (Prsht.h)
description: Usado por hojas de propiedades modeless para recuperar la información devuelta a las hojas de propiedades modales por PropertySheet. Puede enviar este mensaje explícitamente o usar la \_ macro PropSheet GetResult.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT controles de Windows mensaje
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acc8fed8cdaa1f4282c3ed066ad44f68221330fa9e79b0719db8bba1bca37f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169811"
---
# <a name="psm_getresult-message"></a>Mensaje \_ GETRESULT de PSM

Usado por hojas de propiedades modeless para recuperar la información devuelta a las hojas de propiedades modales [**por PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Puede enviar este mensaje explícitamente o usar la macro [**\_ PropSheet GetResult.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor positivo si se realiza correctamente o -1 en caso contrario. Los siguientes valores devueltos tienen un significado especial.



| Código devuelto                                                                                         | Descripción                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Una página envió un [**mensaje PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) a la hoja de propiedades. El equipo debe reiniciarse para que los cambios del usuario suban efecto.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Una página envió un [**mensaje \_ DE PSM RESTARTWINDOWS**](psm-restartwindows.md) a la hoja de propiedades. Windows debe reiniciarse para que los cambios del usuario suban efecto.<br/>  |



 

## <a name="remarks"></a>Comentarios

Para recuperar información de error extendida, llame [**a GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

El valor devuelto para este mensaje es idéntico al que [**propertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) devuelve para una hoja de propiedades modal.

[Versión 5.80.](common-control-versions.md) El [**valor devuelto PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) contiene información diferente para las hojas de propiedades modales y modeless. En algunos casos, las hojas de propiedades no modales pueden necesitar la información que habrían recibido de **PropertySheet** si hubieran sido modales. En concreto, es posible que deban saber si se habría devuelto el \_ id. PSREBOOTSYSTEM o el identificador \_ PSRESTARTWINDOWS.

Para una hoja de propiedades modeless, el bucle de mensajes debe usar [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) para pasar mensajes al cuadro de diálogo de hoja de propiedades y [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) para determinar cuándo destruir el cuadro de diálogo. Cuando el usuario hace clic en el **botón Aceptar** o **Cancelar,** **PSM \_ GETCURRENTPAGEHWND** devuelve **NULL.** A continuación, puede recuperar el valor que una hoja de propiedades modal habría recibido de [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) mediante el envío de un **mensaje \_ GETRESULT de PSM.**

> [!Note]  
> Este mensaje no se admite cuando se usa el estilo del asistente de Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

