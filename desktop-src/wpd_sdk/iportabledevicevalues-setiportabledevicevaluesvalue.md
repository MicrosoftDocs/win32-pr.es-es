---
description: El método SetIPortableDeviceValuesValue agrega un nuevo valor de IPortableDeviceValues (tipo VT \_ desconocido) o sobrescribe uno existente.
ms.assetid: 3e51964e-6ee0-4885-94ca-cc8000b456b4
title: 'IPortableDeviceValues:: SetIPortableDeviceValuesValue (método) (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 265a5d3633dfa8252ff7afd4042a41e476040d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708691"
---
# <a name="iportabledevicevaluessetiportabledevicevaluesvalue-method"></a><span data-ttu-id="3e58c-103">IPortableDeviceValues:: SetIPortableDeviceValuesValue (método)</span><span class="sxs-lookup"><span data-stu-id="3e58c-103">IPortableDeviceValues::SetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="3e58c-104">El método **SetIPortableDeviceValuesValue** agrega un nuevo valor de **IPORTABLEDEVICEVALUES** (tipo VT \_ desconocido) o sobrescribe uno existente.</span><span class="sxs-lookup"><span data-stu-id="3e58c-104">The **SetIPortableDeviceValuesValue** method adds a new **IPortableDeviceValues** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e58c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e58c-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesValue(
  [in] REFPROPERTYKEY        key,
  [in] IPortableDeviceValues *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3e58c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e58c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e58c-107">*clave* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3e58c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e58c-108">**REFPROPERTYKEY** que especifica el elemento que se va a crear o sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="3e58c-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="3e58c-109">*pValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e58c-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e58c-110">Puntero a una interfaz **IPortableDeviceValues** que especifica el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="3e58c-110">Pointer to an **IPortableDeviceValues** interface that specifies the new value.</span></span> <span data-ttu-id="3e58c-111">El SDK copia una referencia a la interfaz enviada y llama a **AddRef** en ella.</span><span class="sxs-lookup"><span data-stu-id="3e58c-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e58c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e58c-112">Return value</span></span>

<span data-ttu-id="3e58c-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3e58c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3e58c-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="3e58c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3e58c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e58c-115">Return code</span></span>                                                                          | <span data-ttu-id="3e58c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e58c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3e58c-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3e58c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3e58c-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="3e58c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e58c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e58c-119">Remarks</span></span>

<span data-ttu-id="3e58c-120">Si un valor existente tiene la misma clave que especifica el parámetro de *clave* , sobrescribe el valor existente sin ninguna advertencia.</span><span class="sxs-lookup"><span data-stu-id="3e58c-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="3e58c-121">La memoria de clave existente se libera adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="3e58c-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e58c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e58c-122">Requirements</span></span>



| <span data-ttu-id="3e58c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e58c-123">Requirement</span></span> | <span data-ttu-id="3e58c-124">Value</span><span class="sxs-lookup"><span data-stu-id="3e58c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e58c-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e58c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3e58c-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e58c-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e58c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e58c-127">Library</span></span><br/> | <dl> <span data-ttu-id="3e58c-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e58c-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e58c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e58c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e58c-130">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3e58c-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3e58c-131">**IPortableDeviceValues::GetIPortableDeviceValuesValue**</span><span class="sxs-lookup"><span data-stu-id="3e58c-131">**IPortableDeviceValues::GetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-getiportabledevicevaluesvalue.md)
</dt> </dl>

 

 




