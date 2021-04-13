---
description: Crea un objeto de datos. En desuso.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'IDirectXFileSaveObject:: CreateDataObject (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362534"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a>IDirectXFileSaveObject:: CreateDataObject (método)

Crea un objeto de datos. En desuso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rguidTemplate* \[ de\]
</dt> <dd>

Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID que representa la plantilla del objeto de datos.

</dd> <dt>

*szName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del objeto de datos. Especifique **null** si el objeto no tiene nombre.

</dd> <dt>

*pguid* \[ de\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* const**

Puntero a un GUID que representa el objeto de datos. Especifique **null** si el objeto no tiene un GUID.

</dd> <dt>

*cbSize* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamaño del objeto de datos, en bytes.

</dd> <dt>

*pvData* \[ de\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a un búfer que contiene todos los datos de miembro necesarios.

</dd> <dt>

*ppDataObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Dirección de un puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Observaciones

Si un objeto de referencia de datos hará referencia al objeto de datos, el parámetro szName o pguid no debe ser **null**.

Guarde las plantillas mediante el método [**IDirectXFileSaveObject:: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) antes de guardar los datos creados por este método. Guarde los datos creados mediante el método [**IDirectXFileSaveObject:: savedata**](idirectxfilesaveobject--savedata.md) .

Si necesita guardar datos opcionales, use el método [**IDirectXFileData:: AddDataObject**](idirectxfiledata--adddataobject.md) después de usar este método y antes de usar [**IDirectXFileSaveObject:: savedata**](idirectxfilesaveobject--savedata.md). Si el objeto tiene objetos secundarios, agréguelos antes de llamar a **IDirectXFileSaveObject:: savedata**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md)
</dt> <dt>

[**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
