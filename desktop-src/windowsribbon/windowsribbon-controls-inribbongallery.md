---
title: Galería de In-Ribbon
description: La galería de In-Ribbon es un control que muestra una colección de elementos o comandos relacionados en la cinta de opciones. Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef644128204fa0b20284dbb63368ef530b0dd0b3
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105676517"
---
# <a name="in-ribbon-gallery"></a>Galería de In-Ribbon

La galería de In-Ribbon es un control que muestra una colección de elementos o comandos relacionados en la cinta de opciones. Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.

-   [Detalles](#details)
-   [Propiedades de la galería de la cinta de opciones](#in-ribbon-gallery-properties)
-   [Temas relacionados](#related-topics)

## <a name="details"></a>Detalles

En la captura de pantalla siguiente se muestra el control Galería de In-Ribbon de la cinta de opciones de Microsoft Paint.

![captura de pantalla de un control inribbongallery en la cinta de opciones de Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a>Propiedades de la galería de In-Ribbon

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control galería de In-Ribbon.

Normalmente, una propiedad de la galería de In-Ribbon se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control Galería de In-Ribbon.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Clave de propiedad</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(solo válido para una galería de elementos)<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.
<blockquote>
[!Note]<br />
Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando <code>UI_INVALIDATIONS_VALUE</code> se pasa como el valor de <em>Flags</em>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento InRibbonGallery**](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> <dt>

[Ejemplo de la galería](windowsribbon-gallerysample.md)
</dt> </dl>

