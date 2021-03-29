---
description: El método MakePalette crea una paleta lógica a partir de la tabla de colores en un formato de vídeo.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Método CImagePalette. MakePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679037"
---
# <a name="cimagepalettemakepalette-method"></a>CImagePalette. MakePalette, método

El `MakePalette` método crea una paleta lógica a partir de la tabla de colores en un formato de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene la tabla de colores.

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del dispositivo de pantalla, devuelto por la función **EnumDisplayDevices** de GDI. Para usar el dispositivo de pantalla principal, establezca este parámetro en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve un identificador a la paleta. De lo contrario, devuelve **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




