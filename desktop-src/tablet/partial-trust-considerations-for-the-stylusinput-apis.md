---
description: Información general sobre los problemas de confianza parcial y la interfaz de programación de aplicaciones (API) de StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Consideraciones de confianza parcial para la API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278009"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Consideraciones de confianza parcial para la API de StylusInput

El [**RealTimeStylus**](realtimestylus-class.md) que toma el parámetro *Handle* requiere los permisos [UIPermissionWindow. allcargador](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) , además de los permisos requeridos por el constructor que toma el parámetro *attachedControl* .

Para obtener más información acerca de los problemas de seguridad y confianza, consulte [seguridad y confianza](security-and-trust.md).

 

 
