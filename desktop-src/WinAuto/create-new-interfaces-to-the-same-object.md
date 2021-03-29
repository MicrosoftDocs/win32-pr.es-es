---
title: Crear nuevas interfaces para el mismo objeto
description: Crear nuevas interfaces para el mismo objeto
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b641eed3918af3acbf399427ad5f7427112f399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665659"
---
# <a name="create-new-interfaces-to-the-same-object"></a><span data-ttu-id="f9f07-103">Crear nuevas interfaces para el mismo objeto</span><span class="sxs-lookup"><span data-stu-id="f9f07-103">Create New Interfaces to the Same Object</span></span>

<span data-ttu-id="f9f07-104">En este escenario, el servidor responde a cada solicitud [**de \_ cliente de OBJID**](object-identifiers.md) obteniendo un nuevo puntero de interfaz al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="f9f07-104">In this scenario, the server responds to each [**OBJID\_CLIENT**](object-identifiers.md) request by obtaining a new interface pointer to the same object.</span></span>

<span data-ttu-id="f9f07-105">En el código de ejemplo siguiente, *m \_ pUIObj* es un puntero a un objeto que admite más de una interfaz del modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="f9f07-105">In the following example code, *m\_pUIObj* is a pointer to an object that supports more than one Component Object Model (COM) interface.</span></span> <span data-ttu-id="f9f07-106">Aunque se reutiliza un objeto existente, se crea un nuevo puntero de interfaz cada vez que se recupera el objeto, por lo que se debe reducir el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="f9f07-106">Even though an existing object is reused, a new interface pointer is created each time the object is retrieved, so the reference count must be decremented.</span></span>


```C++
case WM_GETOBJECT:
   if ((DWORD)lParam == OBJID_CLIENT)
   {
      // Get a new interface to the same object. 
      IAccessible *pAcc = NULL;
      // The following increments the reference count. 
      m_pUIObj->QueryInterface(IID_IAccessible, (LPVOID*)&pAcc); 
      LRESULT lAcc = LresultFromObject(IID_IAccessible, wParam, 
            (LPUNKNOWN) &pAcc); 
      // Release our reference to the object.             
      pAcc->Release();               
      return lAcc;
   }
   break;  // Fall through to DefWindowProc. 
   
```



 

 




