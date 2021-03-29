---
description: Proporciona servicios para establecer el código CHV (comprobación del titular de la tarjeta) y para comprobar el usuario.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Interfaz ISCardVerify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814379"
---
# <a name="iscardverify-interface"></a>Interfaz ISCardVerify

\[La interfaz **ISCardVerify** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La siguiente definición de interfaz se proporciona como un estándar que se puede seguir al desarrollar un [*proveedor de servicios*](../secgloss/c-gly.md)de [*tarjetas inteligentes*](../secgloss/s-gly.md) . La interfaz **ISCardVerify** proporciona servicios para establecer el código CHV (comprobación del titular de la tarjeta) y para comprobar el usuario.

La clase **ISCardVerify** se define para las aplicaciones que implementan la Directiva CHV específica de la aplicación y que tienen un conocimiento detallado de la implementación interna de la tarjeta inteligente.

A continuación se usa el uso típico de la interfaz **ISCardVerify** .

En el procedimiento siguiente se usa **ISCardVerify** para cambiar el código CHV.

**Para cambiar el código CHV de una tarjeta inteligente**

1.  Cree una interfaz **ISCardVerify** (mediante el método de interfaz [**ISCardManage**](iscardmanage.md) correspondiente).
2.  Llame al método [**ChangeCode**](iscardverify-changecode.md) y proporcione código nuevo, especificando si es local o global y si está habilitado o deshabilitado.
3.  Libere la interfaz **ISCardVerify** .

## <a name="members"></a>Miembros

La interfaz **ISCardVerify** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardVerify** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISCardVerify** tiene estos métodos.



| Método                                                        | Descripción                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeCode**](iscardverify-changecode.md)                 | Cambia el código CHV actual.<br/>                                                                                                    |
| [**ResetSecurityState**](iscardverify-resetsecuritystate.md) | Restablece el [*contexto de seguridad*](../secgloss/s-gly.md) de la tarjeta inteligente.<br/> |
| [**Desbloquear**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))                       | Vuelve a habilitar el [*contexto de seguridad*](../secgloss/s-gly.md).<br/>               |
| [**Ver**](iscardverify-verify.md)                         | Autentica al usuario.<br/>                                                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



 

 
