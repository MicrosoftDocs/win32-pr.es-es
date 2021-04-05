---
description: Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada especificado por el usuario y lo escribe en un archivo. wav con el nombre único en el directorio actual. Este ejemplo muestra el almacenamiento en búfer basado en temporizador.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080208"
---
# <a name="capturesharedtimerdriven"></a>CaptureSharedTimerDriven

Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada especificado por el usuario y lo escribe en un archivo. wav con el nombre único en el directorio actual. Este ejemplo muestra el almacenamiento en búfer basado en temporizador.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las características siguientes.

-   [MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.
-   [WASAPI](wasapi.md) para las operaciones de administración de secuencias.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ CaptureSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo CaptureSharedTimerDriven, siga estos pasos:

1.  Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo CaptureSharedTimerDriven.
2.  Ejecute el comando `start WASAPICaptureSharedTimerDriven.sln` en el directorio CaptureSharedTimerDriven para abrir el proyecto WASAPICaptureSharedTimerDriven en la ventana de Visual Studio.
3.  En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** . Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPICaptureSharedTimerDriven. vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable WASAPICaptureSharedTimerDriven.exe. Para ejecutarlo, escriba `WASAPICaptureSharedTimerDriven` en una ventana de comandos seguida de los argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de la captura en el dispositivo multimedia predeterminado.

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

En la tabla siguiente se muestran los argumentos.

| Argumento        | Descripción                                                |
|-----------------|------------------------------------------------------------|
| -?              | Muestra la ayuda.                                                |
| -H              | Muestra la ayuda.                                                |
| -l              | Latencia de captura de audio en milisegundos.                     |
| -d              | Duración de la captura de audio en segundos.                         |
| -M              | Deshabilita el uso de MMCSS.                                 |
| -consola        | Use el dispositivo de consola predeterminado.                            |
| -comunicaciones | Use el dispositivo de comunicación predeterminado.                      |
| -multimedia     | Use el dispositivo multimedia predeterminado.                         |
| -punto de conexión       | Use el identificador de extremo especificado en el valor del modificador. |



 

Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de captura. La consola, la comunicación y los dispositivos multimedia predeterminados aparecen seguidos de los dispositivos y los identificadores de punto de conexión. Si no se especifica Duration, el flujo de audio del dispositivo especificado se captura durante 10 segundos. La aplicación escribe los datos capturados en un archivo. wav con el nombre único.

CaptureSharedTimerDriven muestra el almacenamiento en búfer basado en temporizador. En este modo, el cliente debe esperar durante un período de tiempo (la mitad de la latencia, especificada por el valor del modificador-d, en milisegundos). Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de ejemplos del motor. Antes de cada paso de procesamiento en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos de captura disponibles para que los datos no desbordan el búfer de captura. Los datos de audio que se capturan desde el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer basado en eventos. Este modo se muestra en el ejemplo [CaptureSharedEventDriven](capturesharedeventdriven.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



