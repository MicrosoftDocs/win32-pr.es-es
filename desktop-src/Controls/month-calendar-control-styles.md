---
title: Estilos de control de calendario mensual (CommCtrl. h)
description: Las constantes de estilo siguientes se usan al crear controles de calendario mensual.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649715"
---
# <a name="month-calendar-control-styles"></a>Estilos de control de calendario mensual

Las constantes de estilo siguientes se usan al crear controles de calendario mensual.



| Constante                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <dt>**MCS \_ DAYSTATE**</dt> </dl>                         | [Versión 4,70](common-control-versions.md). El calendario mensual envía notificaciones de [MCN \_ GETDAYSTATE](mcn-getdaystate.md) para solicitar información acerca de los días que se deben mostrar en negrita.<br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <dt>**MCS \_ MULTIselect**</dt> </dl>                | [Versión 4,70](common-control-versions.md). El calendario mensual permite al usuario seleccionar un intervalo de fechas en el control. De forma predeterminada, el intervalo máximo es de una semana. Puede cambiar el intervalo máximo que se puede seleccionar mediante el mensaje de [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) . <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <dt>**MCS \_ WEEKNUMBERS**</dt> </dl>                | [Versión 4,70](common-control-versions.md). El control de calendario mensual muestra los números de semana (1-52) a la izquierda de cada fila de días. La semana 1 se define como la primera semana que contiene al menos cuatro días. <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <dt>**MCS \_ NOTODAYCIRCLE**</dt> </dl>          | [Versión 4,70](common-control-versions.md). El control de calendario mensual no rodea la fecha "hoy". <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <dt>**MCS en la \_ actualidad**</dt> </dl>                            | [Versión 4,70](common-control-versions.md). El control de calendario mensual no muestra la fecha "hoy" en la parte inferior del control. <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <dt>**MCS \_ NOTRAILINGDATES**</dt> </dl>    | **Windows Vista.** Las fechas de los meses anterior y siguiente no se muestran en el calendario del mes actual.<br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <dt>**MCS \_ SHORTDAYSOFWEEK**</dt> </dl>    | **Windows Vista.** Los nombres de los días cortos se muestran en el encabezado.<br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <dt>**MCS \_ NOSELCHANGEONNAV**</dt> </dl> | **Windows Vista.** La selección no cambia cuando el usuario navega a la siguiente o anterior en el calendario. Esto permite al usuario seleccionar un intervalo mayor que visible.<br/>                                                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





