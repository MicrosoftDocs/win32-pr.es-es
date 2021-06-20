---
description: Obtenga información sobre cómo construir un PrintTicket genérico, en caso de que el documento PrintCapabilities del dispositivo no esté disponible.
ms.assetid: 1f991b6b-8443-4234-ad46-dc4220e34c5c
title: Crear un printticket genérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e611205663138b9cc3c0d3cd315c2c19d2d7e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409528"
---
# <a name="creating-a-generic-printticket"></a>Crear un printticket genérico

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Si el documento PrintCapabilities del dispositivo no está disponible o si el dispositivo de destino es desconocido, debe construir un PrintTicket genérico. Dado que no hay ningún documento PrintCapabilities que proporciona un conjunto de elementos Feature y Option, o parámetros, las instancias admitidas de estos tipos de elementos deben obtenerse directamente de las palabras clave de esquema de impresión.

Los pasos que se muestran en la lista siguiente se deben usar al crear un PrintTicket genérico.

1.  Cree un documento XML vacío que contenga la raíz PrintTicket. Asigne un prefijo de espacio de nombres al espacio de nombres Esquema de impresión. Especifique la versión del esquema.

2.  Examine las instancias de característica en las palabras clave de esquema de impresión y determine cuál de ellas desea definir en su PrintTicket. Agregue estas instancias de características a PrintTicket. Al transferir una subfeature, debe transferir la característica primaria y conservar la relación de elementos primarios y secundarios entre la característica y la subfeature en PrintTicket.

    Para cada instancia de característica que transfiera, determine qué instancias de option son aplicables a su PrintTicket. Desde este conjunto de instancias option, transfiera cada instancia de Option completa tal como aparece en el esquema de impresión y, a continuación, quite todas las instancias de propiedad que estén presentes, con la posible excepción de las que tienen importancia para printticket. Mantenga todas las instancias de ScoredProperty y asegúrese de conservar su ubicación. son una parte intrínseca de la definición de opción.

3.  También puede agregar instancias de propiedad a cualquier ScoredProperty. Los elementos de propiedad solo son aplicables si el proveedor PrintTicket admite explícitamente su uso. Cada proveedor debe documentar el propósito y el uso de todas las instancias de propiedad admitidas. Dado que no tiene idea de qué proveedor procesará PrintTicket, es posible que desee anexar solo las instancias de propiedad que son compatibles explícitamente con el proveedor PrintTicket del sistema.

4.  Si las palabras clave de esquema de impresión establecen la propiedad SelectionType en PickMany para una característica determinada, puede seleccionar más de una opción para esa característica, siempre que la opción designada como IdentityOption no sea una de las seleccionadas. IdentityOption en el esquema de impresión tiene el mismo efecto que la opción None en los archivos PPD postscript y los archivos GPD unidrv; sirve como no operativo.

5.  Examine las palabras clave de esquema de impresión para las instancias de ParameterDef que se deben inicializar en printticket. Para cada instancia de ParameterDef de este tipo, seleccione el valor que se usará en la instancia ParameterInit en PrintTicket. Este valor debe ser del tipo de datos correcto, debe estar dentro del intervalo definido en la instancia de ParameterDef y debe cumplir todos los demás requisitos especificados en la instancia de ParameterDef. Use una instancia parameterInit para inicializar el parámetro en el valor que ha seleccionado.

    Si va a desarrollar un componente de interfaz de usuario (UI), diseñe los métodos de generación PrintTicket para que los usuarios puedan escribir el valor del elemento ParameterInit. Además, el método de entrada de la interfaz de usuario debe observar y cumplir las restricciones de entrada especificadas por el elemento ParameterDef asociado.

6.  Examine el contenido de cada instancia de Option que aparece en PrintTicket para ver si hay repeticiones de ParameterRef. Si aún no aparece una instancia de ParameterInit correspondiente en PrintTicket, siga el paso anterior para crear una instancia de ParameterInit en PrintTicket. El propósito de esta instancia parameterInit es inicializar el parámetro al que hace referencia la instancia ParameterRef.

7.  Tenga en cuenta que es posible que el dispositivo que procesa el trabajo no admita todas las características especificadas en PrintTicket. Tenga en cuenta también que una característica con nombre podría ser compatible, pero una opción especificada de esa característica podría no ser. Las mismas advertencias se aplican a los parámetros. Incluso si un dispositivo admite un parámetro con nombre, es posible que el valor especificado en la instancia ParameterInit no esté dentro del intervalo válido para el dispositivo.

8.  Examine las palabras clave de esquema de impresión para las instancias de propiedad que deben estar presentes en printticket. Agregue una instancia de Property para cada una de ellas a PrintTicket y proporcione un valor adecuado para ella mediante el tipo de elemento Value. Asegúrese de que las instancias de propiedad se encuentran correctamente dentro de PrintTicket. Asegúrese de consultar el esquema PrintTicket en lugar del esquema PrintCapabilities.

9.  Examine las instancias de propiedad opcionales definidas en el esquema PrintTicket. Si hay alguna de estas instancias de propiedad que debe estar en printticket, crámelas en printticket.

10. Los elementos secundarios del mismo tipo de elemento no pueden anidar en una profundidad de más de 10 elementos. Esta regla se aplica de forma independiente a cada tipo de elemento que se puede definir.

> [!Note]  
> El contenido XML de PrintTicket DEBE codificarse mediante UTF-8 o UTF-16.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



