---
description: La clase de dispositivo midi/in consta de secuenciadores MIDI que se usan para la entrada. Puede acceder a estos dispositivos mediante las funciones de MIDI, que se describen en Platform Software Development Kit (SDK).
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: midi/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309fe510b08a1e86ef6a00b34a9e3d3282c993babe78eb45aeb6ebb0dab1eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659955"
---
# <a name="midiin"></a>midi/in

La clase de dispositivo midi/in consta de secuenciadores MIDI que se usan para la entrada. Puede acceder a estos dispositivos mediante las funciones de MIDI, que se describen en Platform Software Development Kit (SDK).

Las [**funciones lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) estableciendo el **miembro dwStringFormat** en el valor STRINGFORMAT BINARY y \_ anexando este miembro adicional:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

El **miembro DeviceId** es el identificador de un dispositivo MIDI cerrado. Este identificador se usa en una llamada a la [**función midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) para abrir el dispositivo para la entrada. Puede usar el identificador de dispositivo resultante para registrar datos DE LÍNEA desde la línea o el dispositivo de teléfono.

Para obtener más información sobre las funciones de MIDI, vea [**Funciones multimedia**](../multimedia/multimedia-functions.md).

 

 
