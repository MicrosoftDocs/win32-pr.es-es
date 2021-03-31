---
title: Propiedad MaximizeShell de IMsRdpClientAdvancedSettings
description: Especifica si se deben maximizar los programas iniciados con la propiedad StartProgram.
ms.assetid: d8c194b6-04ef-495f-a763-7e18064230e6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MaximizeShell
- Propiedad MaximizeShell Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad MaximizeShell
- Propiedad MaximizeShell Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad MaximizeShell
- Propiedad MaximizeShell Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad MaximizeShell
- Propiedad MaximizeShell Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad MaximizeShell
- Propiedad MaximizeShell Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad MaximizeShell
- Propiedad MaximizeShell Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad MaximizeShell
- Propiedad MaximizeShell Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad MaximizeShell
- Propiedad MaximizeShell Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad MaximizeShell
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MaximizeShell
- IMsRdpClientAdvancedSettings.get_MaximizeShell
- IMsRdpClientAdvancedSettings.put_MaximizeShell
- IMsRdpClientAdvancedSettings2.MaximizeShell
- IMsRdpClientAdvancedSettings2.get_MaximizeShell
- IMsRdpClientAdvancedSettings2.put_MaximizeShell
- IMsRdpClientAdvancedSettings3.MaximizeShell
- IMsRdpClientAdvancedSettings3.get_MaximizeShell
- IMsRdpClientAdvancedSettings3.put_MaximizeShell
- IMsRdpClientAdvancedSettings4.MaximizeShell
- IMsRdpClientAdvancedSettings4.get_MaximizeShell
- IMsRdpClientAdvancedSettings4.put_MaximizeShell
- IMsRdpClientAdvancedSettings5.MaximizeShell
- IMsRdpClientAdvancedSettings5.get_MaximizeShell
- IMsRdpClientAdvancedSettings5.put_MaximizeShell
- IMsRdpClientAdvancedSettings6.MaximizeShell
- IMsRdpClientAdvancedSettings6.get_MaximizeShell
- IMsRdpClientAdvancedSettings6.put_MaximizeShell
- IMsRdpClientAdvancedSettings7.MaximizeShell
- IMsRdpClientAdvancedSettings7.get_MaximizeShell
- IMsRdpClientAdvancedSettings7.put_MaximizeShell
- IMsRdpClientAdvancedSettings8.MaximizeShell
- IMsRdpClientAdvancedSettings8.get_MaximizeShell
- IMsRdpClientAdvancedSettings8.put_MaximizeShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c172dd71fcf57f2028f6ba64c93ceaeec2ffb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996145"
---
# <a name="imsrdpclientadvancedsettingsmaximizeshell-property"></a><span data-ttu-id="9816f-120">IMsRdpClientAdvancedSettings:: MaximizeShell (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9816f-120">IMsRdpClientAdvancedSettings::MaximizeShell property</span></span>

<span data-ttu-id="9816f-121">Especifica si se deben maximizar los programas iniciados con la propiedad [**StartProgram**](imstscsecuredsettings-startprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="9816f-121">Specifies if programs launched with the [**StartProgram**](imstscsecuredsettings-startprogram.md) property should be maximized.</span></span>

<span data-ttu-id="9816f-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9816f-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9816f-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9816f-123">Syntax</span></span>


```C++
HRESULT put_MaximizeShell(
  [in]  LONG maximizeShell
);

HRESULT get_MaximizeShell(
  [out] LONG *pmaximizeShell
);
```



## <a name="property-value"></a><span data-ttu-id="9816f-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9816f-124">Property value</span></span>

<span data-ttu-id="9816f-125">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="9816f-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9816f-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9816f-126">Error codes</span></span>

<span data-ttu-id="9816f-127">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="9816f-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9816f-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9816f-128">Remarks</span></span>

<span data-ttu-id="9816f-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9816f-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9816f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9816f-130">Requirements</span></span>



| <span data-ttu-id="9816f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9816f-131">Requirement</span></span> | <span data-ttu-id="9816f-132">Value</span><span class="sxs-lookup"><span data-stu-id="9816f-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9816f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9816f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9816f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9816f-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="9816f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9816f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9816f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9816f-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="9816f-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9816f-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="9816f-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9816f-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9816f-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9816f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9816f-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9816f-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9816f-141">IID</span><span class="sxs-lookup"><span data-stu-id="9816f-141">IID</span></span><br/>                      | <span data-ttu-id="9816f-142">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9816f-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9816f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="9816f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9816f-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9816f-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9816f-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9816f-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9816f-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9816f-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9816f-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9816f-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9816f-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9816f-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9816f-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9816f-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9816f-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9816f-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9816f-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9816f-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





