---
title: Enumeración WMDM_STORAGE_ENUM_MODE
description: El \_ tipo de \_ enumeración de modo de enumeración de almacenamiento WMDM \_ define cómo se va a enumerar el contenido del almacenamiento. IWMDMStorage3 SetEnumPreference usa esta enumeración.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- Enumeración WMDM_STORAGE_ENUM_MODE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698642"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a>\_ \_ Enumeración de modo de enumeración de almacenamiento WMDM \_

El tipo de enumeración de **\_ \_ \_ modo de enumeración de almacenamiento WMDM** define cómo se va a enumerar el contenido del almacenamiento. [**IWMDMStorage3:: SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference)usa esta enumeración.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**modo de ENUMERAción \_ \_ sin formato**
</dt> <dd>

Enumera el contenido del almacenamiento tal como está organizado en el sistema de archivos del almacenamiento.

**modo de ENUMERAción \_ \_ use \_ Pref de dispositivo \_**

Enumera el contenido del almacenamiento en función de la preferencia del dispositivo, tal como se indica en el parámetro de dispositivo *UseMetadataViews* .

**\_vistas de \_ metadatos de modo de enumeración \_**

Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.

</dd> <dt>

<span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**modo de ENUMERAción \_ \_ use \_ Pref de dispositivo \_**
</dt> <dd>

Enumera el contenido del almacenamiento en función de la preferencia del dispositivo, tal como se indica en el parámetro de dispositivo *UseMetadataViews* .

**\_vistas de \_ metadatos de modo de enumeración \_**

Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.

</dd> <dt>

<span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_vistas de \_ metadatos de modo de enumeración \_**
</dt> <dd>

Enumera el contenido del almacenamiento organizando el contenido en función de una vista de metadatos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





