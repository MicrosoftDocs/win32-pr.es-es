---
description: El método FindMediaFile busca un archivo y, si se realiza correctamente, recupera la ruta de acceso al archivo.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'IMediaLocator:: FindMediaFile (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679068"
---
# <a name="imedialocatorfindmediafile-method"></a>IMediaLocator:: FindMediaFile (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `FindMediaFile` método busca un archivo y, si se realiza correctamente, recupera la ruta de acceso al archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Entrada* 
</dt> <dd>

Nombre de archivo, incluida la ruta de acceso, donde se conocía por última vez el archivo. Para los objetos de origen de la escala de tiempo, use el nombre del medio actual.

</dd> <dt>

*FilterString* 
</dt> <dd>

**BSTR** que contiene pares de cadenas de filtro, con el formato que requiere el miembro **lpstrFilter** de la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . El localizador de medios usa este filtro si muestra un cuadro de diálogo Abrir archivo. El valor puede ser **null** si el parámetro *Flags* no incluye la \_ \_ marca emergente SFN VALIDATEF.

</dd> <dt>

*pOutput* 
</dt> <dd>

Puntero a una variable que recibe la ruta de acceso real al archivo, si difiere del valor contenido en la *entrada* y si el método localiza correctamente el archivo.

</dd> <dt>

*Marcas* 
</dt> <dd>

Combinación bit a bit de cero o más marcadores. Para obtener una lista de posibles marcas, vea [**marcas de validación de nombre de archivo**](file-name-validation-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La cadena de filtro para el cuadro de diálogo Abrir archivo, que se especifica mediante el parámetro *FilterString* , contiene caracteres nulos internos. Por ejemplo, \\ el vídeo 0 \* . avi \\ 0 \\ 0 es una cadena de filtro válida. No se puede usar la función **SysAllocStr** para asignar el BSTR, porque esa función espera una cadena terminada en NULL y truncará la cadena en el primer carácter nulo. Por lo tanto, use una función como **SysAllocStringLen**, que incluye un parámetro explícito para la longitud:


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



Si el usuario cancela el cuadro de diálogo Abrir archivo, el método devuelve E \_ Fail.

El método asigna memoria para el **BSTR** en *pOutput*. La aplicación debe llamar a **SysFreeString** para liberar memoria.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IMediaLocator**](imedialocator.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 
