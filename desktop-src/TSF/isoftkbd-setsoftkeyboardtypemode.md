---
title: Método ISoftKbd SetSoftKeyboardTypeMode (Softkbdc. h)
description: El método ISoftKbd SetSoftKeyboardTypeMode establece el modo de tipo para un teclado en pantalla.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Método SetSoftKeyboardTypeMode marco de trabajo de servicios de texto
- Método SetSoftKeyboardTypeMode marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492101"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a><span data-ttu-id="2c78c-106">ISoftKbd:: SetSoftKeyboardTypeMode (método)</span><span class="sxs-lookup"><span data-stu-id="2c78c-106">ISoftKbd::SetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="2c78c-107">El método **ISoftKbd:: SetSoftKeyboardTypeMode** establece el modo de tipo para un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="2c78c-107">The **ISoftKbd::SetSoftKeyboardTypeMode** method sets the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c78c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c78c-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="2c78c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2c78c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c78c-110">*TypeMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2c78c-110">*TypeMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c78c-111">Modo de tipo.</span><span class="sxs-lookup"><span data-stu-id="2c78c-111">The type mode.</span></span> <span data-ttu-id="2c78c-112">Se definen los valores posibles para la enumeración [**TYPEMODE**](typemode.md) .</span><span class="sxs-lookup"><span data-stu-id="2c78c-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c78c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c78c-113">Return value</span></span>

<span data-ttu-id="2c78c-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2c78c-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2c78c-115">Value</span><span class="sxs-lookup"><span data-stu-id="2c78c-115">Value</span></span>                                                                                        | <span data-ttu-id="2c78c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c78c-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2c78c-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2c78c-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2c78c-118">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c78c-118">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="2c78c-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2c78c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2c78c-120">El parámetro *TypeMode* no es válido.</span><span class="sxs-lookup"><span data-stu-id="2c78c-120">The *TypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2c78c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c78c-121">Requirements</span></span>



| <span data-ttu-id="2c78c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c78c-122">Requirement</span></span> | <span data-ttu-id="2c78c-123">Value</span><span class="sxs-lookup"><span data-stu-id="2c78c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c78c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c78c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2c78c-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2c78c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2c78c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c78c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2c78c-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c78c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2c78c-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2c78c-128">Redistributable</span></span><br/>          | <span data-ttu-id="2c78c-129">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2c78c-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="2c78c-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2c78c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c78c-131"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c78c-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="2c78c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="2c78c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c78c-133"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c78c-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="2c78c-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c78c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c78c-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c78c-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c78c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c78c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c78c-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="2c78c-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="2c78c-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="2c78c-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="2c78c-139">**TYPEMODE**</span><span class="sxs-lookup"><span data-stu-id="2c78c-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





