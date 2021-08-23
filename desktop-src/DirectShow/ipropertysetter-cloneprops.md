---
description: El método CloneProps clona un conjunto de propiedades de este establecedor de propiedades y las agrega a un nuevo establecedor de propiedades.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: Método IPropertySetter::CloneProps (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54dd2ad08334a0c61918de74396e62fcc21e095df81c2d773995b6cfbdddc19d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755925"
---
# <a name="ipropertysettercloneprops-method"></a>IPropertySetter::CloneProps (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método clona un conjunto de propiedades de este establecedor de propiedades y `CloneProps` las agrega a un nuevo establecedor de propiedades.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSetter* \[ out\]
</dt> <dd>

Recibe un puntero a la **interfaz IPropertySetter** del nuevo setter de propiedad.

</dd> <dt>

*rtStart* \[ En\]
</dt> <dd>

Hora de inicio del intervalo de valores que se va a clonar, en unidades de 100 nanosegundos.

</dd> <dt>

*rtStop* \[ En\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Solo se clonan los valores que se encuentran después de la hora de inicio especificada. A continuación, las horas de los valores clonados se ajustan en relación con la hora de inicio. Por ejemplo, si *rtStart* es 20000000 (2 segundos), se clona un valor en el momento 30000000 (3 segundos) con el tiempo 10000000 (1 segundo). Por último, a cada propiedad clonada se le proporciona un valor inicial igual al valor de la propiedad original en la hora de inicio (interpolado correctamente si es necesario). De hecho, los datos de propiedad se dividen en la hora de inicio especificada.

Si el método se realiza correctamente, la [**interfaz IPropertySetter**](ipropertysetter.md) que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPropertySetter (interfaz)**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




