---
description: Puede usar la biblioteca de tipos de scripting wmi para llamar a métodos de WMI Scripting API desde Microsoft Visual Studio y en archivos WSF Windows host de script.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Uso de la biblioteca de tipos de scripting wmi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20e5a2aa10bccfbd91b003f1db120691b6c61bb4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881181"
---
# <a name="using-the-wmi-scripting-type-library"></a>Uso de la biblioteca de tipos de scripting wmi

Puede usar la biblioteca de tipos de scripting wmi para llamar a métodos de WMI Scripting API desde Microsoft Visual Studio y en archivos WSF Windows host de script.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Uso de la biblioteca de tipos de scripting wmi con Microsoft Visual Studio

> [!Note]  
> Las características de Visual InterDev 6.0 se han integrado [en Microsoft Visual Studio .NET.](https://msdn.microsoft.com/vstudio/default.aspx)

 

En el procedimiento siguiente se describe cómo habilitar el entorno de desarrollo integrado (IDE) para que tenga en cuenta la biblioteca de tipos WbemScripting.

**Para agregar la biblioteca de tipos de scripting WMI a las referencias del proyecto**

1.  Seleccione **Agregar referencias** en el **Project** menú.
2.  En la pestaña COM del cuadro **Agregar referencia,** seleccione Biblioteca de scripting V1.2 wmi de Microsoft.
3.  Si no aparece ninguna opción adecuada en la lista Referencias, agrégrela mediante **Examinar en** el **cuadro** Referencias. El **cuadro** Examinar abre **un cuadro Agregar** referencia que le permite buscar la biblioteca de tipos WbemScripting.

    La biblioteca de tipos WbemScripting reside en el archivo Wbemdisp.tlb del directorio %windir% \\ System32 \\ Wbem.

4.  Seleccione el archivo y haga clic en **Abrir**. Microsoft WMI Scripting V1.2 Library aparece en la lista de referencias. Asegúrese de seleccionar el cuadro situado junto a este elemento en la lista.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>Uso de la biblioteca de tipos de scripting wmi Windows host de script 2.0

Puede incluir la referencia a **WbemScripting.SWbemLocator** en un archivo WSF del host de script de Windows, a diferencia de un script escrito en Visual Basic, Scripting Edition u otros lenguajes de scripting. Esto le permite usar nombres constantes en lugar de valores. Por ejemplo, use **WbemAuthenticationLevelPktPrivacy en** lugar del valor 6 al establecer la autenticación.

Los scripts pueden conectarse con la API de scripting para la biblioteca de tipos WMI mediante los métodos siguientes:

-   Especificar el GUID wbemScripting en los métodos [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) y [**GetObject de**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)VBScript.

    Esto alerta Windows host de script para conectarse al conjunto de objetos WMI.

    En el ejemplo de código de VBScript siguiente se crea [**un nuevo objeto SWbemDateTime.**](swbemdatetime.md)

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Usar la [cadena de Moniker](constructing-a-moniker-string.md) "winmgmts:" al obtener un objeto nuevo o existente.

    En el ejemplo de código de VBScript siguiente se usa el moniker "winmgmts:" para obtener la instancia de [**Proceso de \_ Win32**](/windows/desktop/CIMWin32Prov/win32-process) con una propiedad **Handle** de 0 (cero). **Handle** es la propiedad clave de esta clase.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Hacer referencia a la biblioteca de tipos WMI mediante la etiqueta de referencia del formato de archivo &lt; &gt; XML WSH 2.0. Si usa la etiqueta de referencia, la etiqueta debe tener un atributo uuid cuyo valor sea el GUID de la biblioteca de tipos &lt; &gt; WMI o (recomendado)   un atributo de objeto cuyo valor sea el **PROGID** de cualquiera de los objetos de scripting wmi que puede crear.

    En el ejemplo de código de VBScript siguiente se usa el PROGID de "WbemScripting". Para ejecutar el script, guarde el texto en un archivo con una extensión .wsf.

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   Usar un objeto <**etiqueta>** para crear un objeto de scripting WMI. Puede especificar el atributo **id** con el valor de un nombre que haga referencia al objeto de scripting WMI que desea crear y el atributo **progid** igual al PROID del objeto de scripting WMI.

    El siguiente script WSH muestra el nombre de host y el número de procesadores en el equipo local. Para ejecutar el script, guarde el texto en un archivo con una extensión .wsf.

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[API de scripting para WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
