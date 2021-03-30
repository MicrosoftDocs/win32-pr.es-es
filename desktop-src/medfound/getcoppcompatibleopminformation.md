---
description: Envía una solicitud de estado del Protocolo de protección de la salida (COPP) a un objeto de salida protegido.
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: GetCOPPCompatibleOPMInformation función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275114"
---
# <a name="getcoppcompatibleopminformation-function"></a><span data-ttu-id="878ca-103">GetCOPPCompatibleOPMInformation función)</span><span class="sxs-lookup"><span data-stu-id="878ca-103">GetCOPPCompatibleOPMInformation function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="878ca-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="878ca-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="878ca-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="878ca-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="878ca-106">Envía una solicitud de estado del Protocolo de protección de la salida (COPP) a un objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="878ca-106">Sends a Certified Output Protection Protocol (COPP) status request to a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="878ca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="878ca-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a><span data-ttu-id="878ca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="878ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="878ca-109">*opoOPMProtectedOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="878ca-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="878ca-110">Identificador del objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="878ca-110">A handle to the protected output object.</span></span> <span data-ttu-id="878ca-111">Este identificador se obtiene llamando a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="878ca-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="878ca-112">*pParameters* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="878ca-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="878ca-113">Un puntero a una estructura de **\_ \_ \_ \_ \_ \_ parámetros GET info compatible de DXGKMDT OPM** que contiene los datos de entrada para la solicitud de estado.</span><span class="sxs-lookup"><span data-stu-id="878ca-113">A pointer to a **DXGKMDT\_OPM\_COPP\_COMPATIBLE\_GET\_INFO\_PARAMETERS** structure that contains input data for the status request.</span></span>

</dd> <dt>

<span data-ttu-id="878ca-114">*pRequestedInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="878ca-114">*pRequestedInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="878ca-115">Un puntero a una estructura de **información de DXGKMDT \_ OPM \_ solicitada \_** que recibe los resultados de la solicitud de estado.</span><span class="sxs-lookup"><span data-stu-id="878ca-115">A pointer to a **DXGKMDT\_OPM\_REQUESTED\_INFORMATION** structure that receives the results of the status request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="878ca-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="878ca-116">Return value</span></span>

<span data-ttu-id="878ca-117">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="878ca-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="878ca-118">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="878ca-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="878ca-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="878ca-119">Remarks</span></span>

<span data-ttu-id="878ca-120">Las aplicaciones deben llamar a [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="878ca-120">Applications should call [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) instead of calling this function.</span></span>

<span data-ttu-id="878ca-121">El objeto de salida protegido se debe crear con la semántica de COPP.</span><span class="sxs-lookup"><span data-stu-id="878ca-121">The protected output object must be created with COPP semantics.</span></span> <span data-ttu-id="878ca-122">Vea [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="878ca-122">See [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

<span data-ttu-id="878ca-123">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="878ca-123">This function has no associated import library.</span></span> <span data-ttu-id="878ca-124">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="878ca-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="878ca-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="878ca-125">Requirements</span></span>



| <span data-ttu-id="878ca-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="878ca-126">Requirement</span></span> | <span data-ttu-id="878ca-127">Value</span><span class="sxs-lookup"><span data-stu-id="878ca-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="878ca-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="878ca-128">Minimum supported client</span></span><br/> | <span data-ttu-id="878ca-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="878ca-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="878ca-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="878ca-130">Minimum supported server</span></span><br/> | <span data-ttu-id="878ca-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="878ca-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="878ca-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="878ca-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="878ca-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="878ca-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="878ca-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="878ca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="878ca-135">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="878ca-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="878ca-136">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="878ca-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
