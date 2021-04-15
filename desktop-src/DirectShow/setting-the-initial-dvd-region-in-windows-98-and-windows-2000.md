---
description: Configuración de la región de DVD inicial
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Configuración de la región de DVD inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536442"
---
# <a name="setting-the-initial-dvd-region"></a>Configuración de la región de DVD inicial

Es responsabilidad del fabricante del sistema seleccionar una región de DVD inicial para la unidad de DVD en sus equipos.

> [!Note]  
> Solo se pueden usar discos cifrados para establecer la región.

 

### <a name="windows-2000-and-later"></a>Windows 2000 y versiones posteriores

A partir de Windows 2000, se selecciona la región de DVD predeterminada en función de la configuración regional para la que esté configurada la máquina. Windows 2000 siempre establecerá la región inicial de una unidad de DVD usando esta región predeterminada, así como la región del disco, si hay un disco en la unidad. El fabricante del sistema no tiene que hacer nada para establecer la región inicial de las unidades de DVD de Windows 2000 o posterior.

En el caso de las unidades de RPC1, si no hay ningún disco en la unidad durante el arranque, la región predeterminada se establece según la configuración regional de la máquina. Si hay un disco DVD en la unidad durante el arranque, se selecciona la región predeterminada para que sea la región de la unidad, siempre que coincida con una región del disco; de lo contrario, se selecciona la región más baja del disco como la región inicial de la unidad. El usuario (o fabricante del sistema) tiene permitido un cambio restante, en caso de que el valor predeterminado no sea correcto.

En el caso de las unidades de RPC2, si durante el proceso de instalación Windows 2000 detecta que la unidad no tiene ninguna región establecida, intentará seleccionar una región como la anterior, pero solo si hay un disco en la unidad. (Las unidades de RPC1 elegirán la región sin ningún disco en la unidad). Una vez que se establece una región para las unidades de RPC2, no se cambia automáticamente mediante una reinstalación o una instalación limpia del sistema operativo.

El OEM puede establecer una clave del registro que contenga la región de DVD predeterminada del sistema. En el primer arranque, la región de la unidad se establecerá en este valor. La clave del registro en Windows 2000 y versiones posteriores es HKLM \\ System \\ CurrentControlSet \\ control \\ Class \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (Binary).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad de cambio de región de DVD en Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



