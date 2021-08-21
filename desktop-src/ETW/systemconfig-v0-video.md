---
description: 'SystemConfig_V0_Video clase : esta clase es la clase de tipo de evento para los eventos de configuración de vídeo.'
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: SystemConfig_V0_Video clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7121d56d2acf0890a75bccdaf397f184c8780f1f1d3152d3ce2ea4db7781ecaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151374"
---
# <a name="systemconfig_v0_video-class"></a>Clase SystemConfig \_ V0 \_ Video

Esta clase es la clase de tipo de evento para los eventos de configuración de vídeo.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a>Miembros

La **clase SystemConfig \_ V0 \_ Video** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SystemConfig \_ V0 \_ Video** tiene estas propiedades.

<dl> <dt>

**AdapterString**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8), **Max** (256)
</dt> </dl>

Nombre o descripción del adaptador.

</dd> <dt>

**BiosString**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9), **Max** (256)
</dt> </dl>

Nombre del BIOS del adaptador.

</dd> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Número de bits usados para mostrar cada píxel.

</dd> <dt>

**ChipType**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6), **Max** (256)
</dt> </dl>

Nombre del chip del adaptador.

</dd> <dt>

**DACType**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7), **Max** (256)
</dt> </dl>

Nombre del chip del convertidor digital a analógico (DAC) del adaptador.

</dd> <dt>

**DeviceId**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10), **Max** (256)
</dt> </dl>

Dirección u otra información de identificación para dar un nombre único al dispositivo lógico.

</dd> <dt>

**MemorySize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1)
</dt> </dl>

Cantidad máxima de memoria admitida, en bytes.

</dd> <dt>

**StateFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Marcas de estado del dispositivo. Puede ser cualquier combinación razonable de lo siguiente.



| Value                                                                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <dt>**DISPLAY \_ DISPOSITIVO \_ CONECTADO \_ AL \_ ESCRITORIO**</dt> <dt>1 (0x1)</dt> </dl> | El dispositivo forma parte del escritorio.<br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <dt>**DISPLAY \_ CONTROLADOR \_ DE CREACIÓN DE REFLEJO DEL \_ DISPOSITIVO**</dt> <dt>8 (0x8)</dt> </dl>           | Representa un pseudodispositivo que se usa para reflejar el dibujo de la aplicación para conectarse a un equipo remoto u otros propósitos. Un pseudo monitor invisible está asociado a este dispositivo. Por ejemplo, NetMeeting lo usa.<br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <dt>**DISPLAY \_ MODOS \_ DE DISPOSITIVOPRUNED**</dt> <dt>134217728 (0x8000000)</dt> </dl>             | El dispositivo tiene más modos de presentación de los que admiten sus dispositivos de salida.<br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <dt>**DISPLAY \_ DISPOSITIVO \_ PRINCIPAL \_ DISPOSITIVO**</dt> <dt>4 (0x4)</dt> </dl>                 | El escritorio principal está en el dispositivo. Para un sistema con una sola tarjeta de presentación, esto siempre se establece. Para un sistema con varias tarjetas de presentación, solo un dispositivo puede tener este conjunto.<br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <dt>**DISPLAY \_ DISPOSITIVO \_ EXTRAÍBLE**</dt> <dt>32 (0x20)</dt> </dl>                               | El dispositivo es extraíble; no puede ser la pantalla principal.<br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <dt>**DISPLAY \_ COMPATIBLE \_ CON \_ DEVICE VGA**</dt> <dt>16 (0x10)</dt> </dl>               | El dispositivo es compatible con VGA.<br/>                                                                                                                                                                                     |



 

</dd> <dt>

**VRefresh**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Frecuencia de actualización actual, en hercios.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Número actual de píxeles horizontales.

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Número actual de píxeles verticales.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




