---
description: Pausa el cifrado o descifrado de un volumen.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Método PauseConversion de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688016"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>Método PauseConversion de la \_ clase EncryptableVolume de Win32

El método **PauseConversion** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) pausa el cifrado o descifrado de un volumen.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, esta función puede pausar una operación de eliminación, pero no puede pausar el cifrado basado en hardware.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.

Si este método se usa en un volumen totalmente cifrado o completamente descifrado, o si el cifrado o descifrado ya está pausado en el volumen, se devuelve 0 si no se produce ningún otro error.



| Código o valor devuelto                                                                                                                                                                  | Descripción                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                  | Método realizado correctamente.<br/> |
| <dl> <dt>**FVE \_ \_ \_ Volumen bloqueado de E**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | El volumen está bloqueado.<br/>      |



 

## <a name="remarks"></a>Observaciones

Si este método se usa en un volumen con cifrado o descifrado en curso, la ejecución correcta de este método hace que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que el cifrado o descifrado está en pausa.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop\]<br/>                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
