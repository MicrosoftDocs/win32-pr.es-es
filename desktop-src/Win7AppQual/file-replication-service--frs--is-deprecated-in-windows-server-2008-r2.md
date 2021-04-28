---
description: El servicio de replicación de archivos (FRS) está en desuso en Windows Server 2008 R2
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: El servicio de replicación de archivos (FRS) está en desuso en Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3c34e43daf8346888a32ef76d55f93ac5a563e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088373"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>El servicio de replicación de archivos (FRS) está en desuso en Windows Server 2008 R2

## <a name="platform"></a>Plataforma

 **Servidores:** Windows Server 2008 R2  

## <a name="feature-impact"></a>Impacto en las características

 **Gravedad:** Alto  
**Frecuencia:** Alto  


## <a name="description"></a>Descripción

En Windows Server 2008 R2, el Servicio de replicación de archivos (FRS) no se puede usar para replicar carpetas Sistema de archivos distribuido (DFS) o datos personalizados (que no son SYSVOL). Un controlador de dominio de Windows Server 2008 R2 todavía puede usar FRS para replicar el contenido del recurso compartido SYSVOL en un dominio que usa FRS para replicar el recurso compartido SYSVOL entre controladores de dominio. Sin embargo, los servidores de Windows Server 2008 R2 no pueden usar FRS para replicar el contenido de cualquier réplica establecida aparte del recurso compartido SYSVOL. El Replicación DFS es un reemplazo de FRS y se puede usar para replicar el contenido del recurso compartido SYSVOL, las carpetas DFS, así como otros datos personalizados (que no son SYSVOL). Migre todos los conjuntos de réplicas FRS que no son SYSVOL a Replicación DFS. También se recomienda encarecidamente migrar la replicación del recurso compartido SYSVOL de FRS a Replicación DFS porque Replicación DFS es más sólido, escalable y tiene un mejor rendimiento de replicación que FRS.

## <a name="manifestation"></a>Manifestación

La replicación de FRS de datos personalizados se interrumpirá de forma irreversible tras la actualización local. La única manera de recuperarse de esta situación sería volver a instalar un sistema operativo anterior en el servidor y reinicializar la replicación de FRS. Los servidores que se han actualizado a Windows Server 2008 R2 no pueden participar en grupos de replicación frs existentes.

## <a name="mitigation-of-impact"></a>Mitigación del impacto

Para evitar problemas que puedan producirse como resultado de estos cambios, migre los conjuntos de replicación de FRS personalizados a Replicación DFS. El Replicación DFS cuenta con muchas ventajas con respecto a FRS, incluidas las herramientas de administración mejoradas, un mayor rendimiento y la administración delegada.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [Replicación del sistema de archivos distribuido: preguntas más frecuentes](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Guía de migración de replicación de SYSVOL: Replicación de FRS a DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
