---
description: Implemente la interfaz ISpecifyPropertyPages en el filtro como parte de la creación de una página de propiedades de filtro para un filtro DirectShow personalizado.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Paso 2. Implementación de ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2d1df86ef6e8b3e59f14a3efe1708a286761c9ba6425a7710a692ed6dcd3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951854"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Paso 2. Implementación de ISpecifyPropertyPages

A continuación, **implemente la interfaz ISpecifyPropertyPages** en el filtro. Esta interfaz tiene un único método, **GetPages**, que devuelve una matriz de CLID para las páginas de propiedades que admite el filtro. En este ejemplo, el filtro tiene una sola página de propiedades. Empiece por generar el CLSID y declararlo en el archivo de encabezado:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Ahora implemente **el método GetPages:**


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



Asigne memoria para la matriz **mediante CoTaskMemAlloc**. El autor de la llamada liberará la memoria.

Siguiente: [Paso 3. Compatibilidad con QueryInterface](step-3--support-queryinterface.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



