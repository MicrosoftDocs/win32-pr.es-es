---
title: Rutinas de comprobación personalizadas
description: En esta sección se describe cómo crear una rutina de comprobación personalizada para la herramienta Comprobador de accesibilidad de la interfaz de usuario (AccChecker).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245865a0ab4aa6848d4a4361a30febbb341742208586ebf4ec5b35c34fa30534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030894"
---
# <a name="custom-verification-routines"></a>Rutinas de comprobación personalizadas

En esta sección se describe cómo crear una rutina de comprobación personalizada para la herramienta Comprobador de accesibilidad de la interfaz de usuario (AccChecker).

-   [Creación de una comprobación personalizada](#creating-a-custom-verification)
    -   [Comprobación personalizada de ejemplo](#sample-custom-verification)
-   [Uso de una comprobación personalizada](#using-a-custom-verification)
    -   [El gráfico accChecker Interfaz de usuario (GUI)](#the-accchecker-graphical-user-interface-gui)
    -   [Automatización de AccChecker](#accchecker-automation)
-   [Temas relacionados](#related-topics)

Ui Accessibility Checker (AccChecker) es una herramienta de prueba de accesibilidad diseñada para comprobar la implementación de Microsoft Active Accessibility (MSAA) en una interfaz de usuario de control o aplicación. Los problemas de accesibilidad de alto impacto que podrían exponerse mediante la implementación de MSAA se prueban con un conjunto de rutinas de verificación automatizadas integradas. Estas rutinas de verificación nativas se pueden aumentar con rutinas personalizadas mediante la plataforma extensible AccChecker.

## <a name="creating-a-custom-verification"></a>Creación de una comprobación personalizada

Una comprobación personalizada se basa en una biblioteca de clases (DLL) que implementa una única interfaz ( ) que `IVerificationRoutine` contiene un miembro ( `Execute` ):


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**Parámetros**

*Hwnd*

Tipo: **System.IntPtr**

HWND del elemento que se está verificando.

*Registrador*

Tipo: **AccCheck.Logging.ILogger**

Método de registro seleccionado. Entre los tipos posibles se incluyen **AccumulatingLogger** (usado por AccChecker para almacenar en caché todas las entradas de registro hasta que se completen las comprobaciones), **ConsoleLogger**, **TextFileLogger** y **XMLSerializingLogger.**

*AllowUI*

Tipo: **bool**

Indica si la rutina de comprobación muestra la interfaz de usuario que está probando. Por lo general, se establece en false en escenarios de pruebas automatizadas.

*elementos gráficos*

Tipo: **AccCheck.GraphicsHelper**

Se usa para capturas de pantalla y otras visualizaciones en AccChecker.

### <a name="sample-custom-verification"></a>Comprobación personalizada de ejemplo

El ejemplo siguiente es una comprobación personalizada de C# que realiza una comprobación de profundidad de árbol de elementos simple. Se registra un error si el árbol de elementos tiene más de 50 niveles de profundidad, se registra una advertencia si el árbol de elementos tiene entre 20 y 50 niveles de profundidad y se registra un mensaje informativo en caso contrario.


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> Se incluye Microsoft Visual Studio solución que contiene código de ejemplo de comprobación con la documentación de ayuda. Los archivos se encuentran en la ruta de instalación de AccChecker.

 

## <a name="using-a-custom-verification"></a>Uso de una comprobación personalizada

En esta sección se describe cómo incorporar una comprobación personalizada en escenarios de prueba de AccChecker.

### <a name="the-accchecker-graphical-user-interface-gui"></a>El gráfico accChecker Interfaz de usuario (GUI)

Para incluir una rutina de comprobación personalizada en la aplicación AccChecker, simplemente haga clic en Abrir DLL en el menú Archivo y busque el archivo DLL de la rutina. La rutina personalizada se agregará a la parte inferior de la lista de comprobaciones en el panel Seleccionar rutinas de verificación.

En la siguiente captura de pantalla se muestra la comprobación personalizada sample check tree depth agregada a AccChecker.

![sample check tree depth custom verification routine added to the accchecker ui (Rutina de comprobación personalizada de profundidad de árbol de comprobación de ejemplo agregada a la interfaz de usuario del corrector)](images/accchecker-sample-custom-verification.png)

> [!Note]  
> Si los valores de atributo de comprobación no se especifican en la rutina de comprobación personalizada, la comprobación se sigue cargando en AccChecker aunque no aparezca en la interfaz de usuario. Puesto que no se muestra en la interfaz de usuario, no se puede desactivar ni excluir de las ejecuciones de comprobación posteriores.

 

### <a name="accchecker-automation"></a>Automatización de AccChecker

La incorporación de una rutina de verificación personalizada en un marco de AccChecker automatizado es tan simple como agregar el archivo DLL de verificación y habilitar las rutinas de verificación deseadas.

El siguiente fragmento de código muestra cómo usar la API AccChecker para probar la funcionalidad de tabulación en la Windows panel de control firewall.


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;

public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> Se incluye Microsoft Visual Studio solución de 2008 que contiene código de ejemplo de comprobación con la documentación de ayuda. Los archivos se encuentran en la ruta de instalación de AccChecker.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




