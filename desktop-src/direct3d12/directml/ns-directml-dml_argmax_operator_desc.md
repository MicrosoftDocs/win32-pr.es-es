---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Genera los índices de los elementos con valores máximos dentro de una o varias dimensiones del tensor de entrada.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
f1_keywords:
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 4c2852c3d301a12d318c5e3006b26830c6eaa6e1
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550500"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a>DML_ARGMAX_OPERATOR_DESC estructura (directml.h)

Genera los índices de los elementos con valores máximos dentro de una o varias dimensiones del tensor de entrada.

Cada elemento de salida es el resultado de aplicar una *reducción argmax* en un subconjunto del tensor de entrada. La *función argmax* genera el índice del elemento con valores máximos dentro de un conjunto de elementos de entrada. Los elementos de entrada implicados en cada reducción se determinan mediante los ejes de entrada proporcionados. De forma similar, cada índice de salida es con respecto a los ejes de entrada proporcionados. Si se especifican todos los ejes de entrada, el operador aplica una reducción *argmax* única y genera un único elemento de salida.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a>Members

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor del que se leerá.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. Cada elemento de salida es el resultado de una reducción *argmax* en un subconjunto de elementos de *InputTensor*. 

- *DimensionCount* debe coincidir *con InputTensor.DimensionCount* (se conserva el rango del tensor de entrada).
- *Los* tamaños deben coincidir *con InputTensor.Sizes,* excepto las dimensiones incluidas en los ejes reducidos, que deben tener el tamaño 1.

`AxisCount`

Tipo: **[UINT](../../winprog/windows-data-types.md)**

Número de ejes que se reducirán. Este campo determina el tamaño de la matriz *Axes.*

`Axes`

Tipo: \_ Field_size \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***

Ejes a lo largo de los que se va a reducir. Los valores deben estar en el intervalo `[0, InputTensor.DimensionCount - 1]` .

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Determina qué índice seleccionar cuando varios elementos de entrada tienen el mismo valor.
- **DML_AXIS_DIRECTION_INCREASING** devuelve el índice del primer elemento con valores máximos (por ejemplo, `argmax({3,2,1,2,3}) = 0` )
- **DML_AXIS_DIRECTION_DECREASING** devuelve el índice del último elemento con valores máximos (por ejemplo, `argmax({3,2,1,2,3}) = 4` )

## <a name="examples"></a>Ejemplos

Todos los ejemplos de esta sección usan este mismo tensor de entrada bidimensional.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a>Ejemplo 1. Aplicación de *argmax* a columnas

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a>Ejemplo 2. Aplicación de *argmax* a filas

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a>Ejemplo 3. Aplicar *argmax a* todos los ejes (todo el tensor)

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>Comentarios
Los tamaños de tensor de salida deben ser los mismos que los tamaños de tensor de entrada, excepto los ejes reducidos, que deben ser 1.

Cuando *AxisDirection* es [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), esta API es equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) con [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).

Un subconjunto de esta funcionalidad se expone a través [del operador DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) y se admite en niveles de características anteriores de DirectML.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | De 1 a 8 | INT64, INT32, UINT64, UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |