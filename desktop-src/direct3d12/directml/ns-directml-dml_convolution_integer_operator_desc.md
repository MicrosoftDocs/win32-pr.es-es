---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Realiza una convolución del *filterTensor* con *InputTensor*. Este operador realiza la convolución hacia delante en datos enteros.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: 07406155be9ae5f78fbf5f3b7fcd750aa4631dbc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803381"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="8de90-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="8de90-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8de90-105">Realiza una convolución del *filterTensor* con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="8de90-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="8de90-106">Este operador realiza la convolución hacia delante en datos enteros.</span><span class="sxs-lookup"><span data-stu-id="8de90-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="8de90-107">También se pueden usar tensores de punto cero opcionales para restar valores de punto cero de la entrada y filtrar tensor.</span><span class="sxs-lookup"><span data-stu-id="8de90-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8de90-108">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="8de90-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="8de90-109">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="8de90-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8de90-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8de90-110">Syntax</span></span>
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a><span data-ttu-id="8de90-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8de90-111">Members</span></span>

`InputTensor`

<span data-ttu-id="8de90-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8de90-113">Tensor que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="8de90-113">A tensor containing the input data.</span></span> <span data-ttu-id="8de90-114">Las dimensiones esperadas de *InputTensor* son `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="8de90-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="8de90-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8de90-116">Tensor opcional que contiene los datos de punto cero de entrada.</span><span class="sxs-lookup"><span data-stu-id="8de90-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="8de90-117">Las dimensiones esperadas de *InputZeroPointTensor* son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="8de90-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="8de90-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8de90-119">Tensor que contiene los datos de filtro.</span><span class="sxs-lookup"><span data-stu-id="8de90-119">A tensor containing the filter data.</span></span> <span data-ttu-id="8de90-120">Las dimensiones esperadas de *FilterTensor* son `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="8de90-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="8de90-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8de90-122">Tensor opcional que contiene los datos de punto cero de filtro.</span><span class="sxs-lookup"><span data-stu-id="8de90-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="8de90-123">Las dimensiones esperadas de *FilterZeroPointTensor* son si se requiere una cuantificación por tensor o si se requiere una cuantificación `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` por canal.</span><span class="sxs-lookup"><span data-stu-id="8de90-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="8de90-124">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8de90-125">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="8de90-125">The tensor to write the results to.</span></span> <span data-ttu-id="8de90-126">Las dimensiones esperadas de *OutputTensor* son `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="8de90-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="8de90-127">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8de90-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8de90-128">Número de dimensiones espaciales para la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="8de90-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="8de90-129">Las dimensiones espaciales son las dimensiones inferiores del *objeto FilterTensor* de convolución.</span><span class="sxs-lookup"><span data-stu-id="8de90-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="8de90-130">Este valor también determina el tamaño de las matrices *Strides*, *Posición,* *StartPadding* y *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="8de90-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="8de90-131">Solo se admite un valor de 2.</span><span class="sxs-lookup"><span data-stu-id="8de90-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="8de90-132">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-132">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="8de90-133">Matriz que contiene los avances de la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="8de90-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="8de90-134">Estos strides se aplican al filtro de convolución.</span><span class="sxs-lookup"><span data-stu-id="8de90-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="8de90-135">Son independientes de los avances de tensor incluidos [en DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="8de90-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="8de90-136">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-136">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="8de90-137">Matriz que contiene las sutenciones de la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="8de90-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="8de90-138">Las reparaciones son avances aplicados a los elementos del kernel de filtro.</span><span class="sxs-lookup"><span data-stu-id="8de90-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="8de90-139">Esto tiene el efecto de simular un kernel de filtro mayor mediante el relleno de los elementos internos del kernel de filtro con ceros.</span><span class="sxs-lookup"><span data-stu-id="8de90-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="8de90-140">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-140">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="8de90-141">Matriz que contiene los valores de relleno que se aplicarán al principio de cada dimensión espacial del tensor de entrada y filtro de la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="8de90-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="8de90-142">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="8de90-142">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="8de90-143">Matriz que contiene los valores de relleno que se aplicarán al final de cada dimensión espacial del tensor de entrada y filtro de la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="8de90-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="8de90-144">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8de90-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8de90-145">Número de grupos en los que se va a dividir la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="8de90-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="8de90-146">*GroupCount* se puede usar para lograr la convolución por profundidad estableciendo *GroupCount* igual al recuento de canales de entrada.</span><span class="sxs-lookup"><span data-stu-id="8de90-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="8de90-147">Esto divide la convolución en una convolución independiente por canal de entrada.</span><span class="sxs-lookup"><span data-stu-id="8de90-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="8de90-148">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="8de90-148">Availability</span></span>
<span data-ttu-id="8de90-149">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8de90-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8de90-150">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="8de90-150">Tensor constraints</span></span>
* <span data-ttu-id="8de90-151">*FilterTensor* y *FilterZeroPointTensor* deben tener el mismo *datatype*.</span><span class="sxs-lookup"><span data-stu-id="8de90-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="8de90-152">*InputTensor* y *InputZeroPointTensor* deben tener el mismo *tipo de datos*.</span><span class="sxs-lookup"><span data-stu-id="8de90-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8de90-153">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="8de90-153">Tensor support</span></span>
| <span data-ttu-id="8de90-154">Tensor</span><span class="sxs-lookup"><span data-stu-id="8de90-154">Tensor</span></span> | <span data-ttu-id="8de90-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="8de90-155">Kind</span></span> | <span data-ttu-id="8de90-156">Dimensions</span><span class="sxs-lookup"><span data-stu-id="8de90-156">Dimensions</span></span> | <span data-ttu-id="8de90-157">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="8de90-157">Supported dimension counts</span></span> | <span data-ttu-id="8de90-158">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="8de90-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="8de90-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8de90-159">InputTensor</span></span> | <span data-ttu-id="8de90-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="8de90-160">Input</span></span> | <span data-ttu-id="8de90-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="8de90-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="8de90-162">4</span><span class="sxs-lookup"><span data-stu-id="8de90-162">4</span></span> | <span data-ttu-id="8de90-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="8de90-163">INT8, UINT8</span></span> |
| <span data-ttu-id="8de90-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="8de90-164">InputZeroPointTensor</span></span> | <span data-ttu-id="8de90-165">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="8de90-165">Optional input</span></span> | <span data-ttu-id="8de90-166">{ 1, 1, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="8de90-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="8de90-167">4</span><span class="sxs-lookup"><span data-stu-id="8de90-167">4</span></span> | <span data-ttu-id="8de90-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="8de90-168">INT8, UINT8</span></span> |
| <span data-ttu-id="8de90-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="8de90-169">FilterTensor</span></span> | <span data-ttu-id="8de90-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="8de90-170">Input</span></span> | <span data-ttu-id="8de90-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="8de90-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="8de90-172">4</span><span class="sxs-lookup"><span data-stu-id="8de90-172">4</span></span> | <span data-ttu-id="8de90-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="8de90-173">INT8, UINT8</span></span> |
| <span data-ttu-id="8de90-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="8de90-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="8de90-175">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="8de90-175">Optional input</span></span> | <span data-ttu-id="8de90-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span><span class="sxs-lookup"><span data-stu-id="8de90-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="8de90-177">4</span><span class="sxs-lookup"><span data-stu-id="8de90-177">4</span></span> | <span data-ttu-id="8de90-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="8de90-178">INT8, UINT8</span></span> |
| <span data-ttu-id="8de90-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8de90-179">OutputTensor</span></span> | <span data-ttu-id="8de90-180">Resultados</span><span class="sxs-lookup"><span data-stu-id="8de90-180">Output</span></span> | <span data-ttu-id="8de90-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="8de90-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="8de90-182">4</span><span class="sxs-lookup"><span data-stu-id="8de90-182">4</span></span> | <span data-ttu-id="8de90-183">INT32</span><span class="sxs-lookup"><span data-stu-id="8de90-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="8de90-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8de90-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8de90-185">**Header**</span><span class="sxs-lookup"><span data-stu-id="8de90-185">**Header**</span></span> | <span data-ttu-id="8de90-186">directml.h</span><span class="sxs-lookup"><span data-stu-id="8de90-186">directml.h</span></span> |