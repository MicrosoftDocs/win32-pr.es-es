---
description: Función de proxy para el método GetEncoderInfo.
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: IWICBitmapEncoder_GetEncoderInfo_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 00764021542648c42fa9bf8213e799edb8b8fd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697856"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a><span data-ttu-id="04ade-103">IWICBitmapEncoder \_ GetEncoderInfo \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="04ade-103">IWICBitmapEncoder\_GetEncoderInfo\_Proxy function</span></span>

<span data-ttu-id="04ade-104">Función de proxy para el método [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="04ade-104">Proxy function for the [**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ade-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04ade-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="04ade-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04ade-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ade-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="04ade-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ade-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="04ade-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="04ade-109">Puntero a este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="04ade-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="04ade-110">*ppIEncoderInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="04ade-110">*ppIEncoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04ade-111">Tipo: **[ **IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="04ade-111">Type: **[**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***</span></span>

<span data-ttu-id="04ade-112">Puntero que recibe un puntero a un [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span><span class="sxs-lookup"><span data-stu-id="04ade-112">A pointer that receives a pointer to an [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ade-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04ade-113">Return value</span></span>

<span data-ttu-id="04ade-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="04ade-114">Type: **HRESULT**</span></span>

<span data-ttu-id="04ade-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="04ade-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04ade-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04ade-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ade-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04ade-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="04ade-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ade-118">Requirements</span></span>



| <span data-ttu-id="04ade-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ade-119">Requirement</span></span> | <span data-ttu-id="04ade-120">Value</span><span class="sxs-lookup"><span data-stu-id="04ade-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04ade-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ade-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04ade-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04ade-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="04ade-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ade-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04ade-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="04ade-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="04ade-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04ade-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04ade-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04ade-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




