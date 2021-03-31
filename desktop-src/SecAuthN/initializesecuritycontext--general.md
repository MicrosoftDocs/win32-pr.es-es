---
description: Inicia el lado cliente, el contexto de [*seguridad*](../secgloss/s-gly.md) de salida de un identificador de credencial.
ms.assetid: 21d965d4-3c03-4e29-a70d-4538c5c366b0
title: Función InitializeSecurityContext (General, Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: bc96fe74202f1380d2d85946a373f176e14dfd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361214"
---
# <a name="initializesecuritycontext-general-function"></a>InitializeSecurityContext (general), función

La función **InitializeSecurityContext (general)** inicia el lado cliente, el contexto de [*seguridad*](../secgloss/s-gly.md) de salida de un identificador de credencial. La función se usa para crear un [*contexto de seguridad*](../secgloss/s-gly.md) entre la aplicación cliente y un elemento remoto del mismo nivel. **InitializeSecurityContext (general)** devuelve un token que el cliente debe pasar al elemento remoto del mismo nivel, que, a su vez, envía a la implementación de seguridad local a través de la llamada a [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) . El token generado debe considerarse opaco por todos los llamadores.

Normalmente, se llama a la función **InitializeSecurityContext (general)** en un bucle hasta que se establece un [*contexto de seguridad*](../secgloss/s-gly.md) suficiente.

Para obtener información sobre el uso de esta función con un [*proveedor de compatibilidad de seguridad*](../secgloss/s-gly.md) (SSP) específico, vea los temas siguientes.



| Tema                                                                                  | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)     | Inicia el lado cliente, el contexto de [*seguridad*](../secgloss/s-gly.md) de salida de un identificador de credencial mediante el [*paquete de seguridad*](../secgloss/s-gly.md)del proveedor de compatibilidad para seguridad de credenciales (CredSSP).  
| [**InitializeSecurityContext (Resumen)**](initializesecuritycontext--digest.md)       | Inicia el [*contexto de seguridad*](../secgloss/s-gly.md) de salida del lado cliente desde un identificador de credencial mediante el [*paquete de seguridad*](../secgloss/s-gly.md)de síntesis.                        |
| [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)   | Inicia el [*contexto de seguridad*](../secgloss/s-gly.md) de salida del lado cliente desde un identificador de credencial mediante el [*paquete de seguridad*](../secgloss/s-gly.md)de Kerberos.                      |
| [**InitializeSecurityContext (negociar)**](initializesecuritycontext--negotiate.md) | Inicia el [*contexto de seguridad*](../secgloss/s-gly.md) de salida del lado cliente desde un identificador de credencial mediante el [*paquete de seguridad*](../secgloss/s-gly.md)Negotiate.                     |
| [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)           | Inicia el [*contexto de seguridad*](../secgloss/s-gly.md) de salida del lado cliente desde un identificador de credencial mediante el [*paquete de seguridad*](../secgloss/s-gly.md)de NTLM.                          |
| [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)   | Inicia el [*contexto de seguridad*](../secgloss/s-gly.md) de salida del lado cliente desde un identificador de credencial mediante el [*paquete de seguridad*](../secgloss/s-gly.md)Schannel.                      |



 

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
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

Identificador de las credenciales devueltas por [**AcquireCredentialsHandle (general)**](acquirecredentialshandle--general.md). Este identificador se utiliza para compilar el [*contexto de seguridad*](../secgloss/s-gly.md). La función **InitializeSecurityContext (general)** requiere al menos credenciales de salida.

</dd> <dt>

*phContext* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [CtxtHandle](sspi-handles.md) . En la primera llamada a **InitializeSecurityContext (general)**, este puntero es **null**. En la segunda llamada, este parámetro es un puntero al identificador para el contexto parcialmente formado devuelto en el parámetro *phNewContext* por la primera llamada a.

Este parámetro es opcional con el Microsoft Digest SSP y se puede establecer en **null**.

Al usar Schannel SSP, en la primera llamada a **InitializeSecurityContext (general)**, especifique **null**. En futuras llamadas, especifique el token recibido en el parámetro *phNewContext* después de la primera llamada a esta función.

</dd> <dt>

*pTargetName* \[ en, opcional\]
</dt> <dd>

Puntero a una cadena terminada en null que indica el destino del contexto. El contenido de la cadena es específico del [*paquete de seguridad*](../secgloss/s-gly.md) , tal y como se describe en la tabla siguiente. Esta lista no es exhaustiva. Se pueden agregar a un sistema SSP de sistema adicionales y SSP de terceros.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>SSP en uso</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="Digest"></span><span id="digest"></span><span id="DIGEST"></span><dl> <dt><strong>Resumen</strong></dt> de <dt></dt> </dl></td><td>Cadena terminada en null que identifica de forma única el URI del recurso solicitado. La cadena debe estar formada por caracteres que se permiten en un URI y deben ser representables por el conjunto de código ASCII de EE. UU. La codificación de porcentaje puede usarse para representar caracteres fuera del conjunto de código ASCII de EE. UU.<br/></td></tr><tr class="even"><td><span id="Kerberos_or_Negotiate"></span><span id="kerberos_or_negotiate"></span><span id="KERBEROS_OR_NEGOTIATE"></span><dl> <dt><strong>Kerberos o Negotiate</strong></dt><dt></dt> </dl></td><td>Nombre principal de servicio (SPN) o el [*contexto de seguridad*](../secgloss/s-gly.md) del servidor de destino.<br/></td></tr><tr class="odd"><td><span id="NTLM"></span><span id="ntlm"></span><dl> <dt><strong>NTLM</strong></dt><dt></dt> </dl></td><td>Nombre principal de servicio (SPN) o el [*contexto de seguridad*](../secgloss/s-gly.md) del servidor de destino.<br/></td></tr><tr class="even"><td><span id="Schannel_SSL"></span><span id="schannel_ssl"></span><span id="SCHANNEL_SSL"></span><dl> <dt><strong>Schannel/SSL</strong></dt><dt></dt> </dl></td><td>Cadena terminada en null que identifica de forma única el servidor de destino. Schannel usa este valor para comprobar el certificado del servidor. Schannel también usa este valor para buscar la sesión en la memoria caché de la sesión al volver a establecer una conexión. La sesión almacenada en caché solo se utiliza si se cumplen todas las condiciones siguientes:<ul><li>El nombre de destino es el mismo.</li><li>La entrada de caché no ha expirado.</li><li>El proceso de aplicación que llama a la función es el mismo.</li><li>La sesión de inicio de sesión es la misma.</li><li>El identificador de la credencial es el mismo.</li></ul><br/></td></tr></tbody></table>



 

</dd> <dt>

*fContextReq* \[ de\]
</dt> <dd>

Marcas de bits que indican las solicitudes para el contexto. No todos los paquetes pueden admitir todos los requisitos. Las marcas usadas para este parámetro llevan el prefijo de ISC \_ req \_ , por ejemplo, el delegado de REQ de ISC \_ \_ . Este parámetro puede ser uno o varios de los siguientes marcadores de atributos.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Value</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>El [*paquete de seguridad*](../secgloss/s-gly.md) asigna los búferes de salida. Cuando haya terminado de usar los búferes de salida, liberelos mediante una llamada a la función [<strong>FreeContextBuffer</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-freecontextbuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Cifre los mensajes mediante la función [<strong>EncryptMessage</strong>] (encryptmessage--general.MD).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>El [*contexto de seguridad*](../secgloss/s-gly.md) no controlará los mensajes de formato. Este valor es el predeterminado para la [*delegación restringida*](../secgloss/s-gly.md)de Kerberos, Negotiate y NTLM.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>El servidor puede usar el contexto para autenticarse en otros servidores como cliente. Se debe establecer la marca de ISC_REQ_MUTUAL_AUTH para que esta marca funcione. Válido para Kerberos. Omita esta marca para la [*delegación restringida*](../secgloss/c-gly.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Cuando se produzcan errores, se notificará a la parte remota.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl> <dt><strong>ISC_REQ_HTTP</strong></dt> </dl></td><td>Usar síntesis para HTTP. Omita esta marca para usar Digest como mecanismo SASL.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Firmar mensajes y comprobar firmas mediante las funciones [<strong>EncryptMessage</strong>] (encryptmessage--general.MD) y [<strong>MakeSignature</strong>] (makesignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt> </dl></td><td>Schannel no debe autenticar el servidor automáticamente.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Se satisfará la Directiva de autenticación mutua del servicio.<br/><blockquote>[!Caution]<br />
Esto no significa necesariamente que se realice la autenticación mutua, solo que se cumple la Directiva de autenticación del servicio. Para asegurarse de que se realiza la autenticación mutua, llame a la función [<strong>QueryContextAttributes (general)</strong>] (querycontextattributes--general.MD).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Si se establece esta marca, se omite la marca <strong>ISC_REQ_INTEGRITY</strong> .<br/> Este valor solo es compatible con la [*delegación restringida*](../secgloss/s-gly.md)de Kerberos y Negotiate.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Detectar los mensajes reproducidos que se han codificado mediante las funciones [<strong>EncryptMessage</strong>] (encryptmessage--general.MD) o [<strong>MakeSignature</strong>] (makesignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Detecta mensajes recibidos de la secuencia.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Admitir una conexión orientada a flujos.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>Se debe negociar una nueva [*clave de sesión*](../secgloss/s-gly.md) .<br/> Este valor solo es compatible con la [*delegación restringida*](../secgloss/s-gly.md)de Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt> </dl></td><td>Schannel no debe intentar proporcionar credenciales para el cliente automáticamente.<br/></td></tr></tbody></table>



 

Es posible que el cliente no admita los atributos solicitados. Para obtener más información, consulte el parámetro *pfContextAttr* .

Para obtener más descripciones de los distintos atributos, vea [requisitos de contexto](context-requirements.md).

</dd> <dt>

*Reserved1* \[ de\]
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> <dt>

*TargetDataRep* \[ de\]
</dt> <dd>

Representación de los datos, como el orden de los bytes, en el destino. Este parámetro puede ser \_ \_ DREP nativo de seguridad o DREP de seguridad de \_ red \_ .

Este parámetro no se utiliza con Digest ni Schannel. Establézcalo en cero.

</dd> <dt>

*pInput* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene punteros a los búferes proporcionados como entrada para el paquete. A menos que el servidor inicie el contexto del cliente, el valor de este parámetro debe ser **null** en la primera llamada a la función. En las llamadas subsiguientes a la función o cuando el servidor inició el contexto de cliente, el valor de este parámetro es un puntero a un búfer asignado con suficiente memoria para contener el token devuelto por el equipo remoto.

</dd> <dt>

*Reserved2* \[ de\]
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> <dt>

*phNewContext* \[ in, out, opcional\]
</dt> <dd>

Puntero a una estructura [CtxtHandle](sspi-handles.md) . En la primera llamada a **InitializeSecurityContext (general)**, este puntero recibe el nuevo identificador de contexto. En la segunda llamada, *phNewContext* puede ser el mismo que el identificador especificado en el parámetro *phContext* .

Cuando se usa Schannel SSP, en las llamadas posteriores a la primera llamada, se pasa el identificador que se devuelve aquí como parámetro *phContext* y se especifica **null** para *phNewContext*.

</dd> <dt>

*pOutput* \[ in, out, opcional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene punteros a la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recibe los datos de salida. Si se ha escrito un búfer como lectura en segundo/lectura \_ en la entrada, se mostrará en la salida. El sistema asignará un búfer para el token de seguridad si se solicita (a través de \_ \_ \_ la solicitud de asignación de memoria de ISC) y rellenará la dirección en el descriptor de búfer para el token de seguridad.

Cuando se usa el Microsoft Digest SSP, este parámetro recibe la respuesta de desafío que se debe enviar al servidor.

Cuando se usa Schannel SSP, si \_ \_ se especifica la marca de memoria de asignación de solicitudes de ISC \_ , el SSP de Schannel asignará memoria para el búfer y colocará la información adecuada en [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc). Además, el llamador debe pasar un búfer de tipo **SECBUFFER \_ Alert**. En la salida, si se genera una alerta, este búfer contiene información sobre esa alerta y se produce un error en la función.

</dd> <dt>

*pfContextAttr* \[ enuncia\]
</dt> <dd>

Puntero a una variable para recibir un conjunto de marcadores de bits que indican los [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) del contexto establecido. Para obtener una descripción de los distintos atributos, vea [requisitos de contexto](context-requirements.md).

Las marcas usadas para este parámetro llevan el prefijo ISC \_ RET, como el \_ delegado de ISC RET \_ . Para obtener una lista de valores válidos, vea el parámetro *fContextReq* .

No Compruebe los atributos relacionados con la seguridad hasta que la llamada a la función final se devuelva correctamente. Las marcas de atributo que no están relacionadas con la seguridad, como la marca ASC RET allocated \_ \_ \_ Memory, se pueden comprobar antes de la devolución final.

> [!Note]  
> Los atributos de contexto concretos pueden cambiar durante la negociación con un elemento remoto del mismo nivel.

 

</dd> <dt>

*ptsExpiry* \[ out, opcional\]
</dt> <dd>

Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora de expiración del contexto. Se recomienda que el [*paquete de seguridad*](../secgloss/s-gly.md) devuelva siempre este valor en la hora local. Este parámetro es opcional y se debe pasar **null** para los clientes de corta duración.

No hay ningún tiempo de expiración para las credenciales o el [*contexto de seguridad*](../secgloss/s-gly.md)de SSP de Microsoft Digest.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve uno de los siguientes códigos de éxito.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ \_ finalización \_ y \_ continuación**</dt> </dl> | El cliente debe llamar a [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) y, a continuación, pasar la salida al servidor. Después, el cliente espera un token devuelto y lo pasa, en otra llamada, a [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md).<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**s \_ \_ finalización \_ necesaria**</dt> </dl>        | El cliente debe terminar de compilar el mensaje y, a continuación, llamar a la función [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ \_ \_**</dt> </dl>        | El cliente debe enviar el token de salida al servidor y esperar a que se devuelva un token. Después, el token devuelto se pasa en otra llamada a [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md). El token de salida puede estar vacío.<br/>                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ I \_ credenciales incompletas \_**</dt> </dl> | Use con Schannel. El servidor solicitó la autenticación del cliente y las credenciales proporcionadas no incluyen un certificado o el certificado no fue emitido por una entidad de certificación que sea de confianza para el servidor. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                              |
| <dl> <dt>**s \_ E \_ mensaje incompleto \_**</dt> </dl>     | Use con Schannel. Los datos de todo el mensaje no se leyeron desde la conexión.<br/> Cuando se devuelve este valor, el búfer *pInput* contiene una estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un miembro **BufferType** de **SecBuffer \_ que falta**. El miembro **cbBuffer** de **SecBuffer** contiene un valor que indica el número de bytes adicionales que la función debe leer del cliente antes de que esta función se ejecute correctamente. Aunque este número no siempre es preciso, su uso puede ayudar a mejorar el rendimiento al evitar varias llamadas a esta función.<br/> |
| <dl> <dt>**s \_ E \_ Aceptar**</dt> </dl>                      | El [*contexto de seguridad*](../secgloss/s-gly.md) se inicializó correctamente. No es necesario otra llamada [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) . Si la función devuelve un token de salida, es decir, si el \_ token de SECBUFFER en *pOutput* tiene una longitud distinto de cero, ese token se debe enviar al servidor.<br/>                                                                                                                                                    |



 

Si se produce un error en la función, la función devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                          | Descripción                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ memoria insuficiente \_**</dt> </dl>          | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ E \_ interno \_ error**</dt> </dl>               | Error que no se ha asignado a un código de error SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ identificador no válido \_**</dt> </dl>               | El identificador pasado a la función no es válido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ token no válido \_**</dt> </dl>                | El error se debe a un token de entrada mal formado, como un token dañado en tránsito, un token de tamaño incorrecto o un token pasado al [*paquete de seguridad*](../secgloss/s-gly.md)equivocado. El paso de un token al paquete equivocado puede producirse si el cliente y el servidor no negociaron el [*paquete de seguridad*](../secgloss/s-gly.md)adecuado.<br/> |
| <dl> <dt>**s \_ E \_ Inicio de sesión \_ denegado**</dt> </dl>                 | Error de inicio de sesión.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ sin \_ entidad de autenticación \_**</dt> </dl> | No se pudo establecer contacto con ninguna autoridad para la autenticación. El nombre de dominio de la entidad de autenticación podría ser incorrecto, el dominio podría estar inaccesible o podría haber un error de relación de confianza.<br/>                                                                                  |
| <dl> <dt>**s \_ E \_ sin \_ credenciales**</dt> </dl>               | No hay credenciales disponibles en el [*paquete de seguridad*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**s \_ E \_ destino \_ desconocido**</dt> </dl>               | No se reconoció el destino.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E \_ función no admitida \_**</dt> </dl>         | Una marca de atributo de contexto que no es válida (el \_ \_ delegado de REQ de ISC o \_ \_ el símbolo del sistema \_ de solicitudes de ISC para \_ las credenciales) se especificó en el parámetro *fContextReq* .<br/>                                                                                                                                            |
| <dl> <dt>**s \_ E \_ entidad de seguridad equivocada \_**</dt> </dl>              | La entidad de seguridad que recibió la solicitud de autenticación no es la misma que la que se pasa al parámetro *pszTargetName* . Esto indica un error en la autenticación mutua.<br/>                                                                                                          |



 

## <a name="remarks"></a>Observaciones

El autor de la llamada es responsable de determinar si los atributos de contexto finales son suficientes. Si, por ejemplo, se solicitó la confidencialidad, pero no se pudo establecer, algunas aplicaciones pueden optar por cerrar la conexión inmediatamente.

Si los atributos del [*contexto de seguridad*](../secgloss/s-gly.md) no son suficientes, el cliente debe liberar el contexto creado parcialmente mediante una llamada a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

Un cliente utiliza la función **InitializeSecurityContext (general)** para inicializar un contexto de salida.

Para un [*contexto de seguridad*](../secgloss/s-gly.md)de dos tramos, la secuencia de llamada es la siguiente:

1.  El cliente llama a la función con *phContext* establecido en **null** y rellena el descriptor del búfer con el mensaje de entrada.
2.  El [*paquete de seguridad*](../secgloss/s-gly.md) examina los parámetros y construye un token opaco, colocándolo en el elemento de token en la matriz de búferes. Si el parámetro *fContextReq* incluye la \_ marca ISC req \_ allocate \_ Memory, el [*paquete de seguridad*](../secgloss/s-gly.md) asigna la memoria y devuelve el puntero en el elemento token.
3.  El cliente envía el token devuelto en el búfer de *pOutput* al servidor de destino. A continuación, el servidor pasa el token como argumento de entrada en una llamada a la función [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) .
4.  [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) puede devolver un token, que el servidor envía al cliente para una segunda llamada a **InitializeSecurityContext (general)** si la primera llamada que se devuelve \_ es que se \_ \_ necesita.

En el caso de los [*contextos de seguridad*](../secgloss/s-gly.md)de varios tramos, como la autenticación mutua, la secuencia de llamada es la siguiente:

1.  El cliente llama a la función tal y como se describió anteriormente, pero el paquete devuelve el código de éxito de las SEC \_ que sigo \_ siendo \_ necesarios.
2.  El cliente envía el token de salida al servidor y espera la respuesta del servidor.
3.  Tras recibir la respuesta del servidor, el cliente llama a **InitializeSecurityContext (general)** de nuevo, con *phContext* establecido en el identificador que se devolvió desde la última llamada. El token recibido del servidor se proporciona en el parámetro *pInput* .

Si el servidor ha respondido correctamente, el [*paquete de seguridad*](../secgloss/s-gly.md) devuelve sec \_ e \_ OK y se establece una sesión segura.

Si la función devuelve una de las respuestas de error, no se acepta la respuesta del servidor y no se establece la sesión.

Si la función devuelve los segundos que \_ se \_ necesitan para continuar, \_ \_ \_ es necesario que se complete la segunda vez o se \_ \_ \_ \_ \_ repiten los pasos 2 y 3.

Para inicializar un [*contexto de seguridad*](../secgloss/s-gly.md), es posible que se requiera más de una llamada a esta función, dependiendo del mecanismo de autenticación subyacente, así como de las opciones especificadas en el parámetro *fContextReq* .

Los parámetros *fContextReq* y *pfContextAttributes* son máscaras de texto que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [requisitos de contexto](context-requirements.md). El parámetro *pfContextAttributes* es válido en cualquier devolución correcta, pero solo en la devolución correcta final debe examinar las marcas que pertenecen a los aspectos de seguridad del contexto. Las devoluciones intermedias se pueden establecer, por ejemplo, la \_ \_ marca de memoria asignada de ISC \_ .

Si \_ \_ \_ se establece la marca de credenciales proporcionadas por el uso de ISC \_ , el [*paquete de seguridad*](../secgloss/s-gly.md) debe buscar un \_ tipo de búfer params de SECBUFFER pkg \_ en el búfer de entrada *pInput* . Esta no es una solución genérica, pero permite un fuerte emparejamiento del [*paquete de seguridad*](../secgloss/s-gly.md) y de la aplicación cuando sea necesario.

Si \_ se especificó la solicitud de asignación de memoria de ISC \_ \_ , el llamador debe liberar la memoria mediante una llamada a la función [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Por ejemplo, el token de entrada podría ser el desafío de un administrador de LAN. En este caso, el token de salida sería la respuesta cifrada NTLM al desafío.

La acción que realiza el cliente depende del código de retorno de esta función. Si el código de retorno es en segundos \_ E \_ OK, no habrá ninguna segunda llamada a **InitializeSecurityContext (general)** y no se espera ninguna respuesta del servidor. Si el código de retorno es \_ la \_ necesidad de continuar \_ , el cliente espera un token en respuesta del servidor y lo pasa en una segunda llamada a **InitializeSecurityContext (general)**. El código de retorno seg. de \_ \_ finalización \_ necesario indica que el cliente debe terminar de compilar el mensaje y llamar a la función [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . El \_ código sec I \_ Complete \_ y \_ continue incorpora ambas acciones.

Si **InitializeSecurityContext (general)** devuelve SUCCESS en la primera llamada (o solo), el llamador debe llamar finalmente a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) en el identificador devuelto, aunque se produzca un error en la llamada en un segmento posterior del intercambio de autenticación.

El cliente puede llamar a **InitializeSecurityContext (general)** una vez que se haya completado correctamente. Esto indica al [*paquete de seguridad*](../secgloss/s-gly.md) que se desea una reautenticación.

Los llamadores del modo kernel tienen las siguientes diferencias: el nombre de destino es una cadena [*Unicode*](../secgloss/u-gly.md) que debe asignarse en la memoria virtual mediante [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); no debe estar asignado desde el grupo. Los búferes pasados y proporcionados en *pInput* y *pOutput* deben estar en la memoria virtual, no en el grupo.

Cuando se usa Schannel SSP, si la función devuelve \_ \_ \_ las CREDENCIALes de s incompletas, compruebe que especificó un certificado válido y de confianza en sus credenciales. El certificado se especifica cuando se llama a la función [**AcquireCredentialsHandle (general)**](acquirecredentialshandle--general.md) . El certificado debe ser un certificado de autenticación de cliente emitido por una entidad de certificación (CA) que sea de confianza para el servidor. Para obtener una lista de las entidades de certificación de confianza del servidor, llame a la función [**QueryContextAttributes (general)**](querycontextattributes--general.md) y especifique el \_ atributo de lista de emisores de SECPKG ATTR \_ \_ \_ .

Cuando se usa Schannel SSP, una vez que una aplicación cliente recibe un certificado de autenticación de una CA que es de confianza para el servidor, la aplicación crea una nueva credencial mediante una llamada a la función [**AcquireCredentialsHandle (general)**](acquirecredentialshandle--general.md) y, a continuación, llama a **InitializeSecurityContext (general)** de nuevo, especificando la nueva credencial en el parámetro *phCredential* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>SECUR32. lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nombres Unicode y ANSI<br/>   | **InitializeSecurityContextW** (Unicode) y **InitializeSecurityContextA** (ANSI)<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**AcquireCredentialsHandle (general)**](acquirecredentialshandle--general.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
