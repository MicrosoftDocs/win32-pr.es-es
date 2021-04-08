---
description: Descomprime el archivo de método abreviado lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: e120391a-3839-4f8c-aca3-473d7f8b30bf
ms.tgt_platform: multiple
title: Método UNCOMPRESS de la clase Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48267f519dce9ae5d78581050255bd8e8b02222c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807856"
---
# <a name="uncompress-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="177c9-103">Método UNCOMPRESS de la \_ clase ShortcutFile de Win32</span><span class="sxs-lookup"><span data-stu-id="177c9-103">Uncompress method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="177c9-104">El método de clase **descomprimir** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) descomprime el archivo de método abreviado lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="177c9-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="177c9-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="177c9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="177c9-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="177c9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="177c9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="177c9-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="177c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="177c9-108">Parameters</span></span>

<span data-ttu-id="177c9-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="177c9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="177c9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="177c9-110">Return value</span></span>

<span data-ttu-id="177c9-111">Devuelve un valor de 0 (cero) si el archivo se ha descomprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="177c9-111">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="177c9-112">**0**</span><span class="sxs-lookup"><span data-stu-id="177c9-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-113">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="177c9-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-114">**2**</span><span class="sxs-lookup"><span data-stu-id="177c9-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-115">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="177c9-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-116">**8**</span><span class="sxs-lookup"><span data-stu-id="177c9-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-117">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="177c9-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-118">**9**</span><span class="sxs-lookup"><span data-stu-id="177c9-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-119">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="177c9-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-120">**10**</span><span class="sxs-lookup"><span data-stu-id="177c9-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-121">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="177c9-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-122">**11**</span><span class="sxs-lookup"><span data-stu-id="177c9-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-123">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="177c9-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-124">**12**</span><span class="sxs-lookup"><span data-stu-id="177c9-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-125">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="177c9-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-126">**13**</span><span class="sxs-lookup"><span data-stu-id="177c9-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-127">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="177c9-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-128">**14**</span><span class="sxs-lookup"><span data-stu-id="177c9-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-129">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="177c9-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-130">**15**</span><span class="sxs-lookup"><span data-stu-id="177c9-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-131">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="177c9-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-132">**16**</span><span class="sxs-lookup"><span data-stu-id="177c9-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-133">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="177c9-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-134">**17**</span><span class="sxs-lookup"><span data-stu-id="177c9-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-135">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="177c9-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="177c9-136">**21**</span><span class="sxs-lookup"><span data-stu-id="177c9-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="177c9-137">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="177c9-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="177c9-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="177c9-138">Requirements</span></span>



| <span data-ttu-id="177c9-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="177c9-139">Requirement</span></span> | <span data-ttu-id="177c9-140">Value</span><span class="sxs-lookup"><span data-stu-id="177c9-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="177c9-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="177c9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="177c9-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="177c9-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="177c9-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="177c9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="177c9-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="177c9-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="177c9-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="177c9-145">Namespace</span></span><br/>                | <span data-ttu-id="177c9-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="177c9-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="177c9-147">MOF</span><span class="sxs-lookup"><span data-stu-id="177c9-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="177c9-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="177c9-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="177c9-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="177c9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="177c9-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="177c9-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177c9-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="177c9-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="177c9-152">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="177c9-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="177c9-153">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="177c9-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

