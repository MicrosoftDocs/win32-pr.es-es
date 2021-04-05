---
title: Método SetName de la clase Win32_TSGatewayRADIUSServer
description: Establece la propiedad de nombre de este servidor Servicio de autenticación remota telefónica de usuario (RADIUS).
ms.assetid: 2dabc6fb-7740-4039-9bbd-5b2490fe5988
ms.tgt_platform: multiple
keywords:
- SetName (método) Servicios de Escritorio remoto
- Método SetName Servicios de Escritorio remoto, clase Win32_TSGatewayRADIUSServer
- Clase Win32_TSGatewayRADIUSServer Servicios de Escritorio remoto, método SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4b563c59ce1546b4cf471653407e3390676625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802263"
---
# <a name="setname-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="0afd8-106">Método SetName de la \_ clase TSGatewayRADIUSServer de Win32</span><span class="sxs-lookup"><span data-stu-id="0afd8-106">SetName method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="0afd8-107">Establece la propiedad de **nombre** de este servidor servicio de autenticación remota telefónica de usuario (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="0afd8-107">Sets the **Name** property for this Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0afd8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0afd8-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="0afd8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0afd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afd8-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0afd8-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afd8-111">Nuevo nombre.</span><span class="sxs-lookup"><span data-stu-id="0afd8-111">New name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0afd8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0afd8-112">Return value</span></span>

<span data-ttu-id="0afd8-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="0afd8-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0afd8-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0afd8-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0afd8-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0afd8-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0afd8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0afd8-116">Remarks</span></span>

<span data-ttu-id="0afd8-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="0afd8-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0afd8-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0afd8-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0afd8-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0afd8-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0afd8-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="0afd8-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0afd8-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0afd8-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0afd8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0afd8-122">Requirements</span></span>



| <span data-ttu-id="0afd8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0afd8-123">Requirement</span></span> | <span data-ttu-id="0afd8-124">Value</span><span class="sxs-lookup"><span data-stu-id="0afd8-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0afd8-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0afd8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0afd8-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0afd8-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0afd8-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0afd8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0afd8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0afd8-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0afd8-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0afd8-129">Namespace</span></span><br/>                | <span data-ttu-id="0afd8-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0afd8-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0afd8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0afd8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0afd8-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0afd8-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0afd8-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0afd8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0afd8-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0afd8-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0afd8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0afd8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0afd8-136">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="0afd8-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

