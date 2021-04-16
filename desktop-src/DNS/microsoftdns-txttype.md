---
title: MicrosoftDNS_TXTType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de texto (txt).
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- DNS de la clase MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658349"
---
# <a name="microsoftdns_txttype-class"></a><span data-ttu-id="6f74c-105">MicrosoftDNS ( \_ clase TXTType)</span><span class="sxs-lookup"><span data-stu-id="6f74c-105">MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="6f74c-106">La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de texto (txt).</span><span class="sxs-lookup"><span data-stu-id="6f74c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Text (TXT) record.</span></span>

<span data-ttu-id="6f74c-107">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="6f74c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f74c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f74c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a><span data-ttu-id="6f74c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f74c-109">Members</span></span>

<span data-ttu-id="6f74c-110">La clase **MicrosoftDNS \_ TXTType** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6f74c-110">The **MicrosoftDNS\_TXTType** class has these types of members:</span></span>

-   [<span data-ttu-id="6f74c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f74c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f74c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f74c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f74c-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f74c-113">Methods</span></span>

<span data-ttu-id="6f74c-114">La clase **MicrosoftDNS \_ TXTType** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6f74c-114">The **MicrosoftDNS\_TXTType** class has these methods.</span></span>



| <span data-ttu-id="6f74c-115">Método</span><span class="sxs-lookup"><span data-stu-id="6f74c-115">Method</span></span>                             | <span data-ttu-id="6f74c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f74c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f74c-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6f74c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="6f74c-118">Crea una instancia de un tipo TXT de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el texto del registro.</span><span class="sxs-lookup"><span data-stu-id="6f74c-118">Instantiates a TXT Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and the record's text.</span></span> <span data-ttu-id="6f74c-119">Devuelve una referencia al nuevo objeto como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="6f74c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="6f74c-120">Calificadores: implementados, estáticos</span><span class="sxs-lookup"><span data-stu-id="6f74c-120">Qualifiers: Implemented, static</span></span><br/>        |
| <span data-ttu-id="6f74c-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="6f74c-121">**Modify**</span></span>                         | <span data-ttu-id="6f74c-122">Actualiza el TTL y el texto descriptivo a los valores especificados como parámetros de entrada de este método.</span><span class="sxs-lookup"><span data-stu-id="6f74c-122">Updates the TTL and Descriptive Text to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="6f74c-123">Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro.</span><span class="sxs-lookup"><span data-stu-id="6f74c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="6f74c-124">El método devuelve una referencia al objeto modificado como parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="6f74c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="6f74c-125">Calificadores: implementados</span><span class="sxs-lookup"><span data-stu-id="6f74c-125">Qualifiers: Implemented</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6f74c-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f74c-126">Properties</span></span>

<span data-ttu-id="6f74c-127">La clase **MicrosoftDNS \_ TXTType** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6f74c-127">The **MicrosoftDNS\_TXTType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f74c-128">**DescriptiveText**</span><span class="sxs-lookup"><span data-stu-id="6f74c-128">**DescriptiveText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f74c-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f74c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f74c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f74c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f74c-131">Texto descriptivo, la semántica de que depende del dominio del propietario.</span><span class="sxs-lookup"><span data-stu-id="6f74c-131">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f74c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f74c-132">Requirements</span></span>



| <span data-ttu-id="6f74c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f74c-133">Requirement</span></span> | <span data-ttu-id="6f74c-134">Value</span><span class="sxs-lookup"><span data-stu-id="6f74c-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f74c-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f74c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6f74c-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6f74c-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6f74c-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f74c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6f74c-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f74c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f74c-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f74c-139">Namespace</span></span><br/>                | <span data-ttu-id="6f74c-140">\\MicrosoftDNS raíz</span><span class="sxs-lookup"><span data-stu-id="6f74c-140">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6f74c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="6f74c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f74c-142"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f74c-142"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f74c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f74c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f74c-144">**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS TXTType**</span><span class="sxs-lookup"><span data-stu-id="6f74c-144">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6f74c-145">**Método Modify de la \_ clase MicrosoftDNS TXTType**</span><span class="sxs-lookup"><span data-stu-id="6f74c-145">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="6f74c-146">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6f74c-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





