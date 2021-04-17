---
description: El método SourceListAddSource agrega una red o un origen de dirección URL. Acepta SourcePath, el tipo y el índice como parámetros. Este método llama a MsiSourceListAddSourceEx.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Product. SourceListAddSource (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e0cfda9b8eab0e7dd00afd15eb701a6e7decf2ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653482"
---
# <a name="productsourcelistaddsource-method"></a>Product. SourceListAddSource (método)

El método **SourceListAddSource** agrega una red o un origen de dirección URL. Acepta *SourcePath*, el *tipo* y el *Índice* como parámetros. Este método llama a [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).

## <a name="syntax"></a>Sintaxis


```JScript
Product.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo de origen que se va a agregar: MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Ruta de acceso al origen que se va a agregar.

</dd> <dt>

*Index* 
</dt> <dd>

Si se llama a **SourceListAddSource** con un nuevo origen y el *Índice* se establece en 0, el instalador agrega el origen al final de la lista de origen.

Si se llama a esta función con un origen que ya existe en la lista de origen y el *Índice* se establece en 0, el instalador conserva el índice existente del origen.

Si se llama a la función con un origen existente en la lista de origen y el *Índice* se establece en un valor distinto de cero, el origen se quita de su ubicación actual en la lista y se inserta en la posición especificada por el *Índice*, antes de cualquier origen que ya exista en esa posición.

Si se llama a la función con un nuevo origen y el *Índice* se establece en un valor distinto de cero, el origen se inserta en la posición especificada por el *Índice*, antes de cualquier origen que ya exista en esa posición. El valor de índice de todos los orígenes de la lista después del índice especificado por el *Índice* se actualiza para garantizar que los valores de índice son únicos y se garantiza que el orden preexistente permanece sin cambios.

Si el *Índice* es mayor que el número de orígenes de la lista, el origen se coloca al final de la lista con un valor de índice de uno mayor que cualquier origen existente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Manuales**](product-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




