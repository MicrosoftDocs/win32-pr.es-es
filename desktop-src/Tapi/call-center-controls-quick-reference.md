---
description: Las interfaces del centro de llamadas proporcionan métodos que ponen en cola y distribuyen llamadas dentro de un centro de llamadas.
ms.assetid: 0b9a455d-a614-4698-90ab-e81f020fad3e
title: Referencia rápida de controles de centro de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8aa058d08edee533da950a1ca02a46c2867fd315ad22dff2aa7ba4cd72e1e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948237"
---
# <a name="call-center-controls-quick-reference"></a>Referencia rápida de controles de centro de llamadas

Las interfaces del centro de llamadas proporcionan métodos que ponen en cola y distribuyen llamadas dentro de un centro de llamadas. TAPI 3.x define cinco objetos principales del centro de llamadas: ACDGroup, Agent, AgentHandler, AgentSession y Queue. Todos estos objetos se pueden extender para proporcionar métodos específicos de la implementación. Además, la [**interfaz ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter) del objeto TAPI proporciona métodos para enumerar objetos AgentHandler.



| Interfaz del centro de llamadas                              | Descripción                                                              |
|----------------------------------------------------|--------------------------------------------------------------------------|
| [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)                   | Obtiene información de nombre y cola para un grupo de ACD.                        |
| [**ITACDGroupEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Obtiene la descripción de los eventos de grupo de ACD.                                    |
| [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)                         | Proporciona métodos para establecer y obtener información sobre un agente.         |
| [**ITAgentEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Interfaz de notificación [**para ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                   |
| [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)           | Proporciona métodos para crear objetos del Agente y enumerar grupos de ACD.       |
| [**ITAgentHandlerEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Obtiene la descripción de los eventos AgentHandler.                                 |
| [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)           | Proporciona métodos para establecer y obtener información relacionada con una sesión del agente. |
| [**ITAgentSessionEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Interfaz de notificación [**para ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession).     |
| [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)                         | Obtiene y establece información relativa a una cola.                            |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)               | Obtiene información sobre un evento de cola.                               |
| [**IEnumACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)             | Enumera [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup).                             |
| [**IEnumAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)                   | Enumera [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                                   |
| [**IEnumAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler)     | Enumera [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler).                     |
| [**IEnumAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession)     | Enumera [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession).                     |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)                   | Enumera [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue).                                   |



 

Las interfaces siguientes enumeran los elementos TAPI 3.x según los estándares COM. Estas interfaces constituyen objetos independientes y también se resumen con sus objetos relacionados.



| Interfaz de enumerador                           | Descripción                                          |
|------------------------------------------------|------------------------------------------------------|
| [**IEnumACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)         | Enumera [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup).         |
| [**IEnumAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)               | Enumera [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).               |
| [**IEnumAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler) | Enumera [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler). |
| [**IEnumAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession) | Enumera [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession). |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)               | Enumera [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue).               |



 

Las interfaces de evento (notificación) permiten que una aplicación TAPI 3.x responda a eventos asincrónicos. Debe llamar al método [**ITTAPI::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) y establecer una máscara de filtro de eventos para habilitar la recepción de eventos de solicitud. Si no llama a **ITTAPI::p ut \_ EventFilter**, la aplicación no recibirá ningún evento.



| Interfaz de eventos                                    | Descripción                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------|
| [**ITACDGroupEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Recupera la descripción de los eventos de grupo de distribución automática de llamadas (ACD). |
| [**ITAgentEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Recupera la descripción de los eventos del agente.                                   |
| [**ITAgentHandlerEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Recupera la descripción de los eventos del controlador del agente.                           |
| [**ITAgentSessionEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Recupera la descripción de los eventos de sesión del agente.                           |



 

 

 
