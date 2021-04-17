---
description: 'Más información sobre: método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)'
title: Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100811
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd320c42e1d24c0919010706ae3f7e61a65b78a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707402"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string"></a><span data-ttu-id="30ab7-103">Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)</span><span class="sxs-lookup"><span data-stu-id="30ab7-103">Api.JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String)</span></span>

<span data-ttu-id="30ab7-104">Establece las opciones de configuración de base de datos.</span><span class="sxs-lookup"><span data-stu-id="30ab7-104">Sets database configuration options.</span></span>

<span data-ttu-id="30ab7-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="30ab7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="30ab7-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="30ab7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="30ab7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30ab7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As Integer, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    int paramValue,
    string paramString
)
```

#### <a name="parameters"></a><span data-ttu-id="30ab7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30ab7-108">Parameters</span></span>

  - <span data-ttu-id="30ab7-109">instance</span><span class="sxs-lookup"><span data-stu-id="30ab7-109">instance</span></span>  
    <span data-ttu-id="30ab7-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="30ab7-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="30ab7-111">Instancia en la que se va a establecer la opción o [Nil](./jet-instance.nil-property.md) para establecer la opción en todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="30ab7-111">The instance to set the option on or [Nil](./jet-instance.nil-property.md) to set the option on all instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="30ab7-112">sesid</span><span class="sxs-lookup"><span data-stu-id="30ab7-112">sesid</span></span>  
    <span data-ttu-id="30ab7-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="30ab7-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="30ab7-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="30ab7-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="30ab7-115">paramid</span><span class="sxs-lookup"><span data-stu-id="30ab7-115">paramid</span></span>  
    <span data-ttu-id="30ab7-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="30ab7-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="30ab7-117">Parámetro que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="30ab7-117">The parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="30ab7-118">Parámetro ParamValue</span><span class="sxs-lookup"><span data-stu-id="30ab7-118">paramValue</span></span>  
    <span data-ttu-id="30ab7-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="30ab7-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="30ab7-120">Valor del parámetro que se va a establecer, si el parámetro es un tipo entero.</span><span class="sxs-lookup"><span data-stu-id="30ab7-120">The value of the parameter to set, if the parameter is an integer type.</span></span>

<!-- end list -->

  - <span data-ttu-id="30ab7-121">paramString</span><span class="sxs-lookup"><span data-stu-id="30ab7-121">paramString</span></span>  
    <span data-ttu-id="30ab7-122">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="30ab7-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="30ab7-123">Valor del parámetro que se va a establecer, si el parámetro es un tipo de cadena.</span><span class="sxs-lookup"><span data-stu-id="30ab7-123">The value of the parameter to set, if the parameter is a string type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="30ab7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30ab7-124">Return value</span></span>

<span data-ttu-id="30ab7-125">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="30ab7-125">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="30ab7-126">Código de advertencia de ESENT.</span><span class="sxs-lookup"><span data-stu-id="30ab7-126">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="30ab7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="30ab7-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="30ab7-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="30ab7-128">Reference</span></span>

[<span data-ttu-id="30ab7-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="30ab7-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="30ab7-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="30ab7-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="30ab7-131">Sobrecarga JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="30ab7-131">JetSetSystemParameter overload</span></span>](./api.jetsetsystemparameter-method.md)

[<span data-ttu-id="30ab7-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="30ab7-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
