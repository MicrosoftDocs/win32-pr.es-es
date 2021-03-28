---
description: Obtiene el nombre del contenedor de cuentas del usuario.
title: Propiedad DIDiskQuotaUser. AccountContainerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808821"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="050e4-103">Propiedad DIDiskQuotaUser. AccountContainerName</span><span class="sxs-lookup"><span data-stu-id="050e4-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="050e4-104">Obtiene el nombre del contenedor de cuentas del usuario.</span><span class="sxs-lookup"><span data-stu-id="050e4-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="050e4-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="050e4-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="050e4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="050e4-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="050e4-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="050e4-107">Property value</span></span>

<span data-ttu-id="050e4-108">Valor de cadena que se establece en el nombre del contenedor de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="050e4-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="050e4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="050e4-109">Remarks</span></span>

<span data-ttu-id="050e4-110">En el caso de las cuentas sin información de servicios de directorio, esta propiedad contiene el nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="050e4-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="050e4-111">En el caso de las cuentas con información de servicios de directorio, esta propiedad contiene un nombre canónico con el nombre de objeto de terminación quitado.</span><span class="sxs-lookup"><span data-stu-id="050e4-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="050e4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="050e4-112">Requirements</span></span>



| <span data-ttu-id="050e4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="050e4-113">Requirement</span></span> | <span data-ttu-id="050e4-114">Value</span><span class="sxs-lookup"><span data-stu-id="050e4-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="050e4-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="050e4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="050e4-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="050e4-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="050e4-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="050e4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="050e4-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="050e4-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="050e4-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="050e4-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="050e4-120"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="050e4-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="050e4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="050e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050e4-122">**Objeto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="050e4-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




