---
title: Método DisableSerialPorts de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad SerialPortsDisabled.
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- Método DisableSerialPorts Servicios de Escritorio remoto
- Método DisableSerialPorts Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método DisableSerialPorts
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a4f6941f8bc98d7f8e424a984922ad1f6631c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801460"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="77f4b-106">Método DisableSerialPorts de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="77f4b-106">DisableSerialPorts method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="77f4b-107">Establece la propiedad **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="77f4b-107">Sets the **SerialPortsDisabled** property.</span></span> <span data-ttu-id="77f4b-108">Si la propiedad **DeviceRedirectionType** tiene un valor de "2", la propiedad **SerialPortsDisabled** controla la redirección de los puertos serie para las sesiones que se establecen a través del servidor de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="77f4b-108">If the **DeviceRedirectionType** property has a value of "2", the **SerialPortsDisabled** property controls redirection of the serial ports for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f4b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77f4b-109">Syntax</span></span>


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="77f4b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77f4b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f4b-111">*Deshabilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77f4b-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77f4b-112">Nuevo valor para la propiedad **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="77f4b-112">New value for the **SerialPortsDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77f4b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77f4b-113">Return value</span></span>

<span data-ttu-id="77f4b-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="77f4b-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="77f4b-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="77f4b-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="77f4b-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="77f4b-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77f4b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77f4b-117">Remarks</span></span>

<span data-ttu-id="77f4b-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="77f4b-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="77f4b-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="77f4b-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="77f4b-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="77f4b-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="77f4b-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="77f4b-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="77f4b-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="77f4b-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="77f4b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77f4b-123">Requirements</span></span>



| <span data-ttu-id="77f4b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f4b-124">Requirement</span></span> | <span data-ttu-id="77f4b-125">Value</span><span class="sxs-lookup"><span data-stu-id="77f4b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f4b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77f4b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="77f4b-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="77f4b-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="77f4b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77f4b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="77f4b-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77f4b-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="77f4b-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="77f4b-130">Namespace</span></span><br/>                | <span data-ttu-id="77f4b-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="77f4b-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="77f4b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="77f4b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77f4b-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77f4b-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="77f4b-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77f4b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77f4b-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77f4b-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="77f4b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="77f4b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f4b-137">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="77f4b-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

