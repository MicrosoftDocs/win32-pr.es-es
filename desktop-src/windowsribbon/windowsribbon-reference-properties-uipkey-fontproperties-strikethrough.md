---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica la propiedad Tachado \_ PKEY FontProperties de la \_ interfaz de \_ usuario.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746172ec2209861615375e73dee3f2336950a2dd93e76b33893190e9f7e8bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850315"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>UI \_ PKEY \_ FontProperties \_ Strikethrough

Identifica la propiedad Tachado \_ PKEY FontProperties de la \_ interfaz de \_ usuario.

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Comentarios

Una aplicación usa la interfaz de usuario PKEY FontProperties Strikethrough para consultar \_ el estado del botón \_ \_ **Tachado.**

El valor de propiedad es de la [**\_ enumeración FONTPROPERTIES de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) interfaz de usuario.

El valor predeterminado es `UI_FONTPROPERTIES_NOTSET`.

En la siguiente captura de pantalla se muestra **el botón Tachado** del control [**FontControl de la cinta**](windowsribbon-element-fontcontrol.md)de opciones.

![captura de pantalla del elemento fontcontrol con el atributo richfont establecido en true.](images/markup/fontcontrol-strikethrough.png)

En la tabla siguiente se describen las propiedades y el resultado de la interfaz de usuario.



|   Propiedad                       |    Resultado de la interfaz de usuario                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **El botón tachado** está deshabilitado y solo la aplicación puede establecerlo. |
| `UI_FONTPROPERTIES_NOTSET`       | **El botón Tachado** no está seleccionado.                                    |
| `UI_FONTPROPERTIES_SET`          | **El botón Tachado** está seleccionado.                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**FONTPROPERTIES \_ de la interfaz de usuario**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 