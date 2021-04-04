---
title: Apertura de dispositivos de entrada MIDI
description: Apertura de dispositivos de entrada MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Interfaz digital de instrumentos musicales (MIDI), dispositivos de entrada
- MIDI (interfaz digital de instrumentos musicales), dispositivos de entrada
- grabación de audio MIDI, dispositivos de entrada
- Dispositivos de entrada MIDI
- Interfaz digital de instrumentos musicales (MIDI), abrir dispositivos de entrada
- MIDI (interfaz digital de instrumentos musicales), abrir dispositivos de entrada
- grabar audio MIDI, abrir dispositivos de entrada
- apertura de dispositivos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790888"
---
# <a name="opening-midi-input-devices"></a><span data-ttu-id="a50a9-111">Apertura de dispositivos de entrada MIDI</span><span class="sxs-lookup"><span data-stu-id="a50a9-111">Opening MIDI Input Devices</span></span>

<span data-ttu-id="a50a9-112">Para abrir un dispositivo de entrada MIDI para grabar, utilice la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .</span><span class="sxs-lookup"><span data-stu-id="a50a9-112">To open a MIDI input device for recording, use the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function.</span></span> <span data-ttu-id="a50a9-113">Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador en una ubicación de memoria especificada.</span><span class="sxs-lookup"><span data-stu-id="a50a9-113">This function opens the device associated with the specified device identifier and returns a handle of the open device by writing the handle to a specified memory location.</span></span>

<span data-ttu-id="a50a9-114">Si usa la marca de \_ Estado de e/s de MIDI \_ con **midiInOpen**, el sistema utiliza el mensaje [**\_ MOREDATA de MIM**](mim-moredata.md) para avisar de la función de devolución de llamada de la aplicación cuando no está procesando los datos MIDI lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a50a9-114">If you use the MIDI\_IO\_STATUS flag with **midiInOpen**, the system uses the [**MIM\_MOREDATA**](mim-moredata.md) message to alert your application's callback function when it is not processing MIDI data fast enough to keep up with the input device driver.</span></span> <span data-ttu-id="a50a9-115">(El [**mensaje \_ \_ MOREDATA de MIM de mm**](mm-mim-moredata.md) realiza el mismo trabajo con devoluciones de llamada de ventana.</span><span class="sxs-lookup"><span data-stu-id="a50a9-115">(The [**MM\_MIM\_MOREDATA**](mm-mim-moredata.md) message does the same job with window callbacks.</span></span> <span data-ttu-id="a50a9-116">Sin embargo, por motivos de rendimiento, la mayoría de las aplicaciones usarán funciones de devolución de llamada en lugar de devoluciones de llamada de ventana). Si la aplicación procesa datos MIDI en un subproceso independiente, el aumento de la prioridad del subproceso puede tener un impacto significativo en la capacidad de la aplicación para mantener el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="a50a9-116">However, for performance reasons, most applications will use callback functions instead of window callbacks.) If your application processes MIDI data in a separate thread, boosting the thread's priority can have a significant impact on the application's ability to keep up with the data flow.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a50a9-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a50a9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a50a9-118">Grabación de audio MIDI</span><span class="sxs-lookup"><span data-stu-id="a50a9-118">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 