---
title: LISTBOX. fontStyle
description: El atributo fontStyle especifica o recupera el estilo de fuente para el control de cuadro de lista.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699635"
---
# <a name="listboxfontstyle"></a>LISTBOX. fontStyle

El atributo **fontStyle** especifica o recupera el estilo de fuente para el control de cuadro de lista.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura que contiene uno o varios de los valores siguientes.



| Value     | Descripción           |
|-----------|-----------------------|
| Bold      | Estilo de fuente en negrita.      |
| Cursiva    | Estilo de fuente cursiva.    |
| Subrayado | Estilo de fuente de subrayado. |
| Tacha | Estilo de fuente de tachado. |
| Normal    | Estilo de fuente normal.    |



 

## <a name="remarks"></a>Observaciones

Se puede usar cualquier combinación de valores, separados por espacios. El estilo normal tiene prioridad sobre todos los demás valores, y se omitirán los demás especificados junto con normal.

Para fines de representación, el estilo de fuente predeterminado es normal. El valor predeterminado recuperado de este atributo es "" (cadena vacía).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**LISTBOX. FontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





