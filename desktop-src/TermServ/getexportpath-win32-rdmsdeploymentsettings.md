---
title: Método GetExportPath de la clase Win32_RDMSDeploymentSettings
description: Recupera la ruta de acceso al directorio en el que se implementan las máquinas virtuales para una colección de escritorios virtuales.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Método GetExportPath Servicios de Escritorio remoto
- Método GetExportPath Servicios de Escritorio remoto, clase Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de clase Servicios de Escritorio remoto, método GetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676604"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="f8e77-106">Método GetExportPath de la \_ clase RDMSDeploymentSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="f8e77-106">GetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="f8e77-107">Recupera la ruta de acceso al directorio en el que se implementan las máquinas virtuales para una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="f8e77-107">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e77-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8e77-108">Syntax</span></span>


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="f8e77-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8e77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8e77-110">*DirectoryPath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8e77-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8e77-111">Recibe la ruta de acceso del directorio.</span><span class="sxs-lookup"><span data-stu-id="f8e77-111">Receives the directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8e77-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8e77-112">Return value</span></span>

<span data-ttu-id="f8e77-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f8e77-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e77-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8e77-114">Requirements</span></span>



| <span data-ttu-id="f8e77-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8e77-115">Requirement</span></span> | <span data-ttu-id="f8e77-116">Value</span><span class="sxs-lookup"><span data-stu-id="f8e77-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e77-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8e77-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e77-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f8e77-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f8e77-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8e77-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e77-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f8e77-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f8e77-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8e77-121">Namespace</span></span><br/>                | <span data-ttu-id="f8e77-122">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="f8e77-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f8e77-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f8e77-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8e77-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8e77-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8e77-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8e77-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8e77-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8e77-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f8e77-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8e77-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8e77-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="f8e77-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





