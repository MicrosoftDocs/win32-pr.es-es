---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Vuelve a muestrear los elementos del tensor de origen al de destino, utilizando los factores de escala para calcular el tamaño del tensor de destino. Puede usar un modo de interpolación lineal o de vecino más próximo.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550400"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>DML_RESAMPLE1_OPERATOR_DESC estructura (directml.h)
Vuelve a muestrear los elementos del tensor de origen al de destino, utilizando los factores de escala para calcular el tamaño del tensor de destino. Puede usar un modo de interpolación lineal o de vecino más próximo. El operador admite la interpolación en varias dimensiones, no solo en 2D. Por lo tanto, puede mantener el mismo tamaño espacial, pero interpolar entre canales o lotes. La relación entre las coordenadas de entrada y salida es la siguiente.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de entrada.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los datos de salida.


`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Este campo determina el tipo de interpolación que se usa para elegir los píxeles de salida.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Usa el *algoritmo Vecino más* próximo, que elige el elemento de entrada más cercano al centro de píxeles correspondiente para cada elemento de salida.

- **DML_INTERPOLATION_MODE_LINEAR**. Usa el *algoritmo Quadrilinear,* que calcula el elemento de salida haciendo el promedio ponderado de los 2 elementos de entrada vecinos más cercanos por dimensión. Puesto que se pueden volver a muestrear las cuatro dimensiones, el promedio ponderado se calcula en un total de 16 elementos de entrada para cada elemento de salida.


`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de valores de las matrices a las que apuntan *Scales*, *InputPixelOffsets* y *OutputPixelOffsets.* Este valor debe coincidir con el recuento de dimensiones *de InputTensor* y *OutputTensor*, que debe ser 4.


`Scales`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Escalas que se aplicarán al volver > cambiar el tamaño de la entrada, donde escala > 1 escala verticalmente la imagen y escala < 1 reducir verticalmente la imagen para esa dimensión. Tenga en cuenta que no es necesario que las escalas sean exactamente `OutputSize / InputSize` . Si la entrada después del escalado es mayor que el límite de salida, la recortaremos al tamaño de salida. Por otro lado, si la entrada después del escalado es menor que el límite de salida, se fijan los bordes de salida.


`InputPixelOffsets`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Desplazamientos que se van a aplicar a los píxeles de entrada antes de volver a realizar el muestreo. Cuando este valor es , se usa la esquina superior izquierda del píxel en lugar de su centro, lo que normalmente no `0` dará el resultado esperado. Para volver a muestrear la imagen mediante el centro de los píxeles y obtener el mismo comportamiento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), este valor debe ser `0.5` .


`OutputPixelOffsets`

Tipo: \_ Tamaño de campo \_ \_ (DimensionCount) **const [FLOAT](../../winprog/windows-data-types.md) \***

Desplazamientos que se aplicarán a los píxeles de salida después de volver a realizar el muestreo. Cuando este valor es , se usa la esquina superior izquierda del píxel en lugar de su centro, lo que normalmente no `0` dará el resultado esperado. Para volver a muestrear la imagen mediante el centro de los píxeles y obtener el mismo comportamiento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), este valor debe ser `-0.5` .


## <a name="remarks"></a>Comentarios
Cuando *InputPixelOffsets* se establece en 0,5 y *OutputPixelOffsets* se establece en -0,5, este operador es equivalente a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputTensor* y *OutputTensor* deben tener el mismo *DataType.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |