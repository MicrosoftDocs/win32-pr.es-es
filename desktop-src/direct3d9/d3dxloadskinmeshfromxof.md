---
description: Carga una malla de máscara desde un objeto de datos de archivo de DirectX. x.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: Función D3DXLoadSkinMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820954"
---
# <a name="d3dxloadskinmeshfromxof-function"></a>D3DXLoadSkinMeshFromXof función)

Carga una malla de máscara desde un objeto de datos de archivo de DirectX. x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pxofMesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Puntero a una interfaz [**ID3DXFileData**](id3dxfiledata.md) que representa el objeto de datos de archivo que se va a cargar.

</dd> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas, de la enumeración [**D3DXMESH**](./d3dxmesh.md) , que especifica las opciones de creación para la malla.

</dd> <dt>

*pD3DDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.

</dd> <dt>

*ppAdjacency* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) . Cuando este método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.

</dd> <dt>

*ppMaterials* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) . Cuando el método finaliza, este parámetro se rellena con una matriz de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) .

</dd> <dt>

*ppEffectInstances* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero a un búfer que contiene una matriz de instancias de efecto, una por cada grupo de atributos de la malla devuelta. Una instancia de efecto es una instancia concreta de la información de estado que se usa para inicializar un efecto. Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pMatOut* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero al número de estructuras [**D3DXMATERIAL**](d3dxmaterial.md) en la matriz *ppMaterials* , cuando el método devuelve.

</dd> <dt>

*ppSkinInfo* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Dirección de un puntero a una interfaz [**ID3DXSkinInfo**](id3dxskininfo.md) , que representa la información de la piel.

</dd> <dt>

*ppMesh* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) , que representa la malla cargada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY

## <a name="remarks"></a>Observaciones

Este método toma un puntero a un objeto interno en el archivo. x, lo que le permite cargar la jerarquía de fotogramas.

En el caso de los archivos de malla que no contengan información de instancia de efecto, se generarán instancias de efectos predeterminados a partir de la información de material del archivo. x. Una instancia de efecto predeterminado tendrá valores predeterminados que corresponden a los miembros de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) .

El nombre de textura predeterminado también se rellena, pero se trata de forma diferente. El nombre será Texture0@Name , que corresponde a una variable de efecto por el nombre de "Texture0" con una anotación denominada "nombre". Esto contendrá el nombre del archivo de cadena para la textura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
