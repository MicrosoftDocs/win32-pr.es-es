---
description: Implementa la interfaz IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Clase InkDesktopHost
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105721319"
---
# <a name="inkdesktophost-class"></a><span data-ttu-id="70c7d-103">Clase InkDesktopHost</span><span class="sxs-lookup"><span data-stu-id="70c7d-103">InkDesktopHost class</span></span>

<span data-ttu-id="70c7d-104">Implementa la interfaz [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .</span><span class="sxs-lookup"><span data-stu-id="70c7d-104">Implements the [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) interface.</span></span>

<span data-ttu-id="70c7d-105">Un objeto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) habilita la entrada de lápiz, el procesamiento y la representación a través de la creación de un subproceso de aplicación para hospedar un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e insertarlo en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="70c7d-105">An [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) object enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

## <a name="members"></a><span data-ttu-id="70c7d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="70c7d-106">Members</span></span>

<span data-ttu-id="70c7d-107">La clase **InkDesktopHost** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="70c7d-107">The **InkDesktopHost** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="70c7d-108">**InkDesktopHost** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="70c7d-108">**InkDesktopHost** also has these types of members:</span></span>

- [<span data-ttu-id="70c7d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="70c7d-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70c7d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="70c7d-110">Methods</span></span>

<span data-ttu-id="70c7d-111">La clase **InkDesktopHost** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="70c7d-111">The **InkDesktopHost** class has these methods.</span></span>

| <span data-ttu-id="70c7d-112">Método</span><span class="sxs-lookup"><span data-stu-id="70c7d-112">Method</span></span> | <span data-ttu-id="70c7d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="70c7d-113">Description</span></span> |
|---|---|
| [<span data-ttu-id="70c7d-114">**CreateAndInitializeInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="70c7d-114">**CreateAndInitializeInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | <span data-ttu-id="70c7d-115">Crea un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) en un subproceso de aplicación, lo conecta al árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación y establece el tamaño del objeto.</span><span class="sxs-lookup"><span data-stu-id="70c7d-115">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread, connects it to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree, and sets the size of the object.</span></span><br/> |
| [<span data-ttu-id="70c7d-116">**CreateInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="70c7d-116">**CreateInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | <span data-ttu-id="70c7d-117">Crea un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) en un subproceso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="70c7d-117">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread.</span></span><br/> |
| [<span data-ttu-id="70c7d-118">**QueueWorkItem**</span><span class="sxs-lookup"><span data-stu-id="70c7d-118">**QueueWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | <span data-ttu-id="70c7d-119">Agregue una operación de entrada manuscrita a una cola de trabajo para su ejecución en el subproceso **InkDesktopHost** .</span><span class="sxs-lookup"><span data-stu-id="70c7d-119">Add an ink operation to a work queue for execution on the **InkDesktopHost** thread.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="70c7d-120">Funciones de acceso de creación \\</span><span class="sxs-lookup"><span data-stu-id="70c7d-120">Creation\\Access Functions</span></span>

<span data-ttu-id="70c7d-121">Llame a [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase <strong>InkDesktopHost</strong> para recuperar una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="70c7d-121">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkDesktopHost</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a><span data-ttu-id="70c7d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70c7d-122">Requirements</span></span>

| <span data-ttu-id="70c7d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c7d-123">Requirement</span></span> | <span data-ttu-id="70c7d-124">Value</span><span class="sxs-lookup"><span data-stu-id="70c7d-124">Value</span></span> |
|---|---|
| <span data-ttu-id="70c7d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70c7d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="70c7d-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="70c7d-126">Windows 10 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="70c7d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70c7d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="70c7d-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="70c7d-128">None supported</span></span><br/> |
| <span data-ttu-id="70c7d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70c7d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c7d-130"><dt>InkPresenterDesktop. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c7d-130"><dt>InkPresenterDesktop.h</dt></span></span> </dl>   |
| <span data-ttu-id="70c7d-131">IDL</span><span class="sxs-lookup"><span data-stu-id="70c7d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70c7d-132"><dt>InkPresenterDesktop. idl</dt></span><span class="sxs-lookup"><span data-stu-id="70c7d-132"><dt>InkPresenterDesktop.idl</dt></span></span> </dl> |
| <span data-ttu-id="70c7d-133">IID</span><span class="sxs-lookup"><span data-stu-id="70c7d-133">IID</span></span><br/>                      | <span data-ttu-id="70c7d-134">IID \_ IInkDesktopHost se define como 4ce7d875-a981-4140-a1ff-ad93258e8d59</span><span class="sxs-lookup"><span data-stu-id="70c7d-134">IID\_IInkDesktopHost is defined as 4ce7d875-a981-4140-a1ff-ad93258e8d59</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="70c7d-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70c7d-135">Related topics</span></span>

<span data-ttu-id="70c7d-136">[Clases de presentador de tinta](ink-presenter-classes.md), [interacciones de lápiz y lápiz](/windows/uwp/design/input/pen-and-stylus-interactions), [ejemplo de análisis de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de tinta [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="70c7d-136">[Ink presenter classes](ink-presenter-classes.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
