---
description: Crea una diferencia entre el origen y el destino (proporcionados como búferes) y devuelve la diferencia de salida como búfer asignado por MSDelta.
title: Función CreateDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: ae13dfb82d4699bbb8cc222b4cd1aaa2615e8efaa578de60483f00552faf2086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826929"
---
# <a name="createdeltab-function"></a>Función CreateDeltaB

Crea una diferencia entre el origen y el destino (proporcionados como búferes) y devuelve la diferencia de salida como búfer asignado por MSDelta.

> [!NOTE]
> Debe llamar a [DeltaFree para](msdelta-deltafree.md) liberar el búfer de salida una vez completada esta función.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a>Parámetros

*FileTypeSet*

[in] Valor [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) que indica el tipo de archivo establecido que se va a usar para el proceso de creación.

*SetFlags*

[in] Uno o varios [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especifican las marcas que se usarán durante el proceso de creación, además de las marcas predeterminadas.

*ResetFlags*

[in] Uno o varios valores [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especifican las marcas predeterminadas que se restablecerán durante el proceso de creación.

*Origen*

[in] Estructura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contiene un puntero al búfer que contiene los datos de origen.

*Target*

[in] Estructura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contiene un puntero al búfer que contiene los datos de destino.

*SourceOptions*

[in] Reservado. Pase una [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *editable* establecido en **FALSE,** *lpStart* establecido en **NULL** y *uSize* establecido en 0.

*TargetOptions*

[in] Reservado. Pase una [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *editable* establecido en **FALSE,** *lpStart* establecido en **NULL** y *uSize* establecido en 0.

*GlobalOptions*

[in] Reservado. Pase una [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *lpStart* establecido en **NULL** y *uSize* establecido en 0.

*lpTargetFileTime*

[in] Marca de tiempo establecida en el archivo de destino después de aplicar la diferencia. Si **es NULL,** la marca de tiempo de destino será la hora actual durante el proceso de creación.

*HashAlgId*

[in] ALG_ID del algoritmo que se va a usar para generar la firma de destino. Algunos valores especiales son:

- 0 = Sin firma
- 32 = CRC de 32 bits definido en msdelta.dll

*lpDelta*

[out] Puntero a la [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) estructura donde se va a escribir la diferencia.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE** si se realiza correctamente; de lo contrario, devuelve **FALSE**. Cuando la función devuelve **FALSE,** puede llamar a [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el código de error del sistema Win32 correspondiente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Encabezado | msdelta.h |
| Archivo DLL | msdelta.dll |
| Unicode | No aplicable |

## <a name="see-also"></a>Consulte también

[MSDelta](msdelta.md)

[DeltaFree](msdelta-deltafree.md)
