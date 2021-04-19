---
description: Proporciona al sistema información sobre un documento antes de iniciar una operación abierta.
title: Función DlpNotifyPreOpenDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 557554ad55a3a520fa95fcf53c8044881eed8b21
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495852"
---
# <a name="dlpnotifypreopendocument-function"></a><span data-ttu-id="3473a-103">Función DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="3473a-103">DlpNotifyPreOpenDocument function</span></span>

<span data-ttu-id="3473a-104">Proporciona al sistema información sobre un documento antes de iniciar una operación abierta.</span><span class="sxs-lookup"><span data-stu-id="3473a-104">Provides the system with information about a document before an open operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3473a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3473a-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a><span data-ttu-id="3473a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3473a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3473a-107">*DocumentInfo* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3473a-107">*DocumentInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3473a-108">Puntero a [un](endpointdlp-dlp_document_info.md) PDLP_DOCUMENT_INFO estructura que contiene información sobre el documento que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="3473a-108">A pointer to a [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) structure containing information about the document to be opened.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="3473a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3473a-109">Return value</span></span>

<span data-ttu-id="3473a-110">Devuelve void.</span><span class="sxs-lookup"><span data-stu-id="3473a-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="3473a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3473a-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="3473a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3473a-112">Requirements</span></span>



| <span data-ttu-id="3473a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3473a-113">Requirement</span></span>          |    <span data-ttu-id="3473a-114">Value</span><span class="sxs-lookup"><span data-stu-id="3473a-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3473a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3473a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3473a-116">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="3473a-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="3473a-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3473a-117">DLL</span></span><br/>                      | <span data-ttu-id="3473a-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="3473a-118">EndpointDlp.dll</span></span> |