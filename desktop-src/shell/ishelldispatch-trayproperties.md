---
description: 'Método IShellDispatch.TrayProperties: muestra la barra de tareas y el cuadro de diálogo Propiedades del menú Inicio . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar Propiedades.'
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Método IShellDispatch.TrayProperties (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 424d25d7555090e4244d5cd22084171ca2a4fea9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086623"
---
# <a name="ishelldispatchtrayproperties-method"></a>Método IShellDispatch.TrayProperties

Muestra el cuadro **de diálogo Propiedades de la barra de tareas y del menú** Inicio . Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Propiedades**.

## <a name="syntax"></a>Sintaxis


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Este método no devuelve ningún valor.

### <a name="vb"></a>VB

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método se implementa y se accede a través del [**método Shell.TrayProperties.**](shell-trayproperties.md)

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso **de TrayProperties** en JScript, VBScript y Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




