---
description: El método ReferencesAsync de SWbemObject proporciona una colección de todas las clases de asociación o instancias \_ que hacen referencia al objeto actual. Este método realiza la misma función que la consulta WQL REFERENCES OF.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: SWbemObject.ReferencesAsync_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 551a54430724e52ede0ee0000ac48a8593f4145e2a875766c61da9c24de45c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640075"
---
# <a name="swbemobjectreferencesasync_-method"></a>Método SWbemObject.ReferencesAsync \_

El **método \_ ReferencesAsync** de [**SWbemObject**](swbemobject.md) proporciona una colección de todas las clases de asociación o instancias que hacen referencia al objeto actual. Este método realiza la misma función que la consulta WQL [REFERENCES OF.](references-of-statement.md)

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objWbemSink* \[ En\]
</dt> <dd>

Obligatorio. Receptor de objetos que recibe los objetos de forma asincrónica.

</dd> <dt>

*strResultClass* \[ in, opcional\]
</dt> <dd>

Cadena que contiene un nombre de clase. Si se especifica, este parámetro indica que los objetos de asociación devueltos deben pertenecer a o derivarse de la clase especificada en este parámetro.

</dd> <dt>

*strRole* \[ in, opcional\]
</dt> <dd>

Cadena que contiene un nombre de propiedad. Si se especifica, este parámetro indica que los objetos de asociación devueltos deben limitarse a aquellos en los que el objeto de origen desempeña un rol específico. El nombre de una propiedad de referencia especificada define el rol de una asociación.

</dd> <dt>

*bClassesOnly* \[ in, opcional\]
</dt> <dd>

Valor booleano que indica si se debe devolver o no una lista de nombres de clase en lugar de instancias reales de las clases. Estas son las clases a las que pertenecen los objetos de asociación. El valor predeterminado de este parámetro es **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ in, opcional\]
</dt> <dd>

Valor booleano que indica si la consulta se aplica o no al esquema en lugar de a los datos. El valor predeterminado de este parámetro es **FALSE.** Solo se puede establecer en **TRUE** si el objeto en el que se invoca este método es una clase . Cuando se establece en **TRUE**, el conjunto de puntos de conexión devueltos representa las clases que están asociadas adecuadamente a la clase de origen en el esquema.

</dd> <dt>

*strRequiredQualifier* \[ in, opcional\]
</dt> <dd>

Cadena que contiene un nombre de calificador. Si se especifica, este parámetro indica que los objetos de asociación devueltos deben incluir el calificador especificado.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Entero que especifica marcas adicionales a la operación. Este parámetro puede aceptar los valores siguientes.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Hace que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**SWbemSink.OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Impide que las llamadas asincrónicas envíen actualizaciones de estado al controlador de eventos [**OnProgress**](swbemsink-onprogress.md) para el receptor del objeto.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Hace que Windows Management Instrumentation (WMI) devuelva datos de modificación de clase con la definición de clase base. Para obtener más información, vea [Localización de información de clase WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [SWbemNamedValueSet](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> <dt>

*objWbemAsyncContext* \[ in, opcional\]
</dt> <dd>

Se trata de [un objeto SWbemNamedValueSet](swbemnamedvalueset.md) que vuelve al receptor del objeto para identificar el origen de la llamada asincrónica original. Use este parámetro si realiza varias llamadas asincrónicas con el mismo receptor de objetos. Para usar este parámetro, cree un objeto SWbemNamedValueSet y use el método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para agregar un valor que identifique la llamada asincrónica que está realizando. Este objeto SWbemNamedValueSet se devuelve al receptor del objeto y el origen de la llamada se puede extraer mediante el método [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obtener más información, vea [Llamar a un método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor. Si se realiza correctamente, el receptor recibe un [**evento OnObjectReady**](swbemsink-onobjectready.md) por instancia. Después de la última instancia, el receptor del objeto recibe un [**evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ReferencesAsync, \_** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El usuario actual no tiene permiso para ver una o varias de las clases devueltas por la llamada.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta llamada se devuelve inmediatamente. Los objetos y el estado solicitados se devuelven al autor de la llamada a través de devoluciones de llamada entregadas al receptor especificado en *objWbemSink*. Para procesar cada objeto cuando llega, cree *un objWbemSink*. [**Subrutina de eventos OnObjectReady.**](swbemsink-onobjectready.md) Una vez devueltos todos los objetos, puede realizar el procesamiento final en la implementación de *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Una devolución de llamada asincrónica permite que un usuario no autenticado proporcione datos al receptor. Esto supone riesgos de seguridad para los scripts y las aplicaciones. Para eliminar los riesgos, use la comunicación semisincrónica o la comunicación sincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

Para obtener más información sobre las referencias de consulta WQL asociada, instancias de origen y objetos de asociación, vea [LA INSTRUCCIÓN ASSOCIATORS OF](associators-of-statement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices.ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

