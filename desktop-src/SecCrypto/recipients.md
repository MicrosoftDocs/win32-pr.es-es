---
description: 'Objeto Recipients: representa una colección de objetos Certificate.'
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Objeto Recipients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0f0f6474c6ed8883eb591591eff387fe387f7d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103743"
---
# <a name="recipients-object"></a><span data-ttu-id="cb83c-103">Objeto Recipients</span><span class="sxs-lookup"><span data-stu-id="cb83c-103">Recipients object</span></span>

<span data-ttu-id="cb83c-104">\[El **objeto Recipients** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.</span><span class="sxs-lookup"><span data-stu-id="cb83c-104">\[The **Recipients** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cb83c-105">En su lugar, use [**la clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="cb83c-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="cb83c-106">El **objeto Recipients** representa una colección de [**objetos Certificate.**](certificate.md)</span><span class="sxs-lookup"><span data-stu-id="cb83c-106">The **Recipients** object represents a collection of [**Certificate**](certificate.md) objects.</span></span> <span data-ttu-id="cb83c-107">Cada objeto representa un destinatario previsto del mensaje con sobres.</span><span class="sxs-lookup"><span data-stu-id="cb83c-107">Each object represents an intended recipient of the enveloped message.</span></span> <span data-ttu-id="cb83c-108">Los datos de un objeto [**EnvelopedData**](envelopeddata.md) se cifran con una clave de sesión simétrica y, [*a*](../secgloss/s-gly.md) continuación, esa clave de sesión simétrica se cifra para cada destinatario mediante el uso de la clave pública del certificado de ese destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="cb83c-108">Data in an [**EnvelopedData**](envelopeddata.md) object is encrypted with a [*symmetric*](../secgloss/s-gly.md) session key, and that symmetric session key is then itself encrypted for each recipient by using the public key from that intended recipient's certificate.</span></span> <span data-ttu-id="cb83c-109">Un destinatario con acceso a la clave [](../secgloss/p-gly.md) privada asociada a [](../secgloss/s-gly.md) la clave pública de un certificado puede descifrar la clave de sesión y usar la clave de sesión descifrada para descifrar los datos reales. [](../secgloss/p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="cb83c-109">A recipient with access to the [*private key*](../secgloss/p-gly.md) associated with a certificate's [*public key*](../secgloss/p-gly.md) can decrypt the [*session key*](../secgloss/s-gly.md) and use the decrypted session key to decrypt the actual data.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cb83c-110">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="cb83c-110">When to use</span></span>

<span data-ttu-id="cb83c-111">El **objeto Recipients** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="cb83c-111">The **Recipients** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="cb83c-112">Agregue o quite un [**objeto Certificate**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-112">Add or remove a [**Certificate**](certificate.md) object from the collection.</span></span>
-   <span data-ttu-id="cb83c-113">Recupere el número de certificados de la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-113">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="cb83c-114">Recuperar un objeto **Recipients** específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-114">Retrieve a specific **Recipients** object from the collection.</span></span>
-   <span data-ttu-id="cb83c-115">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="cb83c-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb83c-116">Members</span></span>

<span data-ttu-id="cb83c-117">El **objeto Recipients** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cb83c-117">The **Recipients** object has these types of members:</span></span>

-   [<span data-ttu-id="cb83c-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb83c-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb83c-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb83c-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb83c-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb83c-120">Methods</span></span>

<span data-ttu-id="cb83c-121">El **objeto Recipients** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cb83c-121">The **Recipients** object has these methods.</span></span>



| <span data-ttu-id="cb83c-122">Método</span><span class="sxs-lookup"><span data-stu-id="cb83c-122">Method</span></span>                              | <span data-ttu-id="cb83c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb83c-123">Description</span></span>                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb83c-124">**Añadir**</span><span class="sxs-lookup"><span data-stu-id="cb83c-124">**Add**</span></span>](recipients-add.md)       | <span data-ttu-id="cb83c-125">Agrega un [**objeto Certificate**](certificate.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-125">Adds a [**Certificate**](certificate.md) object to the collection.</span></span><br/>         |
| [<span data-ttu-id="cb83c-126">**Borrar**</span><span class="sxs-lookup"><span data-stu-id="cb83c-126">**Clear**</span></span>](recipients-clear.md)   | <span data-ttu-id="cb83c-127">Quita todos los [**objetos Certificate**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-127">Removes all [**Certificate**](certificate.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="cb83c-128">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="cb83c-128">**Remove**</span></span>](recipients-remove.md) | <span data-ttu-id="cb83c-129">Quita un [**objeto Certificate**](certificate.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-129">Removes a [**Certificate**](certificate.md) object from the collection.</span></span><br/>    |



 

### <a name="properties"></a><span data-ttu-id="cb83c-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb83c-130">Properties</span></span>

<span data-ttu-id="cb83c-131">El **objeto Recipients** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb83c-131">The **Recipients** object has these properties.</span></span>



| <span data-ttu-id="cb83c-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb83c-132">Property</span></span>                                           | <span data-ttu-id="cb83c-133">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="cb83c-133">Access type</span></span>          | <span data-ttu-id="cb83c-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb83c-134">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb83c-135">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="cb83c-135">**\_NewEnum**</span></span>](recipients-newenum.md)<br/> | <span data-ttu-id="cb83c-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb83c-136">Read-only</span></span><br/> | <span data-ttu-id="cb83c-137">Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-137">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="cb83c-138">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="cb83c-138">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="cb83c-139">**Contar**</span><span class="sxs-lookup"><span data-stu-id="cb83c-139">**Count**</span></span>](recipients-count.md)<br/>       |                      | <span data-ttu-id="cb83c-140">Número de objetos de la **colección Recipients.**</span><span class="sxs-lookup"><span data-stu-id="cb83c-140">The number of objects in the **Recipients** collection.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="cb83c-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cb83c-141">**Item**</span></span>](recipients-item.md)<br/>         |                      | <span data-ttu-id="cb83c-142">Objeto indexado de la colección.</span><span class="sxs-lookup"><span data-stu-id="cb83c-142">An indexed object in the collection.</span></span> <span data-ttu-id="cb83c-143">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cb83c-143">This is the default property.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="cb83c-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb83c-144">Remarks</span></span>

<span data-ttu-id="cb83c-145">No **se puede crear** el objeto Recipients.</span><span class="sxs-lookup"><span data-stu-id="cb83c-145">The **Recipients** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb83c-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb83c-146">Requirements</span></span>



| <span data-ttu-id="cb83c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb83c-147">Requirement</span></span> | <span data-ttu-id="cb83c-148">Valor</span><span class="sxs-lookup"><span data-stu-id="cb83c-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb83c-149">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="cb83c-149">Redistributable</span></span><br/> | <span data-ttu-id="cb83c-150">CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb83c-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cb83c-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb83c-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="cb83c-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb83c-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb83c-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cb83c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb83c-154">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="cb83c-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
