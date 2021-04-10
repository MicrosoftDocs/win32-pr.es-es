---
title: IMediaRendererActionInformation IsStopAvailable, método
description: Recupera un valor que indica si el DMR está aceptando actualmente el método StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- Método IsStopAvailable API de streaming de multimedia
- Método IsStopAvailable API de streaming de multimedia, interfaz IMediaRendererActionInformation
- Interfaz IMediaRendererActionInformation API de streaming de multimedia, método IsStopAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149244"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a><span data-ttu-id="d621a-106">IMediaRendererActionInformation:: IsStopAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="d621a-106">IMediaRendererActionInformation::IsStopAvailable method</span></span>

<span data-ttu-id="d621a-107">Recupera un valor que indica si el DMR está aceptando actualmente el método [**StopAsync**](imediarenderer-stopasync.md) .</span><span class="sxs-lookup"><span data-stu-id="d621a-107">Retrieves a value that indicates whether the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d621a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d621a-108">Syntax</span></span>


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="d621a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d621a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d621a-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d621a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d621a-111">Valor booleano que es **true** si el DMR está aceptando actualmente el método [**StopAsync**](imediarenderer-stopasync.md) y **false** si no lo está.</span><span class="sxs-lookup"><span data-stu-id="d621a-111">A boolean value that is **True** if the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d621a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d621a-112">Return value</span></span>

<span data-ttu-id="d621a-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d621a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d621a-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="d621a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d621a-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d621a-115">Return code</span></span>                                                                          | <span data-ttu-id="d621a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d621a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d621a-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d621a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d621a-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="d621a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d621a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d621a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d621a-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="d621a-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

