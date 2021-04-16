---
description: El representador de vídeo se ha destruido o quitado del gráfico.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679127"
---
# <a name="ec_window_destroyed"></a>ventana de EC \_ \_ destruida

El representador de vídeo se ha destruido o quitado del gráfico.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador de vídeo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

El administrador de gráficos de filtros libera esta ventana como el foco, a través de la interfaz [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . No envía la notificación de eventos a la aplicación.

## <a name="remarks"></a>Observaciones

El representador de vídeo envía este evento cuando sale del gráfico de filtros, en el método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) . (El envío del evento cuando se destruye el filtro puede ser demasiado tarde, porque en ese momento también podría destruirse el administrador de gráficos de filtros).

Este evento permite que otros filtros adquieran recursos que dependen del foco de la ventana, como dispositivos de audio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




