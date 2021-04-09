---
description: Devuelve la cadena de identificador disponible en los metadatos del volumen.
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Método GetIdentificationField de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154064"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a>Método GetIdentificationField de la \_ clase EncryptableVolume de Win32

El método **GetIdentificationField** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) devuelve la cadena de identificador disponible en los metadatos del volumen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IdentificationField* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Cadena que especifica el campo de identificación que se asigna al volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/>                                                                           |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Esta unidad está bloqueada por Cifrado de unidad BitLocker. Debe desbloquear este volumen en el panel de control. <br/> |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




