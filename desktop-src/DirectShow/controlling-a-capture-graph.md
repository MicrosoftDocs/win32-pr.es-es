---
description: Controlar un gráfico de captura
ms.assetid: e7afafca-e993-4096-bad4-399ee6c67fe9
title: Controlar un gráfico de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00573256c1c010e23dfc598ceca5ac62d772711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119480"
---
# <a name="controlling-a-capture-graph"></a><span data-ttu-id="110ad-103">Controlar un gráfico de captura</span><span class="sxs-lookup"><span data-stu-id="110ad-103">Controlling a Capture Graph</span></span>

<span data-ttu-id="110ad-104">La interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) del Administrador de gráficos de filtro tiene métodos para ejecutar, detener y pausar todo el gráfico.</span><span class="sxs-lookup"><span data-stu-id="110ad-104">The Filter Graph Manager's [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface has methods for running, stopping, and pausing the entire graph.</span></span> <span data-ttu-id="110ad-105">Sin embargo, si el gráfico de filtros tiene secuencias de captura y vista previa, es probable que quiera controlar las dos secuencias de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="110ad-105">If the filter graph has capture and preview streams, however, you probably want to control the two streams independently.</span></span> <span data-ttu-id="110ad-106">Por ejemplo, es posible que quiera obtener una vista previa del vídeo sin capturarlo.</span><span class="sxs-lookup"><span data-stu-id="110ad-106">For example, you might want to preview the video without capturing it.</span></span> <span data-ttu-id="110ad-107">Puede hacerlo mediante el método [**ICaptureGraphBuilder2::ControlStream.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream)</span><span class="sxs-lookup"><span data-stu-id="110ad-107">You can do this through the [**ICaptureGraphBuilder2::ControlStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-controlstream) method.</span></span>

> [!Note]  
> <span data-ttu-id="110ad-108">Este método no funciona al capturar en un archivo de formato de sistemas avanzados (ASF).</span><span class="sxs-lookup"><span data-stu-id="110ad-108">This method does not work when capturing to an Advanced Systems Format (ASF) file.</span></span>

 

<span data-ttu-id="110ad-109">Controlar el flujo de captura</span><span class="sxs-lookup"><span data-stu-id="110ad-109">Controlling the Capture Stream</span></span>

<span data-ttu-id="110ad-110">El código siguiente establece la secuencia de captura de vídeo para que se ejecute durante cuatro segundos, comenzando un segundo después de que se ejecute el gráfico:</span><span class="sxs-lookup"><span data-stu-id="110ad-110">The following code sets the video capture stream to run for four seconds, starting one second after the graph runs:</span></span>


```C++
// Control the video capture stream. 
REFERENCE_TIME rtStart = 10000000, rtStop = 50000000;
const WORD wStartCookie = 1, wStopCookie = 2;  // Arbitrary values.
hr = pBuild->ControlStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                 // Capture filter.
    &rtStart, &rtStop,     // Start and stop times.
    wStartCookie, wStopCookie  // Values for the start and stop events.
);
pControl->Run();
```



<span data-ttu-id="110ad-111">El primer parámetro especifica qué flujo se va a controlar, como GUID de categoría de pin.</span><span class="sxs-lookup"><span data-stu-id="110ad-111">The first parameter specifies which stream to control, as a pin category GUID.</span></span> <span data-ttu-id="110ad-112">El segundo parámetro proporciona el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="110ad-112">The second parameter gives the media type.</span></span> <span data-ttu-id="110ad-113">El tercer parámetro es un puntero al filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="110ad-113">The third parameter is a pointer to the capture filter.</span></span> <span data-ttu-id="110ad-114">Para controlar todas las secuencias de captura del gráfico, establezca el segundo y el tercer parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="110ad-114">To control all the capture streams in the graph, set the second and third parameters to **NULL**.</span></span>

<span data-ttu-id="110ad-115">Los dos parámetros siguientes definen las horas a las que se iniciará y detendrá la secuencia, en relación con la hora en que el gráfico comienza a ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="110ad-115">The next two parameters define the times when the stream will start and stop, relative to the time when the graph starts running.</span></span> <span data-ttu-id="110ad-116">Llame [**a IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="110ad-116">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the graph.</span></span> <span data-ttu-id="110ad-117">Hasta que ejecute el gráfico, el **método ControlStream** no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="110ad-117">Until you run the graph, the **ControlStream** method has no effect.</span></span> <span data-ttu-id="110ad-118">Si el gráfico ya se está ejecutando, la configuración tendrá efecto inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="110ad-118">If the graph is already running, the settings take effect immediately.</span></span>

<span data-ttu-id="110ad-119">Los dos últimos parámetros se usan para obtener notificaciones de eventos cuando la secuencia se inicia y se detiene.</span><span class="sxs-lookup"><span data-stu-id="110ad-119">The last two parameters are used for getting event notifications when the stream starts and stops.</span></span> <span data-ttu-id="110ad-120">Para cada secuencia que controle mediante este método, el gráfico de filtros envía un par de eventos: [**EC \_ STREAM CONTROL \_ \_ STARTED**](ec-stream-control-started.md) cuando se inicia la secuencia y [**EC STREAM CONTROL \_ \_ \_ STOPPED**](ec-stream-control-stopped.md) cuando se detiene la secuencia.</span><span class="sxs-lookup"><span data-stu-id="110ad-120">For each stream that you control using this method, the filter graph sends a pair of events: [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) when the stream starts, and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) when the stream stops.</span></span> <span data-ttu-id="110ad-121">Los valores de **wStartCookie** y **wStopCookie** se usan como segundo parámetro de evento.</span><span class="sxs-lookup"><span data-stu-id="110ad-121">The values of **wStartCookie** and **wStopCookie** are used as the second event parameter.</span></span> <span data-ttu-id="110ad-122">Por lo tanto, *lParam2* en el evento de inicio es igual a **wStartCookie** y *lParam2* en el evento stop es igual a **wStopCookie.**</span><span class="sxs-lookup"><span data-stu-id="110ad-122">Thus, *lParam2* in the start event equals **wStartCookie**, and *lParam2* in the stop event equals **wStopCookie**.</span></span> <span data-ttu-id="110ad-123">El código siguiente muestra cómo obtener estos eventos:</span><span class="sxs-lookup"><span data-stu-id="110ad-123">The following code shows how to get these events:</span></span>


```C++
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch (evCode)
    {
    case EC_STREAM_CONTROL_STARTED: 
    // param2 == wStartCookie
    break;

    case EC_STREAM_CONTROL_STOPPED: 
    // param2 == wStopCookie
    break;
    
    } 
    pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="110ad-124">El **método ControlStream** define algunos valores especiales para las horas de inicio y de detenerse.</span><span class="sxs-lookup"><span data-stu-id="110ad-124">The **ControlStream** method defines some special values for the start and stop times.</span></span>



| <span data-ttu-id="110ad-125">Valor</span><span class="sxs-lookup"><span data-stu-id="110ad-125">Value</span></span> | <span data-ttu-id="110ad-126">Inicio</span><span class="sxs-lookup"><span data-stu-id="110ad-126">Start</span></span>                                  | <span data-ttu-id="110ad-127">Stop</span><span class="sxs-lookup"><span data-stu-id="110ad-127">Stop</span></span>                               |
|-------------|----------------------------------------|---------|
| <span data-ttu-id="110ad-128">MAXLONGLONG</span><span class="sxs-lookup"><span data-stu-id="110ad-128">MAXLONGLONG</span></span> | <span data-ttu-id="110ad-129">Nunca inicie esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="110ad-129">Never start this stream.</span></span>               | <span data-ttu-id="110ad-130">No se detenga hasta que se detenga el gráfico.</span><span class="sxs-lookup"><span data-stu-id="110ad-130">Do not stop until the graph stops.</span></span> |
| <span data-ttu-id="110ad-131">**NULL**</span><span class="sxs-lookup"><span data-stu-id="110ad-131">**NULL**</span></span>    | <span data-ttu-id="110ad-132">Comience inmediatamente cuando se ejecute el gráfico.</span><span class="sxs-lookup"><span data-stu-id="110ad-132">Start immediately when the graph runs.</span></span> | <span data-ttu-id="110ad-133">Detén inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="110ad-133">Stop immediately.</span></span>                  |



 

<span data-ttu-id="110ad-134">Por ejemplo, el código siguiente detiene la secuencia de captura inmediatamente:</span><span class="sxs-lookup"><span data-stu-id="110ad-134">For example, the following code stops the capture stream immediately:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap,
    0, 0,     // Start and stop times.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="110ad-135">Aunque puede detener la secuencia de captura y reiniciarla más adelante, esto creará un intervalo en las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="110ad-135">Although you can stop the capture stream and restart it later, this will create a gap in the time stamps.</span></span> <span data-ttu-id="110ad-136">Durante la reproducción, parecerá que el vídeo se detiene durante la separación (dependiendo del formato de archivo).</span><span class="sxs-lookup"><span data-stu-id="110ad-136">On playback, the video will appear to stall during the gap (depending on the file format).</span></span>

<span data-ttu-id="110ad-137">Controlar la secuencia de vista previa</span><span class="sxs-lookup"><span data-stu-id="110ad-137">Controlling the Preview Stream</span></span>

<span data-ttu-id="110ad-138">Para controlar el pin de vista previa, llame **a ControlStream,** pero establezca el primer parámetro en PIN \_ CATEGORY \_ PREVIEW.</span><span class="sxs-lookup"><span data-stu-id="110ad-138">To control the preview pin, call **ControlStream** but set the first parameter to PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="110ad-139">Esto funciona igual que para PIN CATEGORY CAPTURE, salvo que no se pueden usar horas de referencia para especificar el inicio y la detenerse, porque los fotogramas de vista previa no tienen marcas \_ \_ de tiempo.</span><span class="sxs-lookup"><span data-stu-id="110ad-139">This works just like it does for PIN\_CATEGORY\_CAPTURE, except that you cannot use reference times to specify the start and stop, because the preview frames do not have time stamps.</span></span> <span data-ttu-id="110ad-140">Por lo tanto, debe **usar NULL** o MAXLONGLONG.</span><span class="sxs-lookup"><span data-stu-id="110ad-140">Therefore, you must use **NULL** or MAXLONGLONG.</span></span> <span data-ttu-id="110ad-141">Use **NULL para** iniciar la secuencia de vista previa:</span><span class="sxs-lookup"><span data-stu-id="110ad-141">Use **NULL** to start the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    NULL,    // Start now.
    0,       // (Don't care.)
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="110ad-142">Use MAXLONGLONG para detener la secuencia de versión preliminar:</span><span class="sxs-lookup"><span data-stu-id="110ad-142">Use MAXLONGLONG to stop the preview stream:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap,
    0,               // (Don't care.)
    MAXLONGLONG,     // Stop now.
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="110ad-143">No importa si la secuencia de vista previa procede de un pin de vista previa en el filtro de captura o del filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="110ad-143">It does not matter whether the preview stream comes from a preview pin on the capture filter, or from the Smart Tee filter.</span></span> <span data-ttu-id="110ad-144">El **método ControlStream** funciona de cualquier manera.</span><span class="sxs-lookup"><span data-stu-id="110ad-144">The **ControlStream** method works either way.</span></span>

<span data-ttu-id="110ad-145">Sin embargo, en el caso de las patillas de puerto de vídeo, se producirá un error en el método.</span><span class="sxs-lookup"><span data-stu-id="110ad-145">For video port pins, however, the method will fail.</span></span> <span data-ttu-id="110ad-146">En ese caso, otro enfoque es ocultar la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="110ad-146">In that case, another approach is to hide the video window.</span></span> <span data-ttu-id="110ad-147">Consulte el gráfico para **IVideoWindow** y use el método [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) para mostrar u ocultar la ventana.</span><span class="sxs-lookup"><span data-stu-id="110ad-147">Query the graph for **IVideoWindow**, and use the [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) method to show or hide the window.</span></span>


```C++
// Hide the video window.
IVideoWindow *pVidWin = 0;
hr = pGraph->QueryInterface(IID_IVideoWindow, (void**)&pVidWin);
if (SUCCEEDED(hr))
{
    pVidWin->put_Visible(OAFALSE);
    pVidWin->Release();
}
```



<span data-ttu-id="110ad-148">Además, si llama [**a IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con el valor OAFALSE antes de ejecutar el gráfico, el filtro Representador de vídeo oculta la ventana hasta que especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="110ad-148">Also, if you call [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value OAFALSE before you run the graph, the Video Renderer filter hides the window until you specify otherwise.</span></span> <span data-ttu-id="110ad-149">De forma predeterminada, el representador de vídeo muestra la ventana al ejecutar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="110ad-149">By default, the Video Renderer shows the window when you run the graph.</span></span>

<span data-ttu-id="110ad-150">Comentarios sobre el control stream</span><span class="sxs-lookup"><span data-stu-id="110ad-150">Remarks about Stream Control</span></span>

<span data-ttu-id="110ad-151">El comportamiento predeterminado de un pin es entregar ejemplos cuando se ejecuta el gráfico.</span><span class="sxs-lookup"><span data-stu-id="110ad-151">The default behavior for a pin is to deliver samples when the graph runs.</span></span> <span data-ttu-id="110ad-152">Por ejemplo, suponga que llama a **ControlStream** con PIN \_ CATEGORY CAPTURE pero no con PIN CATEGORY \_ \_ \_ PREVIEW.</span><span class="sxs-lookup"><span data-stu-id="110ad-152">For example, suppose that you call **ControlStream** with PIN\_CATEGORY\_CAPTURE but not with PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="110ad-153">Al ejecutar el gráfico, la secuencia de vista previa se ejecutará inmediatamente, mientras que la secuencia de captura se ejecutará en el momento especificado en **ControlStream**.</span><span class="sxs-lookup"><span data-stu-id="110ad-153">When you run the graph, the preview stream will run immediately, while the capture stream will run at whatever time you specified in **ControlStream**.</span></span>

<span data-ttu-id="110ad-154">Si va a capturar más de una secuencia y enviarla a un filtro mux (por ejemplo, si va a capturar audio y vídeo en un archivo AVI), debe controlar ambas secuencias conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="110ad-154">If you are capturing more than one stream and sending them to a mux filter — for example, if you are capturing audio and video to an AVI file — you should control both streams in tandem.</span></span> <span data-ttu-id="110ad-155">De lo contrario, el filtro mux podría bloquear la espera de una secuencia, ya que intenta intercalar las dos secuencias.</span><span class="sxs-lookup"><span data-stu-id="110ad-155">Otherwise, the mux filter might block waiting for one stream, as it tries to interleave the two streams.</span></span> <span data-ttu-id="110ad-156">Establezca las mismas horas de inicio y de detenerse en todas las secuencias de captura antes de ejecutar el gráfico:</span><span class="sxs-lookup"><span data-stu-id="110ad-156">Set the same start and stop times on all capture streams before running the graph:</span></span>


```C++
pBuild->ControlStream(&PIN_CATEGORY_CAPTURE, 
    
NULL, NULL,       // All capture streams.
    &rtStart, rtStop, 
    wStartCookie, wStopCookie); 
```



<span data-ttu-id="110ad-157">Internamente, el método **ControlStream** usa la interfaz [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) que se expone en los pines del filtro de captura, el filtro Smart Tee (si está presente) y, posiblemente, el filtro mux.</span><span class="sxs-lookup"><span data-stu-id="110ad-157">Internally, the **ControlStream** method uses the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, which is exposed on the pins of the capture filter, the Smart Tee filter (if present), and possibly the mux filter.</span></span> <span data-ttu-id="110ad-158">Puede usar esta interfaz directamente, en lugar de llamar a **ControlStream**, aunque no hay ninguna ventaja concreta para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="110ad-158">You can use this interface directly, instead of calling **ControlStream**, although there is no particular advantage to doing so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="110ad-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="110ad-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="110ad-160">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="110ad-160">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



