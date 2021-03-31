---
title: Método CreateInstanceFromPropertyData de la clase MicrosoftDNS_HINFOType
description: El método CreateInstanceFromPropertyData crea una instancia de un registro de recursos de información de host (HINFO).
ms.assetid: dfc11ae8-5013-4b48-a1e9-78566dc32297
keywords:
- CreateInstanceFromPropertyData el método DNS
- Método CreateInstanceFromPropertyData DNS, clase MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType de clase DNS, método CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2c8386a9c66ec94436fe4ae4c886ec62ff5b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803518"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="d0e73-106">Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS HINFOType</span><span class="sxs-lookup"><span data-stu-id="d0e73-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="d0e73-107">El método **CreateInstanceFromPropertyData** crea una instancia de un registro de recursos de información de host (HINFO).</span><span class="sxs-lookup"><span data-stu-id="d0e73-107">The **CreateInstanceFromPropertyData** method instantiates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e73-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0e73-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d0e73-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0e73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e73-110">*DnsServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0e73-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e73-111">FQDN o dirección IP del servidor DNS que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="d0e73-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d0e73-112">*ContainerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0e73-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e73-113">Nombre del contenedor de la zona, la memoria caché o la instancia de RootHints que contiene este RR.</span><span class="sxs-lookup"><span data-stu-id="d0e73-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d0e73-114">*Nombrepropietario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0e73-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e73-115">Nombre del propietario del RR.</span><span class="sxs-lookup"><span data-stu-id="d0e73-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="d0e73-116">*RecordClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d0e73-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e73-117">Clase del RR.</span><span class="sxs-lookup"><span data-stu-id="d0e73-117">Class of the RR.</span></span> <span data-ttu-id="d0e73-118">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="d0e73-118">Default value is 1.</span></span> <span data-ttu-id="d0e73-119">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="d0e73-119">The following values are valid.</span></span>



| <span data-ttu-id="d0e73-120">Value</span><span class="sxs-lookup"><span data-stu-id="d0e73-120">Value</span></span>                                                                                                | <span data-ttu-id="d0e73-121">Significado</span><span class="sxs-lookup"><span data-stu-id="d0e73-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d0e73-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d0e73-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d0e73-123">EN (Internet)</span><span class="sxs-lookup"><span data-stu-id="d0e73-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="d0e73-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d0e73-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d0e73-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="d0e73-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="d0e73-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d0e73-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d0e73-127">CH (CAOS)</span><span class="sxs-lookup"><span data-stu-id="d0e73-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="d0e73-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d0e73-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d0e73-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="d0e73-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="d0e73-130">*TTL* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d0e73-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e73-131">Tiempo, en segundos, que un solucionador DNS puede almacenar en caché el RR.</span><span class="sxs-lookup"><span data-stu-id="d0e73-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d0e73-132">*CPU* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d0e73-132">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e73-133">Tipo de CPU del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="d0e73-133">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="d0e73-134">*Sistema operativo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d0e73-134">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e73-135">Sistema operativo del propietario del registro.</span><span class="sxs-lookup"><span data-stu-id="d0e73-135">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="d0e73-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="d0e73-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e73-137">Referencia al nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="d0e73-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e73-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0e73-138">Return value</span></span>

<span data-ttu-id="d0e73-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d0e73-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e73-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0e73-140">Requirements</span></span>



| <span data-ttu-id="d0e73-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e73-141">Requirement</span></span> | <span data-ttu-id="d0e73-142">Value</span><span class="sxs-lookup"><span data-stu-id="d0e73-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e73-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0e73-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e73-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d0e73-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d0e73-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0e73-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e73-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0e73-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d0e73-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d0e73-147">Namespace</span></span><br/>                | <span data-ttu-id="d0e73-148">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="d0e73-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d0e73-149">MOF</span><span class="sxs-lookup"><span data-stu-id="d0e73-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0e73-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0e73-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e73-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0e73-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e73-152">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="d0e73-152">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="d0e73-153">**Método Modify de la \_ clase MicrosoftDNS HINFOType**</span><span class="sxs-lookup"><span data-stu-id="d0e73-153">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="d0e73-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d0e73-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





