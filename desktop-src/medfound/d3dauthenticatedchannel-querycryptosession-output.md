---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION.
ms.assetid: df9d9b41-8188-4597-9e83-d14065eb7fc7
title: D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fb4e6ccad999f183e71f0f57d64544a70cef5534
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696153"
---
# <a name="d3dauthenticatedchannel_querycryptosession_output-structure"></a><span data-ttu-id="a2bff-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_</span><span class="sxs-lookup"><span data-stu-id="a2bff-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT structure</span></span>

<span data-ttu-id="a2bff-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="a2bff-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="a2bff-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="a2bff-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2bff-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2bff-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DXVA2DecodeHandle;
  HANDLE                               CryptoSessionHandle;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="a2bff-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2bff-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2bff-108">**Salida**</span><span class="sxs-lookup"><span data-stu-id="a2bff-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="a2bff-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="a2bff-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="a2bff-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="a2bff-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a2bff-111">Identificador de un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="a2bff-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="a2bff-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="a2bff-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a2bff-113">Identificador de la sesión criptográfica que está asociada con el dispositivo descodificador.</span><span class="sxs-lookup"><span data-stu-id="a2bff-113">A handle to the cryptographic session that is associated with the decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="a2bff-114">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="a2bff-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="a2bff-115">Identificador del dispositivo Direct3D que está asociado con el dispositivo descodificador.</span><span class="sxs-lookup"><span data-stu-id="a2bff-115">A handle to the Direct3D device that is associated with the decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2bff-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2bff-116">Requirements</span></span>



| <span data-ttu-id="a2bff-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2bff-117">Requirement</span></span> | <span data-ttu-id="a2bff-118">Value</span><span class="sxs-lookup"><span data-stu-id="a2bff-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2bff-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2bff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2bff-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2bff-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2bff-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2bff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2bff-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2bff-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a2bff-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2bff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2bff-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2bff-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2bff-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2bff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2bff-126">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a2bff-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="a2bff-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a2bff-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




