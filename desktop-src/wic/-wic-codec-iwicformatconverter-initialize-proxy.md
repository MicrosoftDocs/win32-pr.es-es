---
description: 'IWICFormatConverter_Initialize_Proxy función: función proxy para el método Initialize.'
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ade363204d9edca08003d5bfef1295c4dabf52aafed037cd2e9ca69b56d02a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206534"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a>Función IWICFormatConverter \_ Initialize \_ Proxy

Función de proxy para el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*THIS \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***

Puntero a este [**objeto IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)

</dd> <dt>

*pISource* \[ En\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Mapa de bits de entrada que se convertirá

</dd> <dt>

*dstFormat* \[ En\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

GUID del formato de píxel de destino.

</dd> <dt>

*dither* \[ En\]
</dt> <dd>

Tipo: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**

[**WICBitmapDitherType usado**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) para la conversión.

</dd> <dt>

*pIPalette* \[ En\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Paleta que se usará para la conversión.

</dd> <dt>

*alphaThresholdPercent* \[ En\]
</dt> <dd>

Tipo: **double**

Umbral alfa que se usará para la conversión.

</dd> <dt>

*paletteTranslate* \[ En\]
</dt> <dd>

Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

Tipo de traducción de paleta que se usará para la conversión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, solo Windows aplicaciones \[ de escritorio de Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




