---
title: Método SetParameter de IVMGuestOS (VPCCOMInterfaces.h)
description: Establece un parámetro con nombre dentro del sistema operativo invitado.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- SetParameter method Virtual PC
- SetParameter method Virtual PC , IVMGuestOS interface
- IVMGuestOS interface Virtual PC , SetParameter method
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc99d9b38ab43327b4a435c4128378d49682935
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386714"
---
# <a name="ivmguestossetparameter-method"></a>IVMGuestOS::SetParameter (método)

\[Windows Virtual PC ya no está disponible para su uso a Windows 8. En su lugar, use el proveedor WMI de [Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Establece un parámetro con nombre dentro del sistema operativo invitado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inParameterName* \[ En\]
</dt> <dd>

Nombre del parámetro. Debe tener entre 1 y 255 caracteres y no puede contener un carácter de barra diagonal inversa ( \\ ).

</dd> <dt>

*inParameterValue* \[ En\]
</dt> <dd>

Valor del parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                    | Descripción                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                        |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                         | Un parámetro no es válido o no se ha especificado.<br/>           |
| <dl> <dt>**Máquina virtual \_ Se \_ ha \_ 0xA0040202**</dt> <dt></dt> </dl>                     | La operación no se ha completado a tiempo.<br/>   |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual (VM) no se está ejecutando.<br/>             |
| <dl> <dt>**Máquina virtual \_ E \_ VM \_ PAUSED**</dt> <dt>0xA00400507</dt> </dl>                    | La máquina virtual está en pausa.<br/>                                    |
| <dl> <dt>**Máquina virtual \_ LA \_ CARACTERÍSTICA DE \_ ADICIONES \_ NO \_ ESTÁ**</dt> DISPONIBLE <dt>0XA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                    |



 

## <a name="remarks"></a>Comentarios

La máquina virtual debe estar en ejecución y los componentes de integración deben instalarse cuando se invoca este método. Este método solo se admite para sistemas operativos invitados basados en Windows.

Con los componentes de integración instalados, la siguiente clave se agrega automáticamente al registro del sistema operativo invitado:

**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Virtual Machine \\ Guest \\ Parameters**

Cuando se inicia el sistema operativo invitado, los siguientes valores de cadena del Registro se rellenan en la **clave** Parameters:

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

