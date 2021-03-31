---
description: Los registros de WSDAPI contienen información de depuración que se puede usar para encontrar la causa principal de los errores de aplicación de WSDAPI.
ms.assetid: 28b4c032-1c9a-4b3a-9a6a-2948456572b2
title: Habilitar el seguimiento de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951f8ddfee6043cc662a456c70960e78ed1a3625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082442"
---
# <a name="enabling-wsdapi-tracing"></a>Habilitar el seguimiento de WSDAPI

Los registros de WSDAPI contienen información de depuración que se puede usar para encontrar la causa principal de los errores de aplicación de WSDAPI. Cuando el seguimiento está habilitado, la información de registro se almacena en un archivo. ETL en una ubicación especificada por el usuario. Este archivo. ETL se puede enviar al soporte técnico de Microsoft para desarrolladores para el análisis de la causa principal. Para obtener información sobre cómo ponerse en contacto con el soporte técnico, vaya a [https://support.microsoft.com](https://support.microsoft.com) .

Este procedimiento debe realizarse dos veces: una vez en el cliente y otra en el host.

**Para habilitar el seguimiento de WSDAPI**

1.  Con el Bloc de notas u otro editor de texto, cree un archivo de texto con el siguiente texto:

    ``` syntax
    "{480217a9-f824-4bd4-bbe8-f371caaf9a0d}" 0xFF 0xFF
    "{649e3596-2620-4d58-a01f-17aefe8185db}" 0xFF 0xFF
    "{96ab095a-9519-4f5c-81ee-c510b0a45463}" 0xFF 0xFF
    "{f9be9c98-10db-4318-bb61-cb0ddea08bf7}" 0xFF 0xFF
    "{db1d0418-105a-4c77-9a25-8f96a19716a4}" 0xFF 0xFF
    "{7e2dbfc7-41e8-4987-bca7-76cadfad765f}" 0xFF 0xFF
    "{8b20d3e4-581f-4a27-8109-df01643a7a93}" 0xFF 0xFF
    "{6d04bf88-60a5-4d02-bc5c-94a20ba490ec}" 0xFF 0xFF
    "{75454210-b231-4fea-b2b4-2cc66d7ae8aa}" 0xFF 0xFF
    "{e176aa66-5cc8-4321-9624-f9c1d2b7bf06}" 0xFF 0xFF
    "{836767a6-af31-4938-b4c0-ef86749a9aef}" 0xFF 0xFF
    ```

2.  Guarde el archivo de texto como `C:\temp\traceguids.txt` y, a continuación, cierre el archivo.
3.  Abra una ventana del símbolo del sistema con permisos elevados.
4.  Ejecute el siguiente comando: **logman.exe Create Trace wsdlog-o c: \\ temp \\ WSD**
5.  Ejecute el siguiente comando: **logman.exe Update wsdlog-PF c: \\ temp \\traceguids.txt**
6.  Ejecute el siguiente comando: **logman.exe Start wsdlog**
7.  Reproduzca el error iniciando el host y el cliente, o presionando F5 en el explorador de red.

**Para deshabilitar el seguimiento de WSDAPI**

1.  Abra una ventana del símbolo del sistema con permisos elevados.
2.  Ejecute el siguiente comando: **logman.exe STOP wsdlog**

Una vez capturado el error de aplicación, los \* archivos. ETL se pueden enviar al soporte técnico de Microsoft. Estos archivos se encuentran en `C:\temp\wsd_*.etl` .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos de diagnóstico de WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introducción con la solución de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[https://support.microsoft.com](https://support.microsoft.com)
</dt> </dl>

 

 



