---
description: Obtenga información sobre el elemento ParameterInit, que define un valor para una instancia de un elemento ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b961ede78b313e7fb3655024705a13f04edb947344493be4fe49ff14b5d00843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947861"
---
# <a name="parameterinit"></a>ParameterInit

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Define un valor para una instancia de un elemento ParameterDef. Un elemento ParameterInit es el destino de la referencia realizada por un elemento ParameterRef.

## <a name="element-tag"></a>Etiqueta de elemento

<ParameterInit>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML   | Detalles                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene el atributo name del elemento ParameterDef que se va a inicializar en el contexto del documento actual.<br/> |



 

Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Nombre o restricción                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | PrintTicket (raíz de PrintTicket)<br/>                                                         |
| Elementos secundarios<br/>  | Valor (uno)<br/>                                                                            |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten elementos secundarios duplicados del mismo nivel.<br/> |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

None

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se inicializa un parámetro en 1. En el ejemplo de [ParameterDef](parameterdef.md) se muestra cómo establecer todos los elementos Property necesarios para este parámetro.

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




