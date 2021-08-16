---
description: Define valores que especifican las propiedades de una alternativa de reconocimiento. La interfaz de programación de aplicaciones (API) de Tablet PC usa identificadores únicos globales (GUID) para identificar las propiedades de paquete, que en Automation son cadenas constantes.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Constantes RecognitionProperty (Ms constants).h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd18aeae50e0ae08337dd89a494292a7accbb389e6d02f0b990035fbf9644879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856426"
---
# <a name="recognitionproperty-constants"></a>Constantes recognitionProperty

Define valores que especifican las propiedades de una alternativa de reconocimiento. La interfaz de programación de aplicaciones (API) de Tablet PC usa identificadores únicos globales (GUID) para identificar las propiedades de paquete, que en Automation son cadenas constantes.

En la tabla siguiente se enumeran los campos de identificador único global (GUID) de la propiedad alternativa de reconocimiento disponible. Use estos GUID para acceder a las propiedades de un [**objeto IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) llamando al [**método GetPropertyValue.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Nombre constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </dl></td>
<td style="text-align: left;">GUID que identifica la propiedad para el número de línea del <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>objeto IInkRecognitionAlternate.</strong></a> <br/> LineNumber especifica las alternativas con un número de línea determinado.<br/>
<blockquote>
[!Note]<br />
Este campo no se admite para reconocedores de caracteres de Este de Asia.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </dl></td>
<td style="text-align: left;">GUID que identifica la propiedad para la segmentación del <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>objeto IInkRecognitionAlternate.</strong></a> <br/> La segmentación especifica el fragmento de lápiz básico o la unidad que el reconocedor usa para generar un resultado de reconocimiento.<br/>
<blockquote>
[!Note]<br />
Sin implementar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </dl></td>
<td style="text-align: left;">GUID que identifica la propiedad para el punto de acceso de reconocimiento del <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>objeto IInkRecognitionAlternate.</strong></a> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </dl></td>
<td style="text-align: left;">GUID que identifica la propiedad para el número máximo de trazos del resultado del reconocimiento para el <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>objeto IInkRecognitionAlternate.</strong></a> <br/>
<blockquote>
[!Note]<br />
Sin implementar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </dl></td>
<td style="text-align: left;">GUID que identifica la propiedad para la métrica de puntos por pulgada del <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>objeto IInkRecognitionAlternate.</strong></a> <br/>
<blockquote>
[!Note]<br />
Sin implementar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </dl></td>
<td style="text-align: left;">GUID que identifica la propiedad para el nivel de confianza que el reconocedor tiene en el resultado del reconocimiento.<br/>
<blockquote>
[!Note]<br />
La evaluación de confianza solo está disponible para Estados Unidos inglés y todos los reconocedores de gestos en Microsoft Windows XP Tablet PC Edition y Windows Vista. Los métodos que proporcionan la propiedad de confianza para cualquier otro reconocedor devuelven E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </dl></td>
<td style="text-align: left;">GUID que identifica la propiedad para las métricas de línea del objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate,</strong></a> que es la línea para la que se recuperan las métricas. <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentarios

En C++, puede acceder a estas constantes en el archivo de encabezado Msomisión.h, que se encuentra en el directorio : Archivos de programa sdk de <systemdrive> \\ Microsoft Windows \\ \\ \\ v6.0 \\ Include si instaló el SDK en la ubicación predeterminada.

> [!Note]  
> En C++, estas constantes son WCHARs, no BSTR. Conviéndolos en BSTR antes de usarlos. Para obtener más información sobre el tipo de datos BSTR, vea [Using the COM Library](using-the-com-library.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Método AlternatesWithConstantPropertyValues**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[**Propiedad ConfidenceAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[**Propiedad LineAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[**IInkRecognitionAlternates (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




