---
description: Notifica al controlador cuando una aplicación de Microsoft DirectDraw está cambiando a o desde el modo exclusivo.
ms.assetid: f2b63d90-7ede-479f-a2fd-ae9870c4d7b9
title: Función NtGdiDdSetExclusiveMode (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetExclusiveMode
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1d2420f4ae093b4bfc3f68871daefd5c20da308e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659347"
---
# <a name="ntgdiddsetexclusivemode-function"></a><span data-ttu-id="18b0d-103">NtGdiDdSetExclusiveMode función)</span><span class="sxs-lookup"><span data-stu-id="18b0d-103">NtGdiDdSetExclusiveMode function</span></span>

<span data-ttu-id="18b0d-104">\[Esta función está sujeta a cambios en cada revisión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="18b0d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="18b0d-105">En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]</span><span class="sxs-lookup"><span data-stu-id="18b0d-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="18b0d-106">Notifica al controlador cuando una aplicación de Microsoft DirectDraw está cambiando a o desde el modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="18b0d-106">Notifies the driver when a Microsoft DirectDraw application is switching to or from exclusive mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b0d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18b0d-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetExclusiveMode(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_SETEXCLUSIVEMODEDATA puSetExclusiveModeData
);
```



## <a name="parameters"></a><span data-ttu-id="18b0d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18b0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b0d-109">*hDirectDraw* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18b0d-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b0d-110">Identificador del objeto DirectDraw en modo kernel creado previamente.</span><span class="sxs-lookup"><span data-stu-id="18b0d-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="18b0d-111">*puSetExclusiveModeData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="18b0d-111">*puSetExclusiveModeData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18b0d-112">Puntero a una estructura [**DD \_ SETEXCLUSIVEMODEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) que contiene la información de notificación.</span><span class="sxs-lookup"><span data-stu-id="18b0d-112">Pointer to a [**DD\_SETEXCLUSIVEMODEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b0d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18b0d-113">Return value</span></span>

<span data-ttu-id="18b0d-114">**NtGdiDdSetExclusiveMode** devuelve uno de los siguientes códigos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="18b0d-114">**NtGdiDdSetExclusiveMode** returns one of the following callback codes.</span></span>



| <span data-ttu-id="18b0d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="18b0d-115">Return code</span></span>                                                                                              | <span data-ttu-id="18b0d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="18b0d-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18b0d-117"><dt>**\_controlador DDHAL \_ controlado**</dt></span><span class="sxs-lookup"><span data-stu-id="18b0d-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="18b0d-118">El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación.</span><span class="sxs-lookup"><span data-stu-id="18b0d-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="18b0d-119">Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función.</span><span class="sxs-lookup"><span data-stu-id="18b0d-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="18b0d-120">De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.</span><span class="sxs-lookup"><span data-stu-id="18b0d-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="18b0d-121"><dt>**\_NOTHANDLED del controlador DDHAL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="18b0d-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="18b0d-122">El controlador no tiene ningún comentario en la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="18b0d-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="18b0d-123">Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="18b0d-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="18b0d-124">De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="18b0d-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18b0d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18b0d-125">Requirements</span></span>



| <span data-ttu-id="18b0d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="18b0d-126">Requirement</span></span> | <span data-ttu-id="18b0d-127">Value</span><span class="sxs-lookup"><span data-stu-id="18b0d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18b0d-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18b0d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="18b0d-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="18b0d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="18b0d-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18b0d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="18b0d-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18b0d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="18b0d-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18b0d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="18b0d-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="18b0d-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18b0d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="18b0d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b0d-135">Compatibilidad con clientes de nivel inferior de gráficos</span><span class="sxs-lookup"><span data-stu-id="18b0d-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
