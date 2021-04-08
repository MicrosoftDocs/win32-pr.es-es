---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994350"
---
# <a name="deactivateinput-event"></a>Evento DeactivateInput

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando un cliente deja de ser de entrada y no está activo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent * * * \_ DeactivateInput* *  **(ByVal** *CharacterID ** * *)*



| Parte          | Descripción                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter que hace que el cliente se convierta en no de entrada-activo. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Un cliente que no es de entrada-activo ya no recibe eventos de mouse o de voz del servidor (a menos que vuelva a ser de entrada-activo). El servidor envía este evento solo al cliente que no es de entrada-activo.

Este evento se produce cuando la aplicación cliente es de entrada y el usuario elige el título de otro cliente en el menú emergente de un carácter o en la ventana comandos de voz, o bien se llama al método [**Activar**](activate-method.md) y se establece el parámetro de **Estado** en 0. También se puede producir cuando el usuario selecciona el nombre de otro carácter haciendo clic o hablando. También recibirá este evento cuando el carácter esté oculto u otro carácter esté visible.

### <a name="see-also"></a>Consulte también

[**Evento ActivateInput**](activateinput-event.md)


 

 




