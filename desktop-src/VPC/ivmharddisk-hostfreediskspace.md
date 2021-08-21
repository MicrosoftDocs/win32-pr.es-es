---
title: Propiedad HostFreeDiskSpace de IVMHardDisk (VPCCOMInterfaces.h)
description: Recupera la cantidad de espacio en disco restante disponible en el host para el disco duro virtual.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- HostFreeDiskSpace, propiedad Virtual PC
- HostFreeDiskSpace, propiedad Virtual PC, interfaz IVMHardDisk
- IVMHardDisk interface Virtual PC , propiedad HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b2b92c8a1253fb4dbefb6db2f2ed9a9d278b907ecfb30e448edb36ec2cbe98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123705"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>IVMHardDisk::HostFreeDiskSpace, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la cantidad de espacio en disco restante disponible en el host para el disco duro virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>Valor de propiedad

Cantidad de espacio en disco restante disponible en el equipo host para el archivo de imagen de disco duro actual. Este valor es una **VARIANTE de** tipo VT \_ DECIMAL.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                            | Significado                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                               | La operación se realizó correctamente.<br/>                                |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                                 | El parámetro es **NULL.**<br/>                                   |
| <dl> <dt>HRESULT \_ DESDE \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt> </dl> | La ruta de acceso al archivo de disco duro virtual actual no es válida.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                         | Se produjo un error inesperado.<br/>                            |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk se define como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

