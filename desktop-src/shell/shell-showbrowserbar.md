---
description: 'Método Shell.ShowBrowserBar: muestra una barra del explorador.'
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Método Shell.ShowBrowserBar (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 21bafde8c148ea8249672dd26a244dec152ed0e9fc5ce5fbb769e5cae6c92b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008895"
---
# <a name="shellshowbrowserbar-method"></a>Método Shell.ShowBrowserBar

Muestra una barra del explorador.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sCLSID* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene la forma de cadena del CLSID de la barra del explorador que se va a mostrar. El objeto debe registrarse como un objeto Barra del explorador con una categoría de \_ componente InfoBand CATID. Para obtener más información, vea [Crear barras personalizadas del Explorador, bandas](band-objects.md)de herramientas y bandas de escritorio.

</dd> <dt>

*vShow* \[ En\]
</dt> <dd>

Tipo: **Variant**

Establezca en **true** para mostrar la barra del explorador o **false** para ocultarla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="jscript"></a>JScript

Tipo: **\* Variant**

Devuelve **true si** se realiza correctamente; de lo contrario, **false**.

### <a name="vb"></a>VB

Tipo: **\* Variant**

Devuelve **true si** se realiza correctamente; de lo contrario, **false**.

## <a name="remarks"></a>Comentarios

Puede mostrar una de las barras estándar del Explorador estableciendo el parámetro *sCLSID* en el CLSID de esa barra del explorador. Las barras estándar del explorador y sus cadenas CLSID son las siguientes:



| Barra del explorador | Cadena CLSID                           |
|--------------|----------------------------------------|
| Favoritos    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Carpetas      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Historial      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Search       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso de **Shell.ShowBrowserBar para** mostrar la **barra del explorador Favoritos.** El uso se muestra para JScript y VBScript.

JScript:


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
