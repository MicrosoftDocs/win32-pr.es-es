---
title: Método IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libera una unidad de host capturada de la unidad de DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Método ReleaseHostDrive Virtual PC
- Método ReleaseHostDrive Virtual PC, interfaz IVMDVDDrive
- Interfaz IVMDVDDrive Virtual PC, método ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422203"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a>IVMDVDDrive:: ReleaseHostDrive (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libera una unidad de host capturada de la unidad de DVD.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                         | Descripción                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                               | La operación se realizó correctamente.<br/>                                      |
| <dl> <dt>**E \_ ERROR**</dt> <dt>0x80004005</dt> </dl>                    | Se produjo un error inesperado.<br/>                                  |
| <dl> <dt>**Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida**</dt> <dt></dt> </dl>         | No se encontró la máquina virtual.<br/>                            |
| <dl> <dt>**Máquina virtual \_ E \_ medio \_ de \_ tipo incorrecto**</dt> <dt>0xA00400728</dt> </dl> | El medio capturado actualmente no es una unidad de disco del host.<br/>             |
| <dl> <dt>**Máquina virtual \_ Unidad E 0xA0040502 \_ \_ no válida**</dt> <dt></dt> </dl>      | No se pudo inicializar la unidad debido a una ubicación de bus no válida.<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>         | Se produjo un error inesperado.<br/>                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive se define como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

