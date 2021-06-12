---
description: Obtenga información Windows Installer conceptos que comienzan por la letra E, como el archivo de código fuente externo y con privilegios elevados.
ms.assetid: 8f180e2c-06f4-41d5-b167-52525f4a9985
title: E (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2c65c50427b1f8271be838971a387388ea53db
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011107"
---
# <a name="e-windows-installer"></a><span data-ttu-id="b5867-103">E (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="b5867-103">E (Windows Installer)</span></span>

<span data-ttu-id="b5867-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L M [N](m-gly.md) [O](o-gly.md) P [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="b5867-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b5867-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**Elevado**</span><span class="sxs-lookup"><span data-stu-id="b5867-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**elevated**</span></span>
</dt> <dd>

<span data-ttu-id="b5867-106">Las acciones realizadas con privilegios del sistema se denominan elevados.</span><span class="sxs-lookup"><span data-stu-id="b5867-106">Actions performed with system privileges are called elevated.</span></span>

</dd> <dt>

<span data-ttu-id="b5867-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**fase de ejecución**</span><span class="sxs-lookup"><span data-stu-id="b5867-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**execution phase**</span></span>
</dt> <dd>

<span data-ttu-id="b5867-108">Cuando el instalador ejecuta un script de acciones del instalador.</span><span class="sxs-lookup"><span data-stu-id="b5867-108">When the installer executes a script of installer actions.</span></span> <span data-ttu-id="b5867-109">En Microsoft Windows 2000, el servicio de instalador realiza este proceso.</span><span class="sxs-lookup"><span data-stu-id="b5867-109">In Microsoft Windows 2000, this process is performed by the installer service.</span></span> <span data-ttu-id="b5867-110">En una aplicación administrada, el script se ejecuta con privilegios del sistema.</span><span class="sxs-lookup"><span data-stu-id="b5867-110">In a managed application, the script is executed with system privileges.</span></span> <span data-ttu-id="b5867-111">Para obtener más información, vea [Mecanismo de instalación](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="b5867-111">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5867-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**script de ejecución**</span><span class="sxs-lookup"><span data-stu-id="b5867-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**execution script**</span></span>
</dt> <dd>

<span data-ttu-id="b5867-113">Acciones del instalador para una instalación.</span><span class="sxs-lookup"><span data-stu-id="b5867-113">Installer actions for an installation.</span></span> <span data-ttu-id="b5867-114">El script de ejecución se genera durante la fase [*de adquisición*](a-gly.md) de la instalación y se ejecuta durante la [*fase de ejecución.*](/windows)</span><span class="sxs-lookup"><span data-stu-id="b5867-114">The execution script is generated during the [*acquisition phase*](a-gly.md) of installation and executed during the [*execution phase*](/windows).</span></span> <span data-ttu-id="b5867-115">Para obtener más información, vea [Mecanismo de instalación](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="b5867-115">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5867-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**archivos de origen externos**</span><span class="sxs-lookup"><span data-stu-id="b5867-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**external source files**</span></span>
</dt> <dd>

<span data-ttu-id="b5867-117">Archivos de origen de la aplicación que se instala que se almacenan fuera del [*.msi archivo*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b5867-117">Source files of the application being installed that are stored outside of the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="b5867-118">Varios archivos de origen externos se pueden comprimir y almacenar juntos dentro de un [*archivo de archivador*](c-gly.md) incluido en el [*paquete*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b5867-118">Multiple external source files can be compressed and stored together inside of a [*cabinet file*](c-gly.md) included in the [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5867-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**interfaz de usuario externa**</span><span class="sxs-lookup"><span data-stu-id="b5867-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**external user interface**</span></span>
</dt> <dd>

<span data-ttu-id="b5867-120">Interfaz de usuario proporcionada por el autor de un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="b5867-120">UI provided by the author of an installation package.</span></span> <span data-ttu-id="b5867-121">No usa las funciones internas de la interfaz de usuario del instalador.</span><span class="sxs-lookup"><span data-stu-id="b5867-121">It does not use the internal UI capabilities of the installer.</span></span> <span data-ttu-id="b5867-122">Para obtener más información, [vea Acerca de la Interfaz de usuario](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b5867-122">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> </dl>

 

 
