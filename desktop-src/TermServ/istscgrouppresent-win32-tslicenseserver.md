---
title: Método IsTSCGroupPresent de la clase Win32_TSLicenseServer
description: IsTSCGroupPresent ya no está disponible para su uso a partir de Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Método IsTSCGroupPresent Servicios de Escritorio remoto
- Método IsTSCGroupPresent Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsTSCGroupPresent
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079149"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a>Método IsTSCGroupPresent de la \_ clase TSLicenseServer de Win32

\[**IsTSCGroupPresent** ya no está disponible para su uso a partir de Windows Server 2012.\]

No se admite este método.

**Windows server 2008 R2 y Windows server 2008:** Recupera si el grupo local de equipos Terminal Server existe en el servidor de licencias de Escritorio remoto.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Presente* \[ enuncia\]
</dt> <dd>

Valor booleano que indica si existe el grupo local de equipos Terminal Server.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **WBEM \_ E \_ no \_ compatible**.

**Windows server 2008 R2 y Windows server 2008:** Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                         |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

