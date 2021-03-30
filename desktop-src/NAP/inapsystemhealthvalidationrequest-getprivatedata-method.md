---
title: Método INapSystemHealthValidationRequest GetPrivateData (NapSystemHealthValidator. h)
description: Permite que NapServer recupere información de estado.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- Método GetPrivateData NAP
- Método GetPrivateData NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método GetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803661"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a><span data-ttu-id="d3c50-106">INapSystemHealthValidationRequest:: GetPrivateData (método)</span><span class="sxs-lookup"><span data-stu-id="d3c50-106">INapSystemHealthValidationRequest::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="d3c50-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d3c50-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d3c50-108">El método **INapSystemHealthValidationRequest:: GetPrivateData** permite a NapServer recuperar información de estado.</span><span class="sxs-lookup"><span data-stu-id="d3c50-108">The **INapSystemHealthValidationRequest::GetPrivateData** method allows the NapServer to retrieve state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c50-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3c50-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="d3c50-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3c50-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c50-111">*privateData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d3c50-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c50-112">Un puntero a un puntero a un BLOB de datos opacos [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que contiene información de estado.</span><span class="sxs-lookup"><span data-stu-id="d3c50-112">A pointer to a pointer to [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that contains state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c50-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3c50-113">Return value</span></span>

<span data-ttu-id="d3c50-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="d3c50-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d3c50-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d3c50-115">Return code</span></span>                                                                                     | <span data-ttu-id="d3c50-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3c50-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3c50-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="d3c50-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d3c50-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d3c50-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d3c50-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d3c50-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d3c50-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d3c50-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d3c50-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d3c50-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d3c50-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="d3c50-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3c50-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3c50-123">Remarks</span></span>

<span data-ttu-id="d3c50-124">Solo NapServer puede interpretar el BLOB de datos.</span><span class="sxs-lookup"><span data-stu-id="d3c50-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c50-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3c50-125">Requirements</span></span>



| <span data-ttu-id="d3c50-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c50-126">Requirement</span></span> | <span data-ttu-id="d3c50-127">Value</span><span class="sxs-lookup"><span data-stu-id="d3c50-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c50-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3c50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c50-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d3c50-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="d3c50-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3c50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c50-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3c50-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3c50-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3c50-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3c50-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3c50-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3c50-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d3c50-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3c50-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3c50-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="d3c50-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3c50-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c50-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c50-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="d3c50-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3c50-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c50-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="d3c50-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





