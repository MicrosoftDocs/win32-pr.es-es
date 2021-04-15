---
description: 'Más información sobre: método API. JetGetDatabaseInfo (JET_SESID, JET_DBID, cadena, JET_DbInfo)'
title: Método API. JetGetDatabaseInfo (JET_SESID, JET_DBID, cadena, JET_DbInfo)
TOCTitle: JetGetDatabaseInfo method (JET_SESID, JET_DBID, String, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabaseinfo(v=EXCHG.10)
ms:contentKeyID: 55100714
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d07ce09ac97a59936a47103067b32f348ed2ff56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677316"
---
# <a name="apijetgetdatabaseinfo-method-jet_sesid-jet_dbid-string-jet_dbinfo"></a><span data-ttu-id="afe16-103">Método API. JetGetDatabaseInfo (JET_SESID, JET_DBID, cadena, JET_DbInfo)</span><span class="sxs-lookup"><span data-stu-id="afe16-103">Api.JetGetDatabaseInfo method (JET_SESID, JET_DBID, String, JET_DbInfo)</span></span>

<span data-ttu-id="afe16-104">Recupera cierta información sobre la base de datos dada.</span><span class="sxs-lookup"><span data-stu-id="afe16-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="afe16-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afe16-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afe16-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="afe16-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afe16-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afe16-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef value As String, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim value As String
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseInfo(sesid, dbid, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out string value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="afe16-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afe16-108">Parameters</span></span>

  - <span data-ttu-id="afe16-109">sesid</span><span class="sxs-lookup"><span data-stu-id="afe16-109">sesid</span></span>  
    <span data-ttu-id="afe16-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="afe16-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="afe16-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="afe16-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="afe16-112">dbid</span><span class="sxs-lookup"><span data-stu-id="afe16-112">dbid</span></span>  
    <span data-ttu-id="afe16-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="afe16-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="afe16-114">Identificador de base de datos.</span><span class="sxs-lookup"><span data-stu-id="afe16-114">The database identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="afe16-115">value</span><span class="sxs-lookup"><span data-stu-id="afe16-115">value</span></span>  
    <span data-ttu-id="afe16-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="afe16-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="afe16-117">Valor que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="afe16-117">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="afe16-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="afe16-118">infoLevel</span></span>  
    <span data-ttu-id="afe16-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="afe16-119">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="afe16-120">Datos específicos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="afe16-120">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="afe16-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="afe16-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afe16-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="afe16-122">Reference</span></span>

[<span data-ttu-id="afe16-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="afe16-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="afe16-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="afe16-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="afe16-125">Sobrecarga JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="afe16-125">JetGetDatabaseInfo overload</span></span>](./api.jetgetdatabaseinfo-method.md)

[<span data-ttu-id="afe16-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="afe16-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
