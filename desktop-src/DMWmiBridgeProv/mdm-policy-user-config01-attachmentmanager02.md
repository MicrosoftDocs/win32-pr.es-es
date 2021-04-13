---
title: MDM_Policy_User_Config01_AttachmentManager02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ AttachmentManager02 representa las directivas de administrador de archivos adjuntos disponibles.
ms.assetid: b20ec516-cdc9-4aeb-802d-97cd8423eceb
keywords:
- MDM_Policy_User_Config01_AttachmentManager02 (clase)
- MDM_Policy_User_Config01_AttachmentManager02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_AttachmentManager02
- MDM_Policy_User_Config01_AttachmentManager02.InstanceID
- MDM_Policy_User_Config01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d127fc3770f6ba605bd8e1efdd82314231ab27f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534816"
---
# <a name="mdm_policy_user_config01_attachmentmanager02-class"></a><span data-ttu-id="1e4e3-105">\_Clase AttachmentManager02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="1e4e3-105">MDM\_Policy\_User\_Config01\_AttachmentManager02 class</span></span>

<span data-ttu-id="1e4e3-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1e4e3-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="1e4e3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1e4e3-108">La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ AttachmentManager02 representa las directivas de administrador de archivos adjuntos disponibles.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-108">The MDM\_Policy\_User\_Config01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="1e4e3-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e4e3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e4e3-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="1e4e3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e4e3-111">Members</span></span>

<span data-ttu-id="1e4e3-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ AttachmentManager02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1e4e3-112">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="1e4e3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e4e3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e4e3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e4e3-114">Properties</span></span>

<span data-ttu-id="1e4e3-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ AttachmentManager02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-115">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1e4e3-116">DoNotPreserveZoneInformation</span><span class="sxs-lookup"><span data-stu-id="1e4e3-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e4e3-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e4e3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e4e3-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1e4e3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e4e3-119">HideZoneInfoMechanism</span><span class="sxs-lookup"><span data-stu-id="1e4e3-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e4e3-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e4e3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e4e3-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1e4e3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e4e3-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e4e3-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e4e3-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e4e3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e4e3-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e4e3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e4e3-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e4e3-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e4e3-126">NotifyAntivirusPrograms</span><span class="sxs-lookup"><span data-stu-id="1e4e3-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e4e3-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e4e3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e4e3-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1e4e3-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e4e3-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1e4e3-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e4e3-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e4e3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e4e3-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e4e3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e4e3-132">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e4e3-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e4e3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e4e3-133">Requirements</span></span>



| <span data-ttu-id="1e4e3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e4e3-134">Requirement</span></span> | <span data-ttu-id="1e4e3-135">Value</span><span class="sxs-lookup"><span data-stu-id="1e4e3-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4e3-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e4e3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1e4e3-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e4e3-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e4e3-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e4e3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1e4e3-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1e4e3-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1e4e3-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e4e3-140">Namespace</span></span><br/>                | <span data-ttu-id="1e4e3-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="1e4e3-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1e4e3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1e4e3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e4e3-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e4e3-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e4e3-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e4e3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e4e3-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e4e3-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

