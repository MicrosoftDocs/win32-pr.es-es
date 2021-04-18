---
title: Método WSMan. SessionFlagUseCredSsp (WSManDisp. h)
description: Devuelve el valor de la marca de autenticación WSManFlagUseCredSsp para su uso en el parámetro flags del método WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Método SessionFlagUseCredSsp Administración remota de Windows
- Administración remota de Windows método SessionFlagUseCredSsp, objeto WSMan
- Administración remota de Windows de objeto WSMan, método SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490756"
---
# <a name="wsmansessionflagusecredssp-method"></a>WSMan. SessionFlagUseCredSsp (método)

Devuelve el valor de la marca de autenticación **WSManFlagUseCredSsp** para su uso en el parámetro *Flags* del método [**WSMan. createSession**](wsman-createsession.md) . Este método proporciona una sintaxis más eficaz para usar la constante, de modo que los scripts no sean necesarios para establecer un valor constante. Para obtener más información sobre cómo llamar a este método, vea [constantes de sesión](session-constants.md).

**WSManFlagUseCredSsp** es una constante de la enumeración **\_ \_ WSManSessionFlags** . Para obtener más información, consulte [constantes de autenticación](authentication-constants.md).

## <a name="syntax"></a>Sintaxis


```VB
WSMan.SessionFlagUseCredSsp( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*marcas* \[ de enuncia\]
</dt> <dd>

Valor de la constante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Redistribuible<br/>          | Windows Management Framework en Windows Server 2008 con SP2, Windows Vista con SP1 y Windows Vista con SP2<br/> |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>                                      |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl>                                    |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl>                                    |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**De sesión**](session.md)
</dt> </dl>

 

 





