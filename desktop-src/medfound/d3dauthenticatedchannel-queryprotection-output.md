---
description: Contiene la respuesta a una consulta de protección de D3DAUTHENTICATEDQUERY \_ .
ms.assetid: eb99089a-5e8e-4970-9c40-7f6a9662b5ec
title: D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: d68cafdf545d93a290e90c54be134977e51de4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539604"
---
# <a name="d3dauthenticatedchannel_queryprotection_output-structure"></a><span data-ttu-id="dff2f-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_</span><span class="sxs-lookup"><span data-stu-id="dff2f-103">D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT structure</span></span>

<span data-ttu-id="dff2f-104">Contiene la respuesta a una consulta de [**\_ protección de D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="dff2f-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_PROTECTION**](d3dauthenticatedquery-protection.md) query.</span></span>

<span data-ttu-id="dff2f-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="dff2f-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="dff2f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dff2f-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT     Output;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS ProtectionFlags;
} D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="dff2f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dff2f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="dff2f-108">**Salida**</span><span class="sxs-lookup"><span data-stu-id="dff2f-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="dff2f-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="dff2f-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="dff2f-110">**ProtectionFlags**</span><span class="sxs-lookup"><span data-stu-id="dff2f-110">**ProtectionFlags**</span></span>
</dt> <dd>

<span data-ttu-id="dff2f-111">Una estructura de [**\_ \_ marcas de protección de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) que especifica el nivel de protección.</span><span class="sxs-lookup"><span data-stu-id="dff2f-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dff2f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dff2f-112">Requirements</span></span>



| <span data-ttu-id="dff2f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dff2f-113">Requirement</span></span> | <span data-ttu-id="dff2f-114">Value</span><span class="sxs-lookup"><span data-stu-id="dff2f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dff2f-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dff2f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dff2f-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="dff2f-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dff2f-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dff2f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dff2f-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dff2f-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dff2f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dff2f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff2f-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff2f-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dff2f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="dff2f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff2f-122">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="dff2f-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="dff2f-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="dff2f-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




