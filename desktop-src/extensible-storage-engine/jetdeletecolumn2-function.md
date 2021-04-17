---
description: 'Más información acerca de: JetDeleteColumn2 (función)'
title: JetDeleteColumn2 función)
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35e19eb7ac7b133bb690b268426fec9822efefea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717236"
---
# <a name="jetdeletecolumn2-function"></a><span data-ttu-id="cc28f-103">JetDeleteColumn2 función)</span><span class="sxs-lookup"><span data-stu-id="cc28f-103">JetDeleteColumn2 Function</span></span>


<span data-ttu-id="cc28f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cc28f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletecolumn2-function"></a><span data-ttu-id="cc28f-105">JetDeleteColumn2 función)</span><span class="sxs-lookup"><span data-stu-id="cc28f-105">JetDeleteColumn2 Function</span></span>

<span data-ttu-id="cc28f-106">La función **JetDeleteColumn2** elimina una columna de una tabla de base de datos ese y permite establecer una opción *grbit* .</span><span class="sxs-lookup"><span data-stu-id="cc28f-106">The **JetDeleteColumn2** function deletes a column from an ESE database table and enables a *grbit* option to be set.</span></span>

<span data-ttu-id="cc28f-107">**Windows XP: JetDeleteColumn2** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc28f-107">**Windows XP:  JetDeleteColumn2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="cc28f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc28f-108">Parameters</span></span>

<span data-ttu-id="cc28f-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="cc28f-109">*sesid*</span></span>

<span data-ttu-id="cc28f-110">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="cc28f-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="cc28f-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="cc28f-111">*tableid*</span></span>

<span data-ttu-id="cc28f-112">Tabla que contiene la columna que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="cc28f-112">The table that contains the column to be deleted.</span></span>

<span data-ttu-id="cc28f-113">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="cc28f-113">*szColumnName*</span></span>

<span data-ttu-id="cc28f-114">Nombre de la columna que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="cc28f-114">The name of the column to be deleted.</span></span>

<span data-ttu-id="cc28f-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="cc28f-115">*grbit*</span></span>

<span data-ttu-id="cc28f-116">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc28f-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc28f-117">Value</span><span class="sxs-lookup"><span data-stu-id="cc28f-117">Value</span></span></p></th>
<th><p><span data-ttu-id="cc28f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cc28f-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc28f-119">JET_bitDeleteColumnIgnoreTemplateColumns</span><span class="sxs-lookup"><span data-stu-id="cc28f-119">JET_bitDeleteColumnIgnoreTemplateColumns</span></span></p></td>
<td><p><span data-ttu-id="cc28f-120">La configuración de JET_bitDeleteColumIgnoreTemplateColumns hará que la API solo intente eliminar columnas de la tabla derivada.</span><span class="sxs-lookup"><span data-stu-id="cc28f-120">Setting JET_bitDeleteColumIgnoreTemplateColumns will cause the API to only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="cc28f-121">Si existe una columna con ese nombre en la tabla base, se omitirá.</span><span class="sxs-lookup"><span data-stu-id="cc28f-121">If a column of that name exists in the base table it will be ignored.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="cc28f-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc28f-122">Return Value</span></span>

<span data-ttu-id="cc28f-123">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="cc28f-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cc28f-124">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cc28f-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc28f-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cc28f-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="cc28f-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc28f-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc28f-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cc28f-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cc28f-128">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc28f-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc28f-129">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="cc28f-129">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="cc28f-130">La columna está en uso actualmente.</span><span class="sxs-lookup"><span data-stu-id="cc28f-130">The column is currently in use.</span></span> <span data-ttu-id="cc28f-131">Es posible que un índice lo esté usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="cc28f-131">It may be currently used by an index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc28f-132">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="cc28f-132">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="cc28f-133">Se intentó modificar el DDL fijo.</span><span class="sxs-lookup"><span data-stu-id="cc28f-133">An attempt was made to modify the fixed DDL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc28f-134">JET_errFixedInheritedDDL</span><span class="sxs-lookup"><span data-stu-id="cc28f-134">JET_errFixedInheritedDDL</span></span></p></td>
<td><p><span data-ttu-id="cc28f-135">La columna denominada en <em>szColumnName</em> existe en la tabla de plantilla y el DDL de una tabla de plantilla no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="cc28f-135">The column named in <em>szColumnName</em> exists in the template table, and the DDL of a template table cannot be modified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc28f-136">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="cc28f-136">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="cc28f-137">Se puede devolver si se proporcionó un nombre incorrecto para <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="cc28f-137">This may be returned if a bad name for <em>szColumnName</em> was given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc28f-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="cc28f-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="cc28f-139">No se puede escribir en la tabla.</span><span class="sxs-lookup"><span data-stu-id="cc28f-139">The table is not writable.</span></span> <span data-ttu-id="cc28f-140">Esto puede devolverse si la base de datos se abrió en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc28f-140">This may get returned if the database was opened in read-only mode.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc28f-141">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="cc28f-141">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="cc28f-142">La transacción es una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc28f-142">The transaction is a read-only transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="cc28f-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc28f-143">Remarks</span></span>

<span data-ttu-id="cc28f-144">Llamar a [JetDeleteColumn](./jetdeletecolumn-function.md) es idéntico a llamar a **JetDeleteColumn2** con *grbit* establecido en cero (0).</span><span class="sxs-lookup"><span data-stu-id="cc28f-144">Calling [JetDeleteColumn](./jetdeletecolumn-function.md) is identical to calling **JetDeleteColumn2** with *grbit* set to zero (0).</span></span>

#### <a name="requirements"></a><span data-ttu-id="cc28f-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc28f-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc28f-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="cc28f-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc28f-147">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc28f-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc28f-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cc28f-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc28f-149">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cc28f-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc28f-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cc28f-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc28f-151">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="cc28f-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc28f-152"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="cc28f-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cc28f-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cc28f-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc28f-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cc28f-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cc28f-155">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cc28f-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc28f-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cc28f-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cc28f-157">Se implementa como <strong>JetDeleteColumn2W</strong> (Unicode) y <strong>JetDeleteColumn2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cc28f-157">Implemented as <strong>JetDeleteColumn2W</strong> (Unicode) and <strong>JetDeleteColumn2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cc28f-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cc28f-158">See Also</span></span>

[<span data-ttu-id="cc28f-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cc28f-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cc28f-160">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cc28f-160">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cc28f-161">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cc28f-161">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cc28f-162">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cc28f-162">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cc28f-163">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="cc28f-163">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)
