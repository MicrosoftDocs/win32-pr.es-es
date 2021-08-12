---
title: WM_PSD_FULLPAGERECT mensaje (Commdlg.h)
description: Notifica a un procedimiento de enlace PagePaintHook las coordenadas del rectángulo de página de ejemplo en el cuadro de diálogo Configuración de página . El cuadro de diálogo envía este mensaje cuando está a punto de dibujar el contenido de la página de ejemplo.
ms.assetid: 88ca1d60-3335-480a-b874-c6f248a3c23a
keywords:
- WM_PSD_FULLPAGERECT cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_PSD_FULLPAGERECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b3d49ca34775657fbb626823fe68632ad963abc29a99ff5aa99dce69753e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280375"
---
# <a name="wm_psd_fullpagerect-message"></a>Mensaje \_ \_ FULLPAGERECT de WM PSD

Notifica a un [*procedimiento de enlace PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) las coordenadas del rectángulo de página de ejemplo en el cuadro **de diálogo Configuración** de página . El cuadro de diálogo envía este mensaje cuando está a punto de dibujar el contenido de la página de ejemplo.


```C++
#define WM_USER                  0x0400
#define WM_PSD_FULLPAGERECT     (WM_USER+1)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo para la página de ejemplo.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que contiene las coordenadas, en píxeles, de la página de ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el procedimiento de enlace devuelve **TRUE**, el cuadro de diálogo no envía más mensajes y no dibuja en la página de ejemplo hasta la próxima vez que el sistema necesite volver a dibujar la página de ejemplo.

Si el procedimiento de enlace devuelve **FALSE**, el cuadro de diálogo envía los mensajes restantes de la secuencia de dibujo.

## <a name="remarks"></a>Comentarios

El **cuadro de diálogo Configuración** de página incluye una imagen de una página de ejemplo que muestra cómo afectan las selecciones del usuario a la apariencia de la salida impresa. Al llamar a la [**función PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) puede proporcionar un procedimiento de enlace [*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar la apariencia de la página de ejemplo. Cada vez que el cuadro de diálogo está a punto de dibujar el contenido de la página de ejemplo, el cuadro de diálogo envía una secuencia de mensajes al procedimiento de enlace.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Commdlg.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[*PagePaintHook*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
</dt> <dt>

[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))
</dt> <dt>

[**PÁGINA \_ DE PSD \_ DE WMSETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Biblioteca común de cuadros de diálogo](common-dialog-box-library.md)
</dt> </dl>

 

