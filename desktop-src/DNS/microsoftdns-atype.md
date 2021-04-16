---
title: MicrosoftDNS_AType (clase)
description: Subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de dirección de host (a).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- DNS de la clase MicrosoftDNS_AType
- MicrosoftDNS_AType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656537"
---
# <a name="microsoftdns_atype-class"></a><span data-ttu-id="3302d-105">MicrosoftDNS ( \_ clase AType)</span><span class="sxs-lookup"><span data-stu-id="3302d-105">MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="3302d-106">Subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de dirección de host (a).</span><span class="sxs-lookup"><span data-stu-id="3302d-106">Subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a host Address (A) record.</span></span>

<span data-ttu-id="3302d-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="3302d-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3302d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3302d-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a><span data-ttu-id="3302d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3302d-109">Members</span></span>

<span data-ttu-id="3302d-110">La clase **MicrosoftDNS \_ AType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3302d-110">The **MicrosoftDNS\_AType** class has these types of members:</span></span>

-   [<span data-ttu-id="3302d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3302d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3302d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3302d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3302d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3302d-113">Methods</span></span>

<span data-ttu-id="3302d-114">La clase **MicrosoftDNS \_ AType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3302d-114">The **MicrosoftDNS\_AType** class has these methods.</span></span>



| <span data-ttu-id="3302d-115">Método</span><span class="sxs-lookup"><span data-stu-id="3302d-115">Method</span></span>                             | <span data-ttu-id="3302d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3302d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3302d-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="3302d-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="3302d-118">Crea una instancia de un RR de dirección de host (A) basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la dirección IP del host.</span><span class="sxs-lookup"><span data-stu-id="3302d-118">Instantiates a Host Address (A) RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value and the IP address of the host.</span></span> <span data-ttu-id="3302d-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="3302d-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="3302d-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="3302d-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="3302d-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="3302d-121">**Modify**</span></span>                         | <span data-ttu-id="3302d-122">Actualiza el TTL y la dirección IP a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="3302d-122">Updates the TTL and IP address to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="3302d-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="3302d-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="3302d-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="3302d-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="3302d-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="3302d-125">Qualifiers: Implemented</span></span><br/>             |



 

### <a name="properties"></a><span data-ttu-id="3302d-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3302d-126">Properties</span></span>

<span data-ttu-id="3302d-127">La clase **MicrosoftDNS \_ AType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3302d-127">The **MicrosoftDNS\_AType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3302d-128">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="3302d-128">**IPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3302d-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3302d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3302d-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3302d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3302d-131">Cadena que representa la dirección IPv4 del host.</span><span class="sxs-lookup"><span data-stu-id="3302d-131">String representing the IPv4 address of the host.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3302d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3302d-132">Requirements</span></span>



| <span data-ttu-id="3302d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3302d-133">Requirement</span></span> | <span data-ttu-id="3302d-134">Value</span><span class="sxs-lookup"><span data-stu-id="3302d-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3302d-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3302d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3302d-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3302d-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3302d-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3302d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3302d-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3302d-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3302d-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3302d-139">Namespace</span></span><br/>                | <span data-ttu-id="3302d-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="3302d-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3302d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3302d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3302d-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3302d-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3302d-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3302d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3302d-144">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="3302d-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="3302d-145">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AType**</span><span class="sxs-lookup"><span data-stu-id="3302d-145">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="3302d-146">**Método Modify de la \_ clase MicrosoftDNS AType**</span><span class="sxs-lookup"><span data-stu-id="3302d-146">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





