---
description: Valida el identificador de objeto (OID) de uso mejorado de clave (EKU) del certificado proporcionado.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Método ProtectKeyWithCertificateThumbprint de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e0b47aabccaacfb3ab81968b8a93037aad304f8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688014"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithCertificateThumbprint de la \_ clase EncryptableVolume de Win32

El método **ProtectKeyWithCertificateThumbprint** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) valida el [*identificador de objeto*](../secgloss/o-gly.md) (OID) de uso mejorado de clave (EKU) del certificado proporcionado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ en, opcional\]
</dt> <dd>

Tipo: **String**

Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave. Si no se especifica este parámetro, el parámetro *FriendlyName* se crea con el nombre de sujeto del certificado.

</dd> <dt>

*CertThumbprint* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena que especifica la huella digital del certificado.

</dd> <dt>

*VolumeKeyProtectorID* \[ enuncia\]
</dt> <dd>

Tipo: **String**

Una cadena que identifica de forma única el protector de clave creado que se puede usar para administrar este protector de clave.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                                           | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**Error \_ de \_Datos no válidos**</dt> <dt>(0xd)</dt> </dl>                                           | Los datos no son válidos.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ no \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | El atributo EKU del certificado especificado no permite su uso para Cifrado de unidad BitLocker. BitLocker no requiere que un certificado tenga un atributo EKU, pero si se configura uno, debe establecerse en un OID que coincida con el OID configurado para BitLocker.<br/> |
| <dl> <dt>**FVE \_ Certificado de usuario de directiva de E \_ \_ \_ \_ no \_ permitido**</dt> <dt>2150695026 (0x80310072)</dt> </dl> | Directiva de grupo no permite el uso de certificados de usuario, como tarjetas inteligentes, con BitLocker.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ El \_ certificado de usuario de directiva de E \_ \_ \_ debe \_ ser \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Directiva de grupo requiere que proporcione una tarjeta inteligente para usar BitLocker.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ La \_ Directiva E \_ prohíbe \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Directiva de grupo no permite el uso de certificados autofirmados.<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Observaciones

Si el OID no coincide con el que está asociado con el controlador de servicio en el registro, este método produce un error. Esto impide que el usuario configure los protectores del agente de recuperación de datos (DRA) manualmente en el volumen. Los Dra solo los establece el servicio.

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

 

 
