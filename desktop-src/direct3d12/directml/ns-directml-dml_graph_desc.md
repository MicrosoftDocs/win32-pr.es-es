---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Describe un gráfico de operadores directML usados para compilar un operador optimizado combinado.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418046"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="33e98-103">DML_GRAPH_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="33e98-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="33e98-104">Describe un gráfico de operadores directML usados para compilar un operador optimizado combinado.</span><span class="sxs-lookup"><span data-stu-id="33e98-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="33e98-105">Vea [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="33e98-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33e98-106">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="33e98-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="33e98-107">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="33e98-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="33e98-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33e98-108">Syntax</span></span>
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a><span data-ttu-id="33e98-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="33e98-109">Members</span></span>

`InputCount`

<span data-ttu-id="33e98-110">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="33e98-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="33e98-111">Número de entradas del gráfico general.</span><span class="sxs-lookup"><span data-stu-id="33e98-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="33e98-112">Cada entrada de grafo puede estar conectada a un número variable de nodos internos, por lo que puede ser diferente de *InputEdgeCount.*</span><span class="sxs-lookup"><span data-stu-id="33e98-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="33e98-113">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="33e98-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="33e98-114">Número de salidas del gráfico general.</span><span class="sxs-lookup"><span data-stu-id="33e98-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="33e98-115">Cada salida de grafo puede estar conectada a un número variable de nodos internos, por lo que puede ser diferente de *OutputEdgeCount.*</span><span class="sxs-lookup"><span data-stu-id="33e98-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="33e98-116">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="33e98-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="33e98-117">Número de nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="33e98-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="33e98-118">Tipo: \_ Tamaño de campo \_ \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="33e98-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="33e98-119">Nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="33e98-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="33e98-120">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="33e98-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="33e98-121">Número de conexiones entre las entradas del grafo y las entradas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="33e98-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="33e98-122">Tipo: \_ Tamaño de campo \_ \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="33e98-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="33e98-123">Matriz de conexiones entre las entradas del grafo y las entradas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="33e98-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="33e98-124">El *campo Type* dentro de cada elemento debe establecerse en [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="33e98-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="33e98-125">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="33e98-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="33e98-126">Número de conexiones entre las salidas del grafo y las salidas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="33e98-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="33e98-127">Tipo: \_ Tamaño de campo \_ \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="33e98-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="33e98-128">Matriz de conexiones entre las salidas del grafo y las salidas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="33e98-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="33e98-129">El *campo Type* dentro de cada elemento debe establecerse en [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="33e98-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="33e98-130">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="33e98-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="33e98-131">Número de conexiones internas entre nodos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="33e98-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="33e98-132">Tipo: \_ Tamaño de campo \_ \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="33e98-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="33e98-133">Matriz de conexiones entre las entradas y salidas de los nodos internos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="33e98-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="33e98-134">El campo Type dentro de cada elemento debe establecerse [en DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="33e98-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="33e98-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="33e98-135">Remarks</span></span>
<span data-ttu-id="33e98-136">El gráfico descrito por esta estructura debe ser un grafo acíclico dirigido.</span><span class="sxs-lookup"><span data-stu-id="33e98-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="33e98-137">Debe definir una conexión para la entrada y salida de cada nodo proporcionado, excepto las entradas y salidas que son opcionales para el operador asociado.</span><span class="sxs-lookup"><span data-stu-id="33e98-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="33e98-138">Los nodos pueden usar operadores que se crearon [mediante la DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) para determinadas entradas.</span><span class="sxs-lookup"><span data-stu-id="33e98-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="33e98-139">Todas las entradas de operador que usan esta marca deben estar conectadas a entradas de grafo.</span><span class="sxs-lookup"><span data-stu-id="33e98-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="33e98-140">Todas las entradas de operador conectadas a la misma entrada de grafo deben usar u omitir esta marca de forma equivalente.</span><span class="sxs-lookup"><span data-stu-id="33e98-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="33e98-141">Es legal conectar operadores cuyas entradas y salidas conectadas usan diferentes recuentos de dimensiones, tamaños y tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="33e98-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="33e98-142">Esto implica que cada operador interpreta de forma diferente el blob de datos tensor.</span><span class="sxs-lookup"><span data-stu-id="33e98-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="33e98-143">Sin embargo, el campo *TotalTensorSizeInBytes* de entradas y salidas del tensor conectado debe ser idéntico.</span><span class="sxs-lookup"><span data-stu-id="33e98-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="33e98-144">Los operadores solo deben leer regiones de tensores escritas por operadores anteriores.</span><span class="sxs-lookup"><span data-stu-id="33e98-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="33e98-145">No se garantiza que los operadores de flujo inferior lean como cero las regiones de relleno de la salida de una operación (resultante del uso de strides).</span><span class="sxs-lookup"><span data-stu-id="33e98-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="33e98-146">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="33e98-146">Availability</span></span>

<span data-ttu-id="33e98-147">Esta API se introdujo en la versión de `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="33e98-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="33e98-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33e98-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="33e98-149">**Header**</span><span class="sxs-lookup"><span data-stu-id="33e98-149">**Header**</span></span> | <span data-ttu-id="33e98-150">directml.h</span><span class="sxs-lookup"><span data-stu-id="33e98-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="33e98-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="33e98-151">See also</span></span>

* [<span data-ttu-id="33e98-152">Método IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="33e98-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="33e98-153">DML_GRAPH_NODE_DESC struct</span><span class="sxs-lookup"><span data-stu-id="33e98-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="33e98-154">DML_GRAPH_EDGE_DESC struct</span><span class="sxs-lookup"><span data-stu-id="33e98-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)