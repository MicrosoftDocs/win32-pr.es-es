---
description: El formato de disco duro virtual (VHD) es una especificación de formato de imagen disponible públicamente que permite la encapsulación del disco duro en un archivo individual para que lo use el sistema operativo como un disco virtual en el mismo modo en que se usan los discos duros físicos.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Acerca de VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809793"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>Acerca de VHD

El formato de disco duro virtual (VHD) es una [especificación](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) de formato de imagen disponible públicamente que permite la encapsulación del disco duro en un archivo individual para que lo use el sistema operativo como un *disco virtual* en el mismo modo en que se usan los discos duros físicos. Estos discos virtuales pueden hospedar sistemas de archivos nativos (NTFS, FAT, exFAT y UDF) mientras se admiten operaciones de archivos y discos estándar. La compatibilidad con la API de VHD permite la administración de los discos virtuales. Los discos virtuales creados con la API de VHD pueden funcionar como discos de arranque.

Un ejemplo de cómo se usan los archivos VHD es la característica [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) de Windows 7, windows Server 2008, Virtual Server y Windows Virtual PC. Estos productos usan la API de VHD para contener la imagen de sistema operativo Windows utilizada por una máquina virtual como disco de arranque del sistema.

El kit de desarrollo de software (SDK) de Microsoft Windows integra compatibilidad nativa con VHD para trabajar con discos virtuales, lo que facilita a los desarrolladores y administradores la creación, administración e implementación de imágenes de Windows en archivos VHD mediante la compatibilidad de la API de la plataforma o las herramientas de administración. No es necesario instalar aplicaciones independientes ni implementar un analizador de formato VHD para habilitar estas operaciones. Estas API permiten el uso genérico de discos virtuales independientemente de cualquier otra tecnología de virtualización.

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminología

El término *memoria auxiliar* se usa para hacer referencia al archivo físico que existe en el disco duro real. La memoria auxiliar se representa mediante un *archivo de imagen de disco duro virtual*.

Los términos *Dynamic*, *Expandable* y *Sparse* suelen usarse indistintamente al hacer referencia a discos virtuales expansibles dinámicamente. En el caso de la tecnología de VHD, estos términos son idénticos.

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Información general sobre las características del sistema VHD

En el diagrama siguiente se presenta información general sobre las características de VHD y sus relaciones.

![diagrama de bloque de VHD](images/vhd.png)

A continuación se ofrece una explicación resumida de las características descritas anteriormente.

API nativas de Windows en modo usuario:

-   VirtDisk.dll: biblioteca común para las API de administración de VHD.

Contenedores de administración específicos de dominio en modo de usuario:

-   [API de VHD de VDS](/windows/desktop/VDS/about-vds) : contenedores del modelo de objetos VDS para las API de Windows de VHD.

Controladores de modo kernel:

-   VDrvRoot.sys enumerador de unidad virtual raíz.
-   FsDepends.sys: administración de dependencias de volumen anidada.
-   Vhdmp.sys: el proveedor de propiedades de dependencia y el analizador de VHD.

La documentación del SDK de esta sección trata las API de VHD nativas de Windows en modo de usuario.

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Tipos de discos virtuales

Existen consideraciones para el uso de discos virtuales y los tipos de discos virtuales disponibles:

-   **Corrección**: el archivo de imagen de disco duro virtual se ha asignado previamente en la memoria auxiliar para el tamaño máximo solicitado.
-   **Expandible**: también conocido como "dinámico", "dinámicamente expansible" y "disperso", el archivo de imagen de VHD usa solo tanto espacio en la memoria auxiliar como sea necesario para almacenar los datos reales que contiene actualmente el disco virtual. Al crear este tipo de disco virtual, la API de VHD no comprueba el espacio disponible en el disco físico en función del tamaño máximo solicitado, por lo que es posible crear correctamente un disco virtual dinámico con un tamaño máximo mayor que el espacio disponible en disco físico. Para obtener más información, vea [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).
    **Nota:**  El tamaño máximo de un disco virtual dinámico es de 2.040 GB.

     

-   **Diferencia**: se usa un disco virtual primario como base de este tipo, con las escrituras posteriores escritas en el disco virtual como diferencias con el nuevo archivo de imagen de VHD de diferenciación y el archivo de imagen de VHD primario no se modifica. Por ejemplo, si tiene un disco virtual del sistema operativo de arranque del sistema de instalación limpia como principal y designa el disco virtual de diferenciación como el disco virtual actual que el sistema debe usar, el sistema operativo del disco virtual primario permanece en su estado original para una recuperación rápida o para crear rápidamente más imágenes de arranque basadas en discos virtuales de diferenciación adicionales. Para obtener más información, vea [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).
    **Nota:**  El tamaño máximo de un disco virtual de diferenciación es de 2.040 GB.

     

Todos los tipos de discos virtuales tienen un tamaño mínimo de 3 MB.

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Temas relacionados

[Acerca de VDS](/windows/desktop/VDS/about-vds)

[Referencia de VHD](vhd-reference.md)

[Especificación de formato de imagen de disco duro virtual](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
