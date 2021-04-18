---
title: Método RemovePackageMethod de la clase MDM_EnterpriseModernAppManagement_AppManagement01
description: Método para quitar paquetes. Vea también RemovePackage.
ms.assetid: 0f48fd9c-5a3f-48e5-a954-e937e79af049
keywords:
- Método RemovePackageMethod
- Método RemovePackageMethod, clase MDM_EnterpriseModernAppManagement_AppManagement01
- Clase MDM_EnterpriseModernAppManagement_AppManagement01, método RemovePackageMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.RemovePackageMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2cdeb2c1a8dfaebdde73e52b2910da180b638c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658275"
---
# <a name="removepackagemethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="e31c5-107">Método RemovePackageMethod de la \_ \_ clase APPMANAGEMENT01 de MDM EnterpriseModernAppManagement</span><span class="sxs-lookup"><span data-stu-id="e31c5-107">RemovePackageMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="e31c5-108">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e31c5-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e31c5-109">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e31c5-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e31c5-110">Método para quitar paquetes.</span><span class="sxs-lookup"><span data-stu-id="e31c5-110">Method for removing packages.</span></span> <span data-ttu-id="e31c5-111">Vea también [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="e31c5-111">See also [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="e31c5-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e31c5-112">Syntax</span></span>


```mof
uint32 RemovePackageMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="e31c5-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e31c5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31c5-114">*parámetro* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e31c5-114">*param* \[in\]</span></span>
<span data-ttu-id="e31c5-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e31c5-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e31c5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e31c5-116">Requirements</span></span>



| <span data-ttu-id="e31c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e31c5-117">Requirement</span></span> | <span data-ttu-id="e31c5-118">Value</span><span class="sxs-lookup"><span data-stu-id="e31c5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31c5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e31c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e31c5-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e31c5-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e31c5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e31c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e31c5-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e31c5-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e31c5-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e31c5-123">Namespace</span></span><br/>                | <span data-ttu-id="e31c5-124">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e31c5-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e31c5-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e31c5-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e31c5-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e31c5-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e31c5-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e31c5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e31c5-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31c5-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31c5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e31c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31c5-130">**\_AppManagement01 ENTERPRISEMODERNAPPMANAGEMENT \_ MDM**</span><span class="sxs-lookup"><span data-stu-id="e31c5-130">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> </dl>

 

