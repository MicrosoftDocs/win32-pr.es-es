---
description: La aplicación implementa esta interfaz para guardar los datos de usuario adicionales insertados en los archivos. x.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interfaz ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670229"
---
# <a name="id3dxsaveuserdata-interface"></a>Interfaz ID3DXSaveUserData

La aplicación implementa esta interfaz para guardar los datos de usuario adicionales insertados en los archivos. x. Una instancia de esta interfaz se pasa a [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)y D3DX llama al método adecuado en esta interfaz cada vez que se encuentran los datos adecuados. Por ejemplo, para cada objeto Frame del archivo. x, se llama a [**ID3DXSaveUserData:: AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) y se pasan los datos secundarios.

## <a name="members"></a>Miembros

La interfaz **ID3DXSaveUserData** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSaveUserData** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXSaveUserData** tiene estos métodos.



| Método                                                                              | Descripción                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md)                   | Agregue datos secundarios al marco.<br/>                            |
| [**AddMeshChildData**](id3dxsaveuserdata--addmeshchilddata.md)                     | Agregue datos secundarios a la malla.<br/>                             |
| [**AddTopLevelDataObjectsPost**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | Agregue un objeto de nivel superior después de la jerarquía de fotogramas.<br/>       |
| [**AddTopLevelDataObjectsPre**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | Agregue un objeto de nivel superior antes de la jerarquía de fotogramas.<br/>      |
| [**RegisterTemplates**](id3dxsaveuserdata--registertemplates.md)                   | Una devolución de llamada para que el usuario registre una plantilla de archivo. x.<br/> |
| [**SaveTemplates**](id3dxsaveuserdata--savetemplates.md)                           | Una devolución de llamada para que el usuario guarde una plantilla de archivo. x.<br/>     |



 

## <a name="remarks"></a>Observaciones

El tipo LPD3DXSAVEUSERDATA se define como un puntero a esta interfaz.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
