---
title: Propiedad Enumerator.AtEndOfStream (WSManDisp.h)
description: Obtiene un valor booleano que indica si hay más elementos en la colección.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Propiedad AtEndOfStream Windows administración remota
- Propiedad AtEndOfStream Windows administración remota , objeto enumerador
- Objeto enumerador Windows administración remota , propiedad AtEndOfStream
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1077837f82d650b57dfea0316ef15094b18749eefdb6957e62e6afd92cfe672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113206"
---
# <a name="enumeratoratendofstream-property"></a>Enumerator.AtEndOfStream, propiedad

Obtiene un valor booleano que indica si hay más elementos en la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a>Valor de propiedad

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**Verdad**


</dt> <dd>

No hay más elementos en la colección.

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**Falso**


</dt> <dd>

Hay más elementos disponibles.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si libera el objeto [**Enumerador**](enumerator.md) después de haber obtenido todos los datos necesarios, se quitan las solicitudes de enumeración pendientes. Para obtener más información, [vea Enumerar o enumerar todas las instancias de un recurso.](enumerating-or-listing-all-instances-of-a-resource.md)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de VBScript se enumeran las instancias del sistema operativo. Tenga en cuenta que la liberación del objeto de enumeración limpia las solicitudes de enumeración pendientes. La subrutina DisplayOutput da formato a la salida de datos de la misma manera que la herramienta WinRM.cmd.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
 Dim xmlFile, xslFile
 Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
 Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
 xmlFile.LoadXml( strWinRMXml )
 xslFile.Load( "WsmTxt.xsl" )
 Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Enumerador**](enumerator.md)
</dt> <dt>

[Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





