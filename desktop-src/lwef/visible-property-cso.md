---
title: Propiedad Visible (objeto Commands)
description: Obtenga información sobre la propiedad Visible del objeto Commands, que determina si el título de la colección Commands aparece en el menú emergente del carácter.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396260"
---
# <a name="visible-property-commands-object"></a>Propiedad Visible (objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece un valor que determina si el título de la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Commands.Visible* *  \[  =  *boolean*\]



| Parte      | Descripción                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece en el menú emergente del carácter. <br/> **True** Aparece el título.<br/> **False** El título no aparece.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para que el título aparezca en el menú emergente del carácter cuando la aplicación no sea el cliente activo de entrada, esta propiedad debe establecerse en **True** y la propiedad [**Caption**](caption-property.md) para la colección Commands. Además, esta propiedad debe establecerse en **True** para que los comandos de la colección aparezcan en el menú emergente cuando la aplicación esté activa en la entrada.

 

