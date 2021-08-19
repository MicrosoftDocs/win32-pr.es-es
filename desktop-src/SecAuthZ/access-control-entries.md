---
description: Una entrada de control de acceso (ACE) es un elemento de una lista de control de acceso (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Access Control entradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adcc382da130c57c55b869c47c8837c7780a7cff4e6dbdd881e55aa7b724dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785655"
---
# <a name="access-control-entries"></a>Access Control entradas

Una [*entrada de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACE) es un elemento de una lista de control de [*acceso*](/windows/desktop/SecGloss/a-gly) (ACL). Una ACL puede tener cero o más ACE. Cada ACE controla o supervisa el acceso a un objeto por un administrador de confianza especificado. Para obtener información sobre cómo agregar, quitar o cambiar las ACL de un objeto, vea Modificar las ACL de un objeto [en C++.](modifying-the-acls-of-an-object-in-c--.md)

Hay seis tipos de ACE, tres de los cuales son compatibles con todos los objetos protegibles. Los otros tres tipos son [AE específicas del objeto](object-specific-aces.md) que admiten los objetos de servicio de directorio.

Todos los tipos de ACE contienen la siguiente información de control de acceso:

-   Identificador [de seguridad](security-identifiers.md) (SID) que identifica el administrador de confianza al que se aplica la ACE. [](trustees.md)
-   Máscara [*de acceso*](/windows/desktop/SecGloss/a-gly) que especifica los derechos de [acceso](access-rights-and-access-masks.md) controlados por la ACE.
-   Marca que indica el tipo de ACE.
-   Conjunto de marcas de bits que determinan si los contenedores u objetos secundarios pueden heredar la ACE del objeto principal al que está asociada la ACL.

En la tabla siguiente se enumeran los tres tipos ace admitidos por todos los objetos protegibles.



| Tipo               | Descripción                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE con acceso denegado  | Se usa en una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) para denegar los derechos de acceso a un administrador de confianza.                                       |
| ACE con acceso permitido | Se usa en una DACL para permitir derechos de acceso a un administrador de confianza.                                                                                                                                                                                              |
| ACE de auditoría del sistema   | Se usa en [*una lista de control de*](/windows/desktop/SecGloss/s-gly) acceso del sistema (SACL) para generar un registro de auditoría cuando el administrador de confianza intenta ejercer los derechos de acceso especificados. |



 

Para obtener una tabla de A ACE específicas del objeto, vea [AEC específicas del objeto](object-specific-aces.md).

> [!Note]  
> Actualmente no se admiten las ACE de objeto de alarma del sistema.

 

 

 
