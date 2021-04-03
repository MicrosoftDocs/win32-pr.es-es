---
title: ncadg_ipx atributo)
description: La \_ palabra clave ncadg IPX identifica IPX como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx el atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790185"
---
# <a name="ncadg_ipx-attribute"></a>ncadg \_ atributo IPX

La palabra clave **ncadg \_ IPX** identifica IPX como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dirección de vínculo* 
</dt> <dd>

Especifica el servidor host. Puede ser una cadena de caracteres (el nombre del servidor) o un número hexadecimal de 20 dígitos que consta de la dirección de red del servidor host (8 dígitos) concatenada con la dirección del nodo (12 dígitos). Vea la sección Comentarios para obtener instrucciones sobre cómo obtener la dirección de red y la dirección de nodo. Una cadena **nula** especifica el equipo local.

</dd> <dt>

*nombre del puerto* 
</dt> <dd>

Especifica un número de 16 bits opcional que representa la dirección del socket. Los valores pueden oscilar entre 1 y 65535. Cuando no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de Puerto* válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las siguientes restricciones se aplican a los protocolos de datagramas, **ncadg \_ IPX** y [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md):

-   No admiten las devoluciones de llamada. **\[** [](callback.md) Se producirá un error en todas las funciones que utilicen el **\]** atributo callback.
-   No admiten el uso del constructor de tipo de [**canalización**](pipe.md) .

Cuando se usa el transporte **\_ IPX ncadg** , el nombre del servidor es exactamente el mismo que el nombre de Windows Server de 32 bits. Sin embargo, puesto que los nombres se distribuyen mediante protocolos de Novell, deben cumplir las convenciones de nomenclatura de Novell. Si un nombre de servidor no es un nombre de Novell válido, los servidores no podrán crear extremos con el transporte **\_ IPX ncadg** . La siguiente es una lista parcial de caracteres prohibidos en los nombres de servidor Novell:

" \* + . / : ; < = >? \[ \] \\ \|

La versión de NWLink suministrada con el cliente 3,0 de MS admite el transporte **\_ IPX ncadg** .

las aplicaciones cliente de Windows de 16 bits que usan el transporte **\_ IPX ncadg** requieren que el archivo Nwipxspx.dll instalarse para ejecutarse en el subsistema wow. Póngase en contacto con Novell para obtener este archivo.

Para obtener las direcciones de red y nodo, use la utilidad **ComCheck** de Novell o la API **IPXGetInternetAddress** definida por Novell. En Windows, también puede obtener estas direcciones con el comando **ipxroute config** .

La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación IDL. El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.

> [!Note]  
> Esta familia de protocolos no se admite en Windows XP.

 

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ en \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ NSP**](ncacn-dnet-nsp.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ IPX**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**\_TCP NB \_ ncacn**](ncacn-nb-tcp.md)
</dt> <dt>

[**NP de ncacn \_**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ redes virtuales \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[enlace de cadenas](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 