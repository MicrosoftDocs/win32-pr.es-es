---
title: Mensaje de WM_MENUCHAR (Winuser. h)
description: Se envía cuando un menú está activo y el usuario presiona una tecla que no se corresponde con ninguna tecla de método abreviado o tecla de aceleración. Este mensaje se envía a la ventana que posee el menú.
ms.assetid: de6c91bb-80fd-44b2-8d96-d016477a6547
keywords:
- WM_MENUCHAR menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a278e4a1b4333631741a6a542318a8a55e40b512
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804022"
---
# <a name="wm_menuchar-message"></a>Mensaje de MENUCHAR de WM \_

Se envía cuando un menú está activo y el usuario presiona una tecla que no se corresponde con ninguna tecla de método abreviado o tecla de aceleración. Este mensaje se envía a la ventana que posee el menú.


```C++
#define WM_MENUCHAR                     0x0120
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden inferior especifica el código de carácter correspondiente a la tecla que el usuario presionó.

La palabra de orden superior especifica el tipo de menú activo. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                 | Significado                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_**</dt> <dt>0x00000010L</dt> emergente </dl>       | Menú desplegable, submenú o menú contextual.<br/> |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl> | El menú ventana.<br/>                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del menú activo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación que procesa este mensaje debe devolver uno de los valores siguientes en la palabra de orden superior del valor devuelto.



| Código o valor devuelto                                                                                                                                  | Descripción                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNC \_ CERRAR**</dt> <dt>1</dt> </dl>   | Informa al sistema de que debe cerrar el menú activo.<br/>                                                                                                                      |
| <dl> <dt>**MNC \_ EJECUTAR**</dt> <dt>2</dt> </dl> | Informa al sistema de que debe elegir el elemento especificado en la palabra de orden inferior del valor devuelto. La ventana propietaria recibe un mensaje de [**\_ comando de WM**](wm-command.md) .<br/> |
| <dl> <dt>**MNC \_ OMITIr**</dt> <dt>0</dt> </dl>  | Informa al sistema de que debe descartar el carácter que el usuario presionó y crear un pitido corto en el altavoz del sistema.<br/>                                                       |
| <dl> <dt>**MNC \_ Seleccione**</dt> <dt>3</dt> </dl>  | Informa al sistema de que debe seleccionar el elemento especificado en la palabra de orden inferior del valor devuelto. <br/>                                                                       |



 

## <a name="remarks"></a>Observaciones

La palabra de orden inferior se omite si la palabra de orden superior contiene 0 o 1.

Una aplicación debe procesar este mensaje cuando se utiliza un acelerador para seleccionar un elemento de menú que muestra un mapa de bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Vista**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

