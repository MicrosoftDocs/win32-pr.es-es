---
title: Función de devolución de llamada TranslateDispatch
description: Usado por el cliente de la función DoReaderMode para interceptar y controlar explícitamente los mensajes de Windows destinados al área de desplazamiento de la ventana del modo de lector. Se trata de una función de devolución de llamada definida por la aplicación.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Función de devolución de llamada TranslateDispatch Windows Controles
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08f726c3f56579260e96a882f1123d035df37cb3f7f71fd0ecbc47d41672359c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060535"
---
# <a name="translatedispatch-callback-function"></a>Función de devolución de llamada TranslateDispatch

\[*TranslateDispatch* está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Usado por el cliente de la función [**DoReaderMode**](doreadermode.md) para interceptar y controlar explícitamente los mensajes de Windows destinados al área de desplazamiento de la ventana del modo de lector. Se trata de una función de devolución de llamada definida por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpmsg* \[ En\]
</dt> <dd>

Tipo: **const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \***

Puntero a una [**estructura MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje interceptado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** si esta función controló el mensaje; de lo contrario, **FALSE**. Si **es FALSE**, el mensaje se controla mediante la implementación predeterminada del modo de lector. Esa implementación controla el movimiento del mouse y los botones, así como las pulsaciones de tecla.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se describe una implementación de esta función.


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, solo Windows \[ aplicaciones de escritorio de Vista\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>          |



 

