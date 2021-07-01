---
description: Comandos de OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandos de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119150"
---
# <a name="opm-commands"></a>Comandos de OPM

En esta sección se enumeran los comandos disponibles para [Output Protection Manager](output-protection-manager.md) (OPM).

Para enviar un comando de OPM, llame a [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Para cada comando, se muestra la siguiente información.



| Valor             | Descripción                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de comando | Identifica el comando . Establezca el **miembro guidSetting** de la estructura [**\_ OPM CONFIGURE \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) igual a este valor. |
| Datos de entrada   | Especifica cómo interpretar la matriz **abParameters** en la [**estructura OPM \_ CONFIGURE \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                      |



 

Se definen los siguientes comandos:



| Comando                                                                                                       | Descripción                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SEÑALIZACIÓN DE \_ OPM SET \_ ACP Y \_ \_ CGMSA \_**](opm-set-acp-and-cgmsa-signaling.md)                               | Especifica información sobre la señal de vídeo, aparte del nivel de protección.                      |
| [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md)                                                               | Actualiza el mensaje de renovación del sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP). |
| [**OPM \_ SET \_ PROTECTION \_ LEVEL**](opm-set-protection-level.md)                                               | Establece el nivel de protección para un mecanismo de protección de salida.                                       |
| [**OPM \_ SET \_ PROTECTION \_ LEVEL \_ ACCORDING \_ TO \_ CSS \_ DVD**](opm-set-protection-level-according-to-css-dvd.md) | Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del sistema de codificación de contenido de DVD (CSS). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de OPM](opm-programming-reference.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



