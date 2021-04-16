---
title: Función de tipo Rect (D2d1helper. h)
description: Crea una estructura de rectángulo que almacena sus coordenadas con el tipo de datos especificado.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Rect (función de tipo Direct2D)
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658243"
---
# <a name="recttype-function"></a><Type>Función Rect

Crea una estructura de rectángulo que almacena sus coordenadas con el tipo de datos especificado.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a>Parámetros de plantilla



| Parámetro | Descripción                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| Tipo      | El tipo de datos que se usa para almacenar las dimensiones del rectángulo. Los valores posibles son **float** y **UINT32**. |



 

## <a name="parameters"></a>Parámetros



| Parámetro | Descripción                                             |
|-----------|---------------------------------------------------------|
| izquierda      | Coordenada x de la esquina superior izquierda del rectángulo.  |
| top       | Coordenada y de la esquina superior izquierda del rectángulo.  |
| right     | Coordenada x de la esquina inferior derecha del rectángulo. |
| abajo    | Coordenada y de la esquina inferior derecha del rectángulo. |



 

## <a name="return-value"></a>Valor devuelto

Estructura de rectángulo que contiene las coordenadas especificadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





