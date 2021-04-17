---
description: El hash de archivo está disponible con Windows Installer. Para obtener más información, vea MsiGetFileHash y la tabla MsiFileHash. La tabla MsiFileHash solo se puede usar con archivos sin versión.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Ninguno de los archivos tiene una versión con comprobación de hash de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544254"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Ninguno de los archivos tiene una versión con comprobación de hash de archivo

El hash de archivo está disponible con Windows Installer. Para obtener más información, vea [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) y la [tabla MsiFileHash](msifilehash-table.md). La tabla MsiFileHash solo se puede usar con archivos sin versión.

Si el archivo de clave de un componente que se está instalando (Copy-A) tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino (Copy-B), el instalador compara el número de versión, la fecha y el idioma de los dos archivos.

Si ninguno de los archivos tiene un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente. Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.

Tenga en cuenta que este diagrama muestra las [reglas](file-versioning-rules.md)predeterminadas de control de versiones de archivo, que se pueden invalidar estableciendo la propiedad [**REINSTALLMODE**](reinstallmode.md) . El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".

![reglas predeterminadas de control de versiones de archivo cuando se invalida con la configuración de la propiedad REINSTALLMODE](images/waiflow2b.png)

Vea los ejemplos de control de versiones de archivo predeterminados en [reemplazar archivos existentes](replacing-existing-files.md).

-   [Ambos archivos tienen una versión](both-files-have-a-version.md)
-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Un archivo tiene una versión](one-file-has-a-version.md)

 

 



