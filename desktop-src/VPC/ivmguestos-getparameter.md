---
title: Método GetParameter IVMGuestOS (VPCCOMInterfaces. h)
description: Recupera un parámetro con nombre dentro del sistema operativo invitado.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- GetParameter (método, equipo virtual PC)
- Método GetParameter Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, método GetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535182"
---
# <a name="ivmguestosgetparameter-method"></a>IVMGuestOS:: GetParameter (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera un parámetro con nombre dentro del sistema operativo invitado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inParameterName* \[ de\]
</dt> <dd>

Nombre del parámetro. Debe tener entre 1 y 255 caracteres de longitud y no puede contener una barra diagonal inversa ( \) carácter.

</dd> <dt>

*outParameterValue* \[ out, retval\]
</dt> <dd>

Valor del parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                    | Descripción                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | Un parámetro no es válido o no se ha especificado.<br/>                        |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                            | El parámetro es **null**.<br/>                                        |
| <dl> <dt>**Máquina virtual \_ 0xA0040202 \_ agotó el tiempo de \_ espera**</dt> <dt></dt> </dl>                     | La operación no se completó de manera oportuna.<br/>                |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                               |
| <dl> <dt>**Máquina virtual \_ E/s de \_ VM en \_ pausa**</dt> <dt>0xA00400507</dt> </dl>                    | La máquina virtual está en pausa.<br/>                                    |
| <dl> <dt>**Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible**</dt> <dt>0xA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                 |



 

## <a name="remarks"></a>Observaciones

La máquina virtual debe estar en ejecución y los componentes de integración deben instalarse cuando se invoca este método. Este método solo es compatible con sistemas operativos invitados basados en Windows.

Con los componentes de integración de instalados, se agrega automáticamente la clave siguiente al registro del sistema operativo invitado:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**

Cuando se inicia el sistema operativo invitado, los siguientes valores de cadena del registro se rellenan en la clave **Parameters** :

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

