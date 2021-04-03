---
title: IBasicDevice FriendlyName (método)
description: Recupera el nombre descriptivo del dispositivo.
ms.assetid: 693806E1-CA66-457D-A25B-D79064776965
keywords:
- FriendlyName (método) API de streaming de multimedia
- FriendlyName Method API de streaming de media, interfaz IBasicDevice
- IBasicDevice interface media streaming API, FriendlyName (método)
topic_type:
- apiref
api_name:
- IBasicDevice.FriendlyName
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec2b2edfa3a98dfdbbdd1d236acb6e1f1433f141
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784102"
---
# <a name="ibasicdevicefriendlyname-method"></a><span data-ttu-id="380ea-106">IBasicDevice:: FriendlyName (método)</span><span class="sxs-lookup"><span data-stu-id="380ea-106">IBasicDevice::FriendlyName method</span></span>

<span data-ttu-id="380ea-107">Recupera el nombre descriptivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380ea-107">Retrieves the device s friendly name.</span></span>

## <a name="syntax"></a><span data-ttu-id="380ea-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="380ea-108">Syntax</span></span>


```C++
HRESULT FriendlyName(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="380ea-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="380ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380ea-110">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="380ea-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="380ea-111">Recibe un puntero al nombre descriptivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="380ea-111">Receives a pointer to the device s friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380ea-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="380ea-112">Return value</span></span>

<span data-ttu-id="380ea-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="380ea-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="380ea-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="380ea-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="380ea-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="380ea-115">Return code</span></span>                                                                          | <span data-ttu-id="380ea-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="380ea-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="380ea-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="380ea-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="380ea-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="380ea-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="380ea-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="380ea-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380ea-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="380ea-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





