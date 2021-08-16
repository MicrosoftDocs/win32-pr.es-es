---
title: atributo pipe
description: El constructor de tipo de canalización permite transmitir un flujo de datos con tipo de extremo abierto a través de una llamada a procedimiento remoto.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- atributo de canalización MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c407bef0a9e610d21e7221eb9a06560f33300f4f1f388fa699ca9dfb18531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641958"
---
# <a name="pipe-attribute"></a>atributo pipe

El **constructor de** tipo de canalización permite transmitir un flujo de datos con tipo de extremo abierto a través de una llamada a procedimiento remoto.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*element-type* 
</dt> <dd>

Define el tamaño de un solo elemento en el búfer de transferencia. El *tipo de elemento puede* ser un tipo [base](midl-base-types.md), un tipo predefinido, una estructura , una \_ [**enumeración de 32b**](v1-enum.md)o un identificador de tipo. [](struct.md) Se aplican varias restricciones a *los tipos \_ de elementos*, como se describe en Comentarios, a continuación.

</dd> <dt>

*pipe-declarator* 
</dt> <dd>

Especifica uno o varios identificadores o punteros a identificadores. Separe varios declaradores con comas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede usar el constructor **de tipo de** canalización para transmitir datos en ambas direcciones. Un parámetro in pipe permite al servidor extraer el flujo de **\[** [](in.md) **\]** datos del cliente durante una llamada a procedimiento remoto. Un **\[** [**parámetro de**](out-idl.md) **\]** canalización de salida permite que el servidor vuelva a insertar el flujo de datos en el cliente. Las rutinas del lado cliente se suministran para insertar y extraer el flujo de datos y para asignar un búfer global para los datos. Las rutinas de código auxiliar de cliente y servidor serializan y desmarshaln los datos y pasan una referencia al búfer de vuelta a la aplicación.

Las restricciones siguientes se aplican a las canalizaciones:

-   Un elemento de canalización no puede ser ni contener un puntero, una matriz conforme o variable, un identificador o un identificador de contexto. Además, en la implementación de Canalizaciones de Microsoft, un elemento de canalización no puede ser ni contener una unión [**,**](union.md)una enumeración [**16b**](enum.md)o [**\_ \_ int3264**](--int3264.md).
-   No se puede aplicar **\[** [**la transmisión \_ como**](transmit-as.md), representar como , serialización de conexión o atributos de serialización de usuario a un tipo de canalización **\]** o al tipo **\[** [**\_**](represent-as.md) **\]** de **\[** [**\_**](wire-marshal.md) **\]** **\[** [**\_**](user-marshal.md) **\]** *elemento*.
-   Un tipo de canalización no puede ser miembro de una estructura o unión, el destino de un puntero o el tipo base de una matriz.
-   Un tipo de datos declarado como tipo de canalización solo se puede usar como parámetro de una llamada remota.
-   Puede pasar un parámetro de canalización en cualquier dirección por valor o por referencia **\[** [**(puntero ref).**](ref.md) **\]** Sin embargo, no se puede **\[** [**aplicar el atributo ptr**](ptr.md) **\]** a una canalización que se pasa por referencia. No se puede especificar un parámetro de canalización con un puntero **\[** [](unique.md) **\]** único o completo, independientemente de la dirección.
-   No se pueden usar canalizaciones en **\[** [**interfaces**](object.md) **\]** de objeto.
-   No se puede aplicar el **\[** [**atributo idempotente**](idempotent.md) **\]** a una rutina que tenga un parámetro de canalización.
-   No puede usar los atributos de serialización, **\[** [**codificar y**](encode.md) **\]** **\[** [**descodificar con**](decode.md) **\]** canalizaciones.
-   No se pueden usar identificadores automáticos, ya sea de forma predeterminada, o con el **\[** [**atributo de \_ identificador**](auto-handle.md) **\]** automático, con canalizaciones.

> [!Note]  
> El compilador MIDL solo admite [**canalizaciones en modo /Oif.**](-oi.md)

 

Para obtener más información sobre cómo implementar rutinas con parámetros de canalización, vea [Canalizaciones](/windows/desktop/Rpc/pipes) en la Guía y referencia del programador de RPC.

## <a name="examples"></a>Ejemplos

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**identificador \_ automático**](auto-handle.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**Decodificar**](decode.md)
</dt> <dt>

[**Codificar**](encode.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**Estructura**](struct.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**Único**](unique.md)
</dt> <dt>

[**serialización \_ de usuario**](user-marshal.md)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> </dl>

 

 