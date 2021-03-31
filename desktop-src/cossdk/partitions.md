---
description: Especifica las aplicaciones contenidas en cada partición.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Colección de particiones
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807958"
---
# <a name="partitions-collection"></a>Colección de particiones

Especifica las aplicaciones contenidas en cada partición.

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección de **particiones** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**APLICACIONES**](applications.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForPartition**](rolesforpartition.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [Sustituir](#changeable)
-   [Eliminable](#deleteable)
-   [Descripción](#description)
-   [Id](#partitions-collection)
-   [Nombre](#name)

### <a name="changeable"></a>Sustituir



| Entrada | Value |
|----------------|--------------------------------------------------|
| Descripción    | Determina si esta partición es modificable. |
| Access         | ReadWrite                                        |
| Tipo           | Bool                                             |
| Valor predeterminado        | True                                             |
| Sistema mínimo | Windows Server 2003                              |



 

### <a name="deleteable"></a>Eliminable



| Entrada | Value |
|----------------|---------------------------------------------------|
| Descripción    | Determina si se puede eliminar esta partición. |
| Access         | ReadWrite                                         |
| Tipo           | Bool                                              |
| Valor predeterminado        | True                                              |
| Sistema mínimo | Windows Server 2003                               |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|---------------------------------------------------------------------|
| Descripción    | Esta propiedad representa la descripción que identifica la partición. |
| Access         | ReadWrite                                                           |
| Tipo           | String                                                              |
| Predeterminado        | ""                                                                  |
| Sistema mínimo | Windows Server 2003                                                 |



 

### <a name="id"></a>id



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Un GUID que representa la partición. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                          |
| Tipo           | String                                                                                                                                                             |
| Predeterminado        | <Generated>                                                                                                                                                  |
| Sistema mínimo | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el nombre de la partición. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                 |
| Predeterminado        | "Nueva partición"                                                                                                                                                                                                                        |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
