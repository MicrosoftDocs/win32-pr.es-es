---
description: La propiedad ComponentClients de solo lectura devuelve un objeto StringList que enumera el conjunto de clientes de un componente especificado.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Installer.ComponentClients, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c94a30247bbfc39675308308457c369785bd9a67413a5b0b62af143e17e2112b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632717"
---
# <a name="installercomponentclients-property"></a>Installer.ComponentClients, propiedad

La propiedad **ComponentClients de** solo lectura devuelve un [**objeto StringList**](stringlist-object.md) que enumera el conjunto de clientes de un componente especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Valor de propiedad

GUID de cadena que representa el código de componente del componente. Los códigos de componente se especifican en la columna ComponentId de la [tabla Component](component-table.md).

## <a name="remarks"></a>Comentarios

Para enumerar los clientes de componentes, una aplicación puede recorrer en iteración el [**objeto StringList**](stringlist-object.md) mediante una construcción For Each. Dado que los clientes no están ordenados, los nuevos componentes tienen un índice arbitrario. Esto significa que la función puede devolver clientes en cualquier orden.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




