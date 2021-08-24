---
description: Proporciona la capacidad de devolver una lista filtrada de instancias \_ de BaseMetricValue de CIM.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Método GetMetricValues de la CIM_MetricService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d010128bdef9bec4ce7df5fb3b1021a80a6ac99bdfbaf797958a76b27a812479
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695005"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a>Método GetMetricValues de la clase \_ MetricService de CIM

Proporciona la capacidad de devolver una lista filtrada de [**instancias \_ de BaseMetricValue**](cim-basemetricvalue.md) de CIM.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Definición* \[ En\]
</dt> <dd>

Identifica una [**\_ baseMetricDefinition CIM**](cim-basemetricdefinition.md) para la que se devolverán las métricas.

</dd> <dt>

*Intervalo* \[ En\]
</dt> <dd>

Identifica cómo se seleccionan las instancias. El algoritmo para ordenar instancias de valor es específico de la definición de métrica.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Mínimo** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Máximo** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico del** proveedor (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Identifica el número máximo de instancias que va a devolver el método .

</dd> <dt>

*Valores* \[ out\]
</dt> <dd>

Tras la finalización correcta del método , contiene referencias a instancias de [**\_ CIM BaseMetricValue**](cim-basemetricvalue.md), filtradas según los valores de los parámetros de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Método reservado** (..)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




