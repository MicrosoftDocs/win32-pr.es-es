---
description: 'Método IShellDispatch2.ServiceStart: inicia un servicio con nombre.'
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: Método IShellDispatch2.ServiceStart (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f48d13e593898b7b4f91fc9246745b183b928ffaa0a799100990a327a3f670ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090345"
---
# <a name="ishelldispatch2servicestart-method"></a>Método IShellDispatch2.ServiceStart

Inicia un servicio con nombre.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sServiceName* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene el nombre del servicio.

</dd> <dt>

*vPersistent* \[ En\]
</dt> <dd>

Tipo: **Variant**

Establezca en **true para** que el administrador de control de servicios inicie automáticamente el servicio durante el inicio del sistema. Establezca en **false** para dejar la configuración del servicio sin cambios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* Variant**

Devuelve **true si** se realiza correctamente; de lo contrario, **false**.

### <a name="vb"></a>VB

Tipo: **\* Variant**

Devuelve **true si** se realiza correctamente; de lo contrario, **false**.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.ServiceStart.**](./shell-servicestart.md)

El método devuelve **false** si el servicio ya se ha iniciado. Antes de llamar a este método, puede llamar a [**Shell.IsServiceRunning**](./shell-isservicerunning.md) para determinar el estado del servicio.

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **ServiceStart** para iniciar el servicio Messenger. El uso se muestra para JScript y VBScript.

JScript:


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
