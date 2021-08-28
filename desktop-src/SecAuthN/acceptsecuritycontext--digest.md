---
description: Permite que el componente de servidor de una aplicación de transporte establezca un contexto de seguridad entre el servidor y un cliente remoto que usa Digest.
ms.assetid: 017683e3-b21a-4e97-9232-582ac7dbd5b2
title: Función AcceptSecurityContext (Digest) (Sspi.h)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: ec6ad11e754124f56f5852b4e0b0a0347f1bb099
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628717"
---
# <a name="acceptsecuritycontext-digest-function"></a>Función AcceptSecurityContext (Digest)

La **función AcceptSecurityContext (Digest)** permite que el componente de servidor de una aplicación de transporte establezca un contexto de seguridad [*entre*](../secgloss/s-gly.md) el servidor y un cliente remoto. El cliente remoto usa la [**función InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) para iniciar el proceso de establecimiento de un contexto de seguridad. El servidor puede requerir uno o varios tokens de respuesta del cliente remoto para completar el establecimiento del contexto de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _Inout_opt_ PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phCredential* \[ en, opcional\]
</dt> <dd>

Identificador de las credenciales del servidor. El servidor llama a [**la función AcquireCredentialsHandle (Digest)**](acquirecredentialshandle--digest.md) con la marca SECPKG CRED INBOUND o \_ SECPKG CRED BOTH establecida para \_ recuperar este \_ \_ identificador.

</dd> <dt>

*phContext* \[ in, out, optional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **AcceptSecurityContext (Digest),** este puntero es **NULL.** En las llamadas posteriores, *phContext* es el identificador del contexto parcialmente formado que la primera llamada devolvió en el parámetro *phNewContext.*

</dd> <dt>

*pInput* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generada por una llamada de cliente a [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) que contiene el descriptor de búfer de entrada.

En la tabla siguiente se muestra la configuración del búfer para HTTP de síntesis. El primer búfer debe ser de tipo **\_ SECBUFFER TOKEN** y el resto debe ser de tipo **SECBUFFER \_ PKG \_ PARAMS.** SASL solo requiere el búfer cero.



| Buffer \# /buffer type                                                                                                                                                                                                 | Significado                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**TOKEN DE**</dt> <dt> **0 \_ SECBUFFER**</dt> </dl>                                        | Vacío para la primera llamada y la respuesta de desafío recibida del cliente para la segunda llamada.<br/>                                                             |
| <span id="1"></span><dl> <dt>**1**</dt> <dt> **SBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Método. Los caracteres son formato de línea de conexión de la línea de solicitud. Caracteres de un solo byte ASCII de EE. UU.<br/>                                                                |
| <span id="2"></span><dl> <dt>**2**</dt> <dt> **SBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Reservado.<br/>                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> <dt> **SBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | HEntity. Representación hexadecimal de H(entity-body). Caracteres de un solo byte ASCII de EE. UU.<br/>                                                                       |
| <span id="4"></span><dl> <dt>**4**</dt> <dt> **SBUFFER \_ PKG \_ PARAMS**</dt> </dl>                                  | Reino. Cadena de dominio del desafío. Cadena Unicode que debe ser representable en ASCII de EE. UU.<br/>                                                                 |
| <span id="5"></span><dl> <dt>**ENLACES DE CANAL**</dt> SECBUFFER DE 5 <dt> **\_ \_** \| **SECBUFFER \_ READONLY**</dt> </dl> | Contiene el valor del token de enlace de canal.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |



 

</dd> <dt>

*fContextReq* \[ En\]
</dt> <dd>

Marcas de bits que especifican los atributos requeridos por el servidor para establecer el contexto. Las marcas de bits se pueden combinar mediante operaciones **OR** bit a bit. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASIGNACIÓN DE MEMORIA DE ASC \_ REQ \_ \_**</dt> </dl>                                                  | Digest le asigna búferes de salida. Cuando haya terminado de usar los búferes de salida, puede liberarlos llamando a la [**función FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br/>                                                                                                                                                                                                                                      |
| <span id="ASC_REQ_ALLOW_MISSING_BINDINGS"></span><span id="asc_req_allow_missing_bindings"></span><dl> <dt>**ASC \_ REQ PERMITIR \_ ENLACES QUE \_ \_ FALTAN**</dt> </dl>                            | Indica que digest no requiere enlaces de canal para los canales internos y externos. Este valor se usa para la compatibilidad con versiones anteriores cuando no se conoce la compatibilidad con el enlace de canal de punto de conexión.<br/> Este valor es mutuamente excluyente con **ASC \_ REQ \_ PROXY \_ BINDINGS**.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> <br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**CONFIDENCIALIDAD DE ASC \_ REQ \_**</dt> </dl>                                                   | Cifrar y descifrar mensajes. <br/> El SSP de resumen solo admite esta marca para SASL.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="ASC_REQ_PROXY_BINDINGS"></span><span id="asc_req_proxy_bindings"></span><dl> <dt>**ENLACES DE PROXY DE ASC \_ REQ \_ \_**</dt> </dl>                                                     | Indica que digest requiere el enlace de canal.<br/> Este valor es mutuamente excluyente con **ASC \_ REQ \_ ALLOW MISSING \_ \_ BINDINGS**.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> <br/>                                                                                                                                         |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**CONEXIÓN DE ASC \_ \_ REQ**</dt> </dl>                                                                  | El [*contexto de seguridad*](../secgloss/s-gly.md) no controlará los mensajes de formato.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ERROR EXTENDIDO DE ASC \_ REQ \_ \_**</dt> </dl>                                                     | Cuando se produzcan errores, se notificará a la parte remota.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="ASC_REQ_HTTP__0x10000000_"></span><span id="asc_req_http__0x10000000_"></span><span id="ASC_REQ_HTTP__0X10000000_"></span><dl> <dt>**ASC \_ REQ \_ HTTP (0x10000000)**</dt> </dl> | Use Digest para HTTP. Omita esta marca para usar Digest como mecanismo SASL.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**INTEGRIDAD DE ASC \_ REQ \_**</dt> </dl>                                                                     | Firmar mensajes y comprobar firmas.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>                                                        | Detectar paquetes reproducido.<br/>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl>                                                  | Detectar los mensajes recibidos fuera de la secuencia.<br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

Para ver las posibles marcas de atributo y sus significados, vea [Requisitos de contexto.](context-requirements.md) Las marcas usadas para este parámetro tienen el prefijo ASC \_ REQ, por ejemplo, ASC \_ REQ \_ DELEGATE.

Es posible que el cliente no sea compatible con los atributos solicitados. Para obtener más información, vea el *parámetro pfContextAttr.*

</dd> <dt>

*TargetDataRep* \[ En\]
</dt> <dd>

Representación de datos, como la ordenación de bytes, en el destino. Este parámetro puede ser SECURITY \_ NATIVE \_ DREP o SECURITY \_ NETWORK \_ DREP.

Este parámetro no se usa con digest SSP. Cuando use Digest SSP, especifique cero para este parámetro.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **AcceptSecurityContext (Digest),** este puntero recibe el nuevo identificador de contexto. En las llamadas posteriores, *phNewContext* puede ser el mismo que el identificador especificado en el *parámetro phContext.*

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene el descriptor de búfer de salida. Este búfer se envía al cliente para su entrada en llamadas adicionales [**a InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Se puede generar un búfer de salida incluso si la función devuelve SEC \_ E \_ OK. Cualquier búfer generado debe devolverse a la aplicación cliente.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un conjunto de marcas de bits que indican los atributos del contexto establecido. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md) Las marcas usadas para este parámetro tienen el prefijo ASC \_ RET, por ejemplo, ASC \_ RET \_ DELEGATE.

No compruebe los atributos relacionados con la seguridad hasta que la llamada a la función final se devuelva correctamente. Las marcas de atributo no relacionadas con la seguridad, como la marca ASC RET ALLOCATED MEMORY, se pueden comprobar \_ \_ antes de la \_ devolución final.

</dd> <dt>

*ptsTimeStamp* \[ out, opcional\]
</dt> <dd>

Puntero a una [**estructura TimeStamp**](timestamp.md) que recibe la hora de expiración del contexto. Se recomienda que el [*paquete de seguridad*](../secgloss/s-gly.md) devuelva siempre este valor en la hora local.

Este parámetro se establece en un tiempo máximo constante. No hay tiempo de expiración para las credenciales o contextos de seguridad [*de*](../secgloss/s-gly.md)resumen o cuando se usa el SSP de resumen.

> [!Note]  
> Hasta la última llamada del proceso de autenticación, la hora de expiración del contexto puede ser incorrecta porque se proporciona más información durante las fases posteriores de la negociación. Por lo tanto, *ptsTimeStamp* debe ser **NULL hasta** la última llamada a la función.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los valores siguientes.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Código o valor devuelto</th><th>Descripción</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Error en la función. No hay suficiente memoria disponible para completar la acción solicitada.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Error en la función. Error que no se ha asignado a un código de error SSPI.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Error en la función. El identificador pasado a la función no es válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Error en la función. El token pasado a la función no es válido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Error de inicio de sesión.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Error en la función. No se pudo ponerse en contacto con ninguna autoridad para la autenticación. Esto podría deberse a las condiciones siguientes:<br/><ul><li>El nombre de dominio de la entidad de autenticación es incorrecto.</li><li>El dominio no está disponible.</li><li>Error en la relación de confianza.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>Error en la función. El identificador de credenciales especificado en el <em>parámetro phCredential</em> no es válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>La función se ha realizado correctamente. Se [*aceptó*](../secgloss/s-gly.md) el contexto de seguridad recibido del cliente. Si la función generó un token de salida, se debe enviar al proceso de cliente.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_SECURITY_QOS_FAILED</strong></dt> <dt>0x80090332L</dt> </dl></td><td>Error en la función. Se especificó una marca de atributo de contexto que no es válida en el <em>parámetro fContextReq.</em><br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe llamar a [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) y pasar el token de salida al cliente. A continuación, el servidor espera un token de devolución del cliente y, a continuación, realiza otra llamada a [<strong>AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe terminar de compilar el mensaje desde el cliente y, a continuación, llamar a la función [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe enviar el token de salida al cliente y esperar un token devuelto. El token devuelto debe pasarse en <em>pInput para</em> otra llamada a [<strong>AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>Error en la función. Se llamó a la función [<strong>AcceptSecurityContext (Digest)</strong>](acceptsecuritycontext--digest.md) después de establecer el contexto especificado.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_BAD_BINDINGS</strong></dt> <dt>0x80090346L</dt> </dl></td><td>Error en la función. No se ha cumplido la directiva de enlace de canal.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Comentarios

La **función AcceptSecurityContext (Digest)** es el homólogo del servidor de [**la función InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md)

Cuando el servidor recibe una solicitud de un cliente, el servidor usa el parámetro *fContextReq* para especificar lo que requiere de la sesión. De este modo, un servidor puede especificar que los [](../secgloss/i-gly.md)clientes deben ser capaces de usar una sesión confidencial o comprobada por integridad, y puede rechazar clientes que no puedan satisfacer esa demanda. Como alternativa, un servidor no puede requerir nada y lo que el cliente pueda proporcionar o requiera se devuelve en el *parámetro pfContextAttr.*

Para un paquete que admite la autenticación de varios pasos, como la autenticación mutua, la secuencia de llamada es la siguiente:

1.  El cliente transmite un token al servidor.
2.  El servidor llama **a AcceptSecurityContext (Digest)** la primera vez, lo que genera un token de respuesta que se envía al cliente.
3.  El cliente recibe el token y lo pasa a [**InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Si **InitializeSecurityContext (Digest)** devuelve SEC E OK, se ha completado la autenticación mutua y se puede iniciar \_ una sesión \_ segura. Si **InitializeSecurityContext (Digest)** devuelve un código de error, finaliza la negociación de autenticación mutua. De lo contrario, el token de seguridad devuelto por **InitializeSecurityContext (Digest)** se envía al cliente y se repiten los pasos 2 y 3.

Los *parámetros fContextReq* y *pfContextAttr* son máscaras de bits que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md)

> [!Note]  
> El *parámetro pfContextAttr es* válido en cualquier devolución correcta, pero solo en la devolución correcta final debe examinar las marcas relativas a los aspectos de seguridad del contexto. Los resultados intermedios pueden establecer, por ejemplo, la marca \_ ISC RET \_ ALLOCATED \_ MEMORY.

 

El autor de la llamada es responsable de determinar si los atributos de contexto final son suficientes. Si, por ejemplo, se solicitó confidencialidad (cifrado), pero no se pudo establecer, algunas aplicaciones pueden optar por apagar la conexión inmediatamente. Si no [*se puede establecer el*](../secgloss/s-gly.md) contexto de seguridad, el servidor debe liberar el contexto creado parcialmente llamando a la función [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) Para obtener información sobre cuándo llamar a **la función DeleteSecurityContext,** vea **DeleteSecurityContext**.

Una vez [*establecido el contexto*](../secgloss/s-gly.md) de seguridad, la aplicación de servidor puede usar la función [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar un identificador de la cuenta de usuario a la que se ha asignado el certificado de cliente. Además, el servidor puede usar la [**función ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para suplantar al usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> </dl>

 

 
