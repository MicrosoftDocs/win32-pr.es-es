---
title: Método ImportAgreementLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Método ImportAgreementLicenseKeyPack Servicios de Escritorio remoto
- Método ImportAgreementLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ImportAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151084"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Método ImportAgreementLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32

Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AgreementType* \[ de\]
</dt> <dd>

Tipo de contrato.

<dt>

0
</dt> <dd>

El paquete de claves de licencia procede de un contrato de licencia por volumen Select (para clientes con 250 o más equipos). El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.

</dd> <dt>

1
</dt> <dd>

El paquete de claves de licencia procede de un contrato de licencia por volumen empresarial para clientes con 250 o más equipos. El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.

</dd> <dt>

2
</dt> <dd>

El paquete de claves de licencia procede de un contrato de licencia por volumen de campus para una institución de educación superior. El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.

</dd> <dt>

3
</dt> <dd>

El paquete de claves de licencia proviene de un contrato de licencia por volumen escolar para instituciones principales y secundarias. El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.

</dd> <dt>

4
</dt> <dd>

El paquete de claves de licencia procede de un contrato de licencia de proveedor de servicios para que los proveedores de servicios de licencias de software de Microsoft se basen mensualmente. El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.

</dd> <dt>

5
</dt> <dd>

El paquete de claves de licencia procede de otro contrato de licencia, como un valor abierto, una licencia Open de varios años y una licencia de suscripción abierta. El parámetro *sAgreementNumber* es el número de contrato proporcionado con la información del programa.

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[ de\]
</dt> <dd>

Número de contrato o número de inscripción. El parámetro *sAgreementNumber* es una cadena numérica de siete dígitos sin guiones.

</dd> <dt>

*ProductVersion* \[ de\]
</dt> <dd>

Versión del producto.

<dt>

0
</dt> <dd>

No se admite.

</dd> <dt>

1
</dt> <dd>

No se admite.

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[ de\]
</dt> <dd>

Tipo de producto.

<dt>

0
</dt> <dd>

El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo. Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.

</dd> <dt>

1
</dt> <dd>

El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario. Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.

</dd> <dt>

2
</dt> <dd>

Este tipo de producto no es válido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ de\]
</dt> <dd>

Número de licencias que se van a importar.

</dd> <dt>

*sSourceLSName* \[ de\]
</dt> <dd>

Nombre del servidor de licencias de origen Escritorio remoto. Este es el nombre completo completo o la dirección IP del servidor.

</dd> <dt>

*sSourceLSProductId* \[ de\]
</dt> <dd>

Identificador del servidor de licencias Escritorio remoto. Es una cadena alfanumérica de 35 caracteres que no puede incluir guiones.

</dd> <dt>

*KeyPackId* \[ enuncia\]
</dt> <dd>

Recibe el identificador del paquete de claves.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





