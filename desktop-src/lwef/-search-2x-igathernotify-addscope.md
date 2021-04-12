---
title: IGatherNotify parámetro addscope (deprecated) (método)
description: Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API ISearchPersistentItemsChangedSink de Windows Search en el Windows SDK. | IGatherNotify parámetro addscope (deprecated) (método)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Parámetro addscope (obsoleto) características de entorno de Windows heredado
- Parámetro addscope (obsoleto) características de entorno heredado de Windows, interfaz IGatherNotify
- Interfaz IGatherNotify características del entorno heredado de Windows, parámetro addscope (en desuso) (método)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362201"
---
# <a name="igathernotifyaddscope-deprecated-method"></a><span data-ttu-id="24f46-107">IGatherNotify:: parámetro addscope (deprecated) (método)</span><span class="sxs-lookup"><span data-stu-id="24f46-107">IGatherNotify::AddScope (Deprecated) method</span></span>

<span data-ttu-id="24f46-108">\[**Parámetro addscope** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]</span><span class="sxs-lookup"><span data-stu-id="24f46-108">\[**AddScope** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="24f46-109">Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="24f46-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="24f46-110">Agrega la página de inicio o la dirección URL que está supervisando.</span><span class="sxs-lookup"><span data-stu-id="24f46-110">Adds the start page or URL you are monitoring.</span></span> <span data-ttu-id="24f46-111">Esto inicia un rastreo incremental al conectarse y, a continuación, asume que todos los cambios de dirección URL adicionales son por notificación.</span><span class="sxs-lookup"><span data-stu-id="24f46-111">This initiates an incremental crawl when you connect, and then assumes all further URL changes are by notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f46-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24f46-112">Syntax</span></span>


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a><span data-ttu-id="24f46-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24f46-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f46-114">*bstrScope* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24f46-114">*bstrScope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f46-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="24f46-115">Type: **BSTR**</span></span>

<span data-ttu-id="24f46-116">Una cadena que especifica la página de inicio o el URLthat que está supervisando.</span><span class="sxs-lookup"><span data-stu-id="24f46-116">A string that specifies the start page or URLthat you are monitoring.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f46-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24f46-117">Return value</span></span>

<span data-ttu-id="24f46-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="24f46-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24f46-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24f46-119">Remarks</span></span>

<span data-ttu-id="24f46-120">La llamada a este método inicia un rastreo incremental cuando se conecta al almacén.</span><span class="sxs-lookup"><span data-stu-id="24f46-120">Calling this method starts an incremental crawl when connected to the store.</span></span> <span data-ttu-id="24f46-121">A partir de ese momento, se supone que todos los cambios de dirección URL son por notificación después de la actualización inicial.</span><span class="sxs-lookup"><span data-stu-id="24f46-121">Thereafter, it is assumed that all URL changes are by notification after the initial update.</span></span>

 

 
