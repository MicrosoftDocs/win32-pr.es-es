---
title: Método RemoveComputerGroupNames de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Quita los nombres de grupo de equipos especificados de la propiedad ComputerGroupNames.
ms.assetid: 5f4e566a-1a2e-459d-ab6c-53ffd42271d8
ms.tgt_platform: multiple
keywords:
- Método RemoveComputerGroupNames Servicios de Escritorio remoto
- Método RemoveComputerGroupNames Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método RemoveComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ec281798fba0257883eebfb60ac199b0f3c1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079147"
---
# <a name="removecomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="af240-106">Método RemoveComputerGroupNames de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="af240-106">RemoveComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="af240-107">Quita los nombres de grupo de equipos especificados de la propiedad **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="af240-107">Removes specified computer group names from the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="af240-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af240-108">Syntax</span></span>


```mof
uint32 RemoveComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="af240-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af240-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af240-110">*ComputerGroupNames* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="af240-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af240-111">Lista separada por puntos y comas de nombres de grupos de equipos que se van a quitar de la propiedad **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="af240-111">Semicolon-separated list of computer group names to remove from the **ComputerGroupNames** property.</span></span> <span data-ttu-id="af240-112">Los nombres de los grupos de equipos deben tener el formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="af240-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af240-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af240-113">Return value</span></span>

<span data-ttu-id="af240-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="af240-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="af240-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="af240-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="af240-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="af240-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af240-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af240-117">Remarks</span></span>

<span data-ttu-id="af240-118">Si hay varios nombres de grupos de equipos en el parámetro *ComputerGroupNames* y uno de los nombres no se puede procesar, no se procesará ninguno de los nombres.</span><span class="sxs-lookup"><span data-stu-id="af240-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="af240-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="af240-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="af240-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="af240-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="af240-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="af240-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="af240-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="af240-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="af240-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="af240-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="af240-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af240-124">Requirements</span></span>



| <span data-ttu-id="af240-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="af240-125">Requirement</span></span> | <span data-ttu-id="af240-126">Value</span><span class="sxs-lookup"><span data-stu-id="af240-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af240-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af240-127">Minimum supported client</span></span><br/> | <span data-ttu-id="af240-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="af240-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="af240-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af240-129">Minimum supported server</span></span><br/> | <span data-ttu-id="af240-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af240-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="af240-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="af240-131">Namespace</span></span><br/>                | <span data-ttu-id="af240-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="af240-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="af240-133">MOF</span><span class="sxs-lookup"><span data-stu-id="af240-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af240-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af240-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="af240-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af240-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af240-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af240-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="af240-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="af240-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af240-138">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="af240-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

