---
description: Se envía a un procedimiento DLL de extensión del Administrador de archivos cuando el Administrador de archivos quiere una cadena de Ayuda para un elemento de comando de menú o barra de herramientas.
title: FMEVENT_HELPSTRING mensaje (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: 6fe187330e27f7e246c9bbd68005f68f346bbc90
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841286"
---
# <a name="fmevent_helpstring-message"></a>Mensaje \_ HELPSTRING de FMEVENT

Se envía a un procedimiento DLL de extensión del Administrador de archivos cuando el Administrador de archivos quiere una cadena de Ayuda para un elemento de comando de menú o barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lpfmshs* 
</dt> <dd>

Dirección de una estructura [**\_ HELPSTRING de FMS**](fms-helpstring.md) que comunica los datos de la cadena de ayuda del elemento de comando. La **estructura \_ HELPSTRING de FMS** identifica el elemento de comando para el que se desea una cadena de Ayuda, junto con un identificador para su menú. A continuación, una aplicación escribe la cadena de Ayuda adecuada en el miembro szHelp de la estructura **\_ HELPSTRING** **de FMS.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un procedimiento DLL de extensión debe devolver cero si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




