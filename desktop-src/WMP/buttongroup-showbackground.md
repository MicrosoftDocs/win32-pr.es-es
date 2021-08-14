---
title: BUTTONGROUP.showBackground
description: El atributo showBackground especifica o recupera un valor que indica si BUTTONGROUP muestra solo los botones o muestra el mapa de bits completo especificado en el atributo image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- ButtonGROUP.showBackground Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb95b707fa7e14b00e86c5a65949ff9fba3ce3db32745116fa65ca4c53ac1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342678"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP.showBackground

El **atributo showBackground** especifica o recupera un valor que indica si **BUTTONGROUP** muestra solo los botones o muestra el mapa de bits completo especificado en el **atributo image.**

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Valor | Descripción                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Se muestran los botones y el área no ocupada por los botones se dibuja desde el mapa de bits Imagen. |
| false | Predeterminada. Solo se muestran los botones.                                                   |



 

## <a name="remarks"></a>Comentarios

Cuando **showBackground** es true, toda la imagen **principal** estará visible.

Cuando **showBackground** es false, solo se representarán las áreas correspondientes a los colores **mappingImage** asignados. En otras palabras, solo estarán visibles **buttonelements** con su **mappingColor** asignado.

Si se especifica un valor no válido, se mantiene el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





