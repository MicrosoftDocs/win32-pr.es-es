---
description: Devuelve un identificador para el hash del Protocolo de enlace.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Función SslHashHandshake (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002683"
---
# <a name="sslhashhandshake-function"></a>SslHashHandshake función)

La función **SslHashHandshake** devuelve un identificador para el hash del Protocolo de enlace.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSslProvider* \[ de\]
</dt> <dd>

Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hHandshakeHash* \[ in, out\]
</dt> <dd>

Identificador del objeto hash.

</dd> <dt>

*pbInput* \[ enuncia\]
</dt> <dd>

Dirección de un búfer que contiene los datos a los que se va a aplicar un algoritmo hash.

</dd> <dt>

*cbInput* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer *pbInput* .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro se reserva para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve cero.

## <a name="remarks"></a>Observaciones

La función **SslHashHandshake** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.

1.  Se llama a la función [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) para obtener un identificador hash.
2.  A la función **SslHashHandshake** se le llama cualquier número de veces con el identificador hash para agregar datos al hash.
3.  Se llama a la función [**SslComputeFinishedHash**](sslcomputefinishedhash.md) con el identificador hash para obtener el Resumen de los datos con hash.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

