---
description: Contiene información de título sobre la nota de Journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697752"
---
# <a name="title-element"></a>Elemento Title

Contiene información de título sobre la nota de Journal.

## <a name="definition"></a>Definición

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos primarios

[**Diseño de fondo**](stationery-element.md)

## <a name="child-elements"></a>Elementos secundarios

[**TitleArea**](titlearea-element.md)

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
<th>Valores posibles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Estilo</strong></td>
<td><strong>xs:string</strong></td>
<td>Obligatorio</td>
<td>Especifica el tipo de borde que rodea el título de la nota.</td>
<td><ul>
<li>None</li>
<li>SolidSquare</li>
<li>OutlineSquare</li>
<li>SolidRoundRect</li>
<li>OutlineRoundRect</li>
<li>SolidRoundRectDottedBaseline</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DateStyle</strong></td>
<td><strong>xs:string</strong></td>
<td>Obligatorio</td>
<td>Define si el título incluye o no una fecha.</td>
<td><ul>
<li>None</li>
<li>Short</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Color</strong></td>
<td><a href="colortype-simple-type.md"><strong>SimpleType de ColorType</strong></a></td>
<td>Opcionales</td>
<td>Especifica el color del fondo.</td>
<td>Consulte <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Información de elemento



|              |                                                         |
|--------------|---------------------------------------------------------|
| Tipo de elemento | [**TitleType**](titletype-complex-type.md) complexType |
| Espacio de nombres    | urn: schemas-microsoft-com: TabletPC: richink              |
| Nombre del esquema  | Lector de diario                                          |



 

 

 



