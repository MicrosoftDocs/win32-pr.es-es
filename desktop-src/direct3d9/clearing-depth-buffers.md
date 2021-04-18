---
description: Muchas aplicaciones de C++ borran el búfer de profundidad antes de representar cada nuevo fotograma.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Borrar búferes de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714825"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Borrar búferes de profundidad (Direct3D 9)

Muchas aplicaciones de C++ borran el búfer de profundidad antes de representar cada nuevo fotograma. Puede borrar explícitamente el búfer de profundidad a través de Direct3D llamando a [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) y especificando D3DCLEAR \_ ZBUFFER para el parámetro flags. El método **IDirect3DDevice9:: Clear** permite especificar un valor de profundidad arbitrario en el parámetro Z.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
