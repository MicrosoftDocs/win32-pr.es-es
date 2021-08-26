---
description: El conjunto de propiedades protección de copia de DVD proporciona autenticación de información de protección de copia de descifradores de hardware o software. Use esta propiedad establecida para evitar la copia no autorizada de DVD-Video grabado previamente.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Conjunto de propiedades de protección de copia de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76034c0ac9b310d446f142d31b96ea2edbe6b725
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477354"
---
# <a name="dvd-copy-protection-property-set"></a>Conjunto de propiedades de protección de copia de DVD

El conjunto de propiedades protección de copia de DVD proporciona autenticación de información de protección de copia de descifradores de hardware o software. Use esta propiedad establecida para evitar la copia no autorizada de DVD-Video grabado previamente.

Microsoft proporciona software que facilita el proceso de autenticación requerido por el esquema de cifrado, lo que permite que una unidad DE DVD-ROM autentique y transfiera claves con un descifrador de DVD. Microsoft no tiene planes actuales para enviar un descifrador de DVD y, en su lugar, proporciona código de sistema operativo que actuará como agente para habilitar la autenticación de descifradores de hardware o software.

El navegador de DVD inicia y controla el proceso de intercambio de claves. El minidriver de DVD solo necesita implementar las siguientes propiedades. Otros componentes controlan el resto.

Cada flujo de entrada de DVD recibirá las propiedades de protección de copia. Esto es así incluso si el mismo hardware controla todas las secuencias de DVD.

En la siguiente información se presentan las constantes y los tipos de datos necesarios que se usarán para este conjunto de propiedades en las llamadas a [**métodos IKsPropertySet.**](ikspropertyset.md) Proporciona valores para los parámetros **GUID** (*guidPropSet*), property ID (*dwPropID*) y property data type (*pPropData*).



| Etiqueta | Valor |
|-------------------|---------------------------|
| GUID del conjunto de propiedades | CopyProt de AM \_ KSPROPSETID \_ |



 




| Id. de propiedad | Descripción | 
|-------------|-------------|
| <a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a> | Consulta si la salida del vídeo es vídeo de componentes análogos de definición estándar. | 
| AM_PROPERTY_COPY_MACROVISION | Se trata de una propiedad de solo conjunto. Esta propiedad establece el nivel de protección de copia análoga para el codificador ENCODER en el extremo de salida del pin receptor. Usa <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>. | 
| AM_PROPERTY_DVDCOPY_CHLG_KEY | En esta propiedad se admiten las operaciones get y set. Una operación get solicita al descodificador que proporcione su clave de desafío de bus. Una operación set proporciona al descodificador la clave de desafío de bus de la unidad de DVD. Los datos pasados en esta propiedad serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_DEC_KEY2 | Se trata de una propiedad get-only. Esta propiedad solicita que la clave de bus 2 del descodificador se transfiera a la unidad de DVD. Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_DISC_KEY | Propiedad de solo establecimiento. Esto proporciona la tecla de disco. La clave es una estructura de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>tipo</strong></a>AM_DVDCOPY_DISCKEY . | 
| AM_PROPERTY_DVDCOPY_DVD_KEY1 | Se trata de una propiedad de solo conjunto. Esta propiedad proporciona la clave 1 del bus de unidad de DVD al descodificador. Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_REGION | El código de región solicita la definición de región en la que el descodificador puede reproducirse según lo definido por el consorcio de DVD. Esta región se define como una <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>estructura DVD_REGION</strong></a> datos. | 
| AM_PROPERTY_DVDCOPY_SET_COPY_STATE | Tanto get como set se admiten en esta propiedad. Se llama primero a Get para determinar si se requiere autenticación. Las propiedades del conjunto son indicaciones sobre qué fase de negociación de protección de copia está especificando el filtro. Los datos pasados serán una estructura de tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>. | 
| AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT | Si esta propiedad es <strong>TRUE,</strong>el navegador de DVD no envía <strong>AM_UseNewCSSKey</strong> ejemplos antes de negociar la clave de disco. Vea <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br /> Solo lectura. Los datos de propiedad son <strong>un valor BOOL.</strong><br /><blockquote>[!Note]<br />Se aplica a Windows 7.</blockquote><br /> | 
| AM_PROPERTY_DVDCOPY_TITLE_KEY | Se trata de una propiedad de solo conjunto. Esto proporciona la clave de título del contenido actual. La clave es una estructura de <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>tipo</strong></a>AM_DVDCOPY_TITLEKEY . | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 




