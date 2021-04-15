---
title: En (sendEmailType) (elemento)
description: Contiene las direcciones de correo electrónico a las que se enviará el correo electrónico.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- Al elemento Programador de tareas
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676621"
---
# <a name="to-sendemailtype-element"></a>En (sendEmailType) (elemento)

Contiene las direcciones de correo electrónico a las que se enviará el correo electrónico.

``` syntax
<xs:element name="To"
    type="string"
 />
```

El elemento **to** se define mediante el tipo complejo de [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                              | Derivado de                                                           | Descripción                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa una acción que envía un mensaje de correo electrónico.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**to (propiedad) de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).

Para el desarrollo de scripts, vea [**EmailAction.to**](emailaction-to.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





