---
title: Tipos de datos simples adsi (Iads.h)
description: Active Directory Interfaces de servicio (ADSI) define y usa los siguientes tipos de datos simples.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422fc0e20195e576f3ade8b39948992d61a376b58fd22f399ca1009db79cbdb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023703"
---
# <a name="adsi-simple-data-types"></a>Tipos de datos simples adsi

Active Directory Interfaces de servicio (ADSI) define y usa los siguientes tipos de datos simples.


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

**ADS \_ BOOLEAN**
</dt> <dd>

DWORD

</dd> <dt>

**CADENA \_ EXACTA DE \_ MAYÚSCULAS Y \_ MINÚSCULAS DE ANUNCIOS**
</dt> <dd>

LPWSTR

</dd> <dt>

**CADENA DE \_ OMITIR \_ MAYÚSCULAS Y MINÚSCULAS DE \_ ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ DN \_ STRING**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ INTEGER**
</dt> <dd>

DWORD

</dd> <dt>

**ADS \_ LARGE \_ INTEGER**
</dt> <dd>

[**ENTERO \_ GRANDE**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**CADENA \_ NUMÉRICA DE \_ ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ (CLASE DE \_ OBJETO)**
</dt> <dd>

LPWSTR

</dd> <dt>

**CADENA \_ IMPRIMIBLE DE \_ ANUNCIOS**
</dt> <dd>

LPWSTR

</dd> <dt>

**IDENTIFICADOR DE \_ BÚSQUEDA DE \_ ADS**
</dt> <dd>

HANDLE

</dd> <dt>

**HORA \_ UTC de \_ ADS**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando ADSI lee un atributo que se ha definido como **INTEGER** en el esquema LDAP, siempre controlará el entero como un valor de 32 bits y puede truncar los datos. Esto solo es un problema para los servidores LDAP que permiten valores enteros de tamaño arbitrario. Si el atributo es un atributo personalizado definido mediante la extensión del esquema, este problema se puede evitar definiendo el atributo personalizado como una cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                    |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl> |



 

