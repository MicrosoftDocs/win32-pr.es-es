---
description: Especifica la hora de inicio de una topología, relativa al inicio de la primera topología de la secuencia.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: MF_TOPOLOGY_PROJECTSTOP atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544334"
---
# <a name="mf_topology_projectstop-attribute"></a>\_Atributo PROJECTSTOP de la topología MF \_

Especifica la hora de inicio de una topología, relativa al inicio de la primera topología de la secuencia.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Trata como un valor de **LONGLONG** .

## <a name="remarks"></a>Observaciones

El valor se proporciona en unidades de 100 nanosegundos.

Si la sesión multimedia se creó con el atributo de [**\_ \_ \_ hora global de la sesión MF**](mf-session-global-time-attribute.md) igual a **true**, todas las topologías deben contener el atributo PROJECTSTOP de la **\_ topología \_ MF** . De lo contrario, las topologías no deben contener el atributo **\_ \_ PROJECTSTOP de la topología MF** . Para obtener más información, vea [tiempos de presentación de secuencias](sequence-presentation-times.md).

Este atributo es un valor con signo, aunque se almacena como **UINT64**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tiempos de presentación de secuencia](sequence-presentation-times.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**\_PROJECTSTART de topología \_ MF**](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




