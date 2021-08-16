---
description: Al igual que con otros lenguajes como PowerShell, VBScript o C++, puede usar C# para supervisar de forma remota el hardware y el software en equipos remotos.
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 'Conexión a WMI de forma remota con C #'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9ed735a1440d124a065a9f509eac7c58b1fded9be0683e361903b9f02fc1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319443"
---
# <a name="connecting-to-wmi-remotely-with-c"></a>Conexión a WMI de forma remota con C #

Al igual que con otros lenguajes como PowerShell, VBScript o C++, puede usar C# para supervisar de forma remota el hardware y el software en equipos remotos. Las conexiones remotas para código administrado se logran a través del espacio [de nombres Microsoft.Management.Infrastructure.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) (Las versiones anteriores de WMI usaban [el espacio de nombres System.Management,](/dotnet/api/system.management) que se incluye aquí para mayor integridad).

> [!Note]  
> **System.Management era el** espacio de nombres original de .NET que se usaba para tener acceso a WMI; Sin embargo, las API de este espacio de nombres suelen ser más lentas y no escalan tan bien en relación con sus homólogos **microsoft.management.infrastructure** más modernos.

 

La conexión remota mediante clases en el espacio [de nombres Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) usa DCOM como mecanismo remoto subyacente. Las conexiones WMI remotas se deben ajustar a los requisitos de seguridad de DCOM en lo que respecta a la suplantación y la autenticación. De forma predeterminada, un ámbito está enlazado al equipo local y al espacio de nombres del sistema \\ "ROOT CIMv2". Sin embargo, puede cambiar el equipo, el dominio y el espacio de nombres WMI a los que tiene acceso. También puede establecer la autoridad, la suplantación, las credenciales y otras opciones de conexión.

**Para conectarse a WMI de forma remota con C# (Microsoft.Management.Infrastructure)**

1.  Cree una sesión en el equipo remoto con una llamada a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).

    Si se conecta a un equipo remoto con las mismas credenciales (dominio y nombre de usuario) con las que ha iniciado sesión, puede especificar el nombre del equipo en la llamada [a](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) Crear. Una vez que haya devuelto [el objeto CimSession,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) puede realizar la consulta WMI.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    Para obtener más información sobre cómo realizar consultas WMI con la API **Microsoft.Management.Infrastructure** en C#, vea Recuperar datos de instancia o [clase WMI.](retrieving-class-or-instance-data.md)

2.  Si desea establecer diferentes opciones para la conexión, como diferentes credenciales, configuración regional o niveles de suplantación, debe usar un objeto [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) en la llamada a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).

    [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) es una clase base para [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) y [DComSessionOptions.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) Puede usar cualquiera de las opciones para establecer las opciones en las sesiones WS-Man y DCOM, respectivamente. En el ejemplo de código siguiente se describe el uso de un [objeto DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) para establecer el nivel de suplantación en Suplantar.

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  Si desea establecer las credenciales de la conexión, deberá crear y agregar un objeto [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) a [CimSessionOptions.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))

    En el ejemplo de código siguiente se describe cómo crear una clase [WSManSessionOptions,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) rellenarla con el [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))adecuado y usarlo en una [llamada a CimSession.Create.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))

    ```CSharp
    string computer = “Computer_B”;
    string domain = “Domain1″;
    string username = “User1″;

    string plaintextpassword; 

    //Retrieve password from the user. 
    //For the complete code, see the sample at the bottom of this topic.

    CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, domain, username, securepassword); 

    WSManSessionOptions SessionOptions = new WSManSessionOptions();
    SessionOptions.AddDestinationCredentials(Credentials); 

    CimSession Session = CimSession.Create(computer, SessionOptions);
    ```

    

    Por lo general, se recomienda no codificar de forma segura una contraseña en las aplicaciones. Como indica el ejemplo de código anterior, siempre que sea posible, intente consultar la contraseña al usuario y almacenarla de forma segura.

WMI está diseñado para supervisar el hardware y el software en equipos remotos. Las conexiones remotas para WMI v1 se logran a través del [objeto ManagementScope.](/dotnet/api/system.management.managementscope)

**Para conectarse a WMI de forma remota con C# (System.Management)**

1.  Cree un [objeto ManagementScope,](/dotnet/api/system.management.managementscope) con el nombre del equipo y la ruta de acceso WMI, y conéctese al destino con una llamada a ManagementScope. Conectar().

    Si se conecta a un equipo remoto con las mismas credenciales (dominio y nombre de usuario) con las que ha iniciado sesión, solo tiene que especificar la ruta de acceso de WMI. Una vez que se haya conectado, puede realizar la consulta WMI.

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    Para obtener más información sobre cómo realizar consultas WMI con la API [System.Management](/dotnet/api/system.management) en C#, vea Recuperar datos de instancia [o clase WMI.](retrieving-class-or-instance-data.md)

2.  Si se conecta a un equipo remoto en un dominio diferente o con un nombre de usuario y una contraseña diferentes, debe usar un objeto [ConnectionOptions](/dotnet/api/system.management.connectionoptions) en la llamada a [ManagementScope](/dotnet/api/system.management.managementscope).

    [ConnectionOptions contiene propiedades](/dotnet/api/system.management.connectionoptions) para describir las opciones de autenticación, suplantación, nombre de usuario, contraseña y otras opciones de conexión. En el ejemplo de código siguiente se describe el uso [de ConnectionOptions para](/dotnet/api/system.management.connectionoptions) establecer el nivel de suplantación en Suplantar.

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    Por lo general, se recomienda establecer el nivel de suplantación en Suplantar a menos que se necesite explícitamente lo contrario. Además, intente evitar escribir su nombre y contraseña en código de C#. (Si es posible, vea si puede consultar al usuario para proporcionarlos dinámicamente en tiempo de ejecución).

    Para obtener más ejemplos de cómo establecer diferentes propiedades en una conexión WMI remota, vea la sección Ejemplos de la [página de referencia ConnectionOptions.](/dotnet/api/system.management.connectionoptions)

## <a name="microsoftmanagementinfrastructure-example"></a>Ejemplo de Microsoft.Management.Infrastructure

En el siguiente ejemplo de código de C#, basado en la siguiente entrada de blog en [TechNet,](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage)se describe cómo usar [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) y [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) para establecer credenciales en una conexión remota.


```CSharp
using System;
using System.Text;
using System.Threading;
using Microsoft.Management.Infrastructure;
using Microsoft.Management.Infrastructure.Options;
using System.Security; 

namespace SMAPIQuery
{
    class Program
    {
        static void Main(string[] args)
        { 

            string computer = "Computer_B";
            string domain = "DOMAIN";
            string username = "AdminUserName";


            string plaintextpassword; 

            Console.WriteLine("Enter password:");
            plaintextpassword = Console.ReadLine(); 

            SecureString securepassword = new SecureString();
            foreach (char c in plaintextpassword)
            {
                securepassword.AppendChar(c);
            } 

            // create Credentials
            CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, 
                                                          domain, 
                                                          username, 
                                                          securepassword); 

            // create SessionOptions using Credentials
            WSManSessionOptions SessionOptions = new WSManSessionOptions();
            SessionOptions.AddDestinationCredentials(Credentials); 

            // create Session using computer, SessionOptions
            CimSession Session = CimSession.Create(computer, SessionOptions); 

            var allVolumes = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Volume");
            var allPDisks = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_DiskDrive"); 

            // Loop through all volumes
            foreach (CimInstance oneVolume in allVolumes)
            {
                // Show volume information

                if (oneVolume.CimInstanceProperties["DriveLetter"].ToString()[0] > ' '  )
                {
                    Console.WriteLine("Volume ‘{0}’ has {1} bytes total, {2} bytes available", 
                                      oneVolume.CimInstanceProperties["DriveLetter"], 
                                      oneVolume.CimInstanceProperties["Size"], 
                                      oneVolume.CimInstanceProperties["SizeRemaining"]);
                }

            } 

            // Loop through all physical disks
            foreach (CimInstance onePDisk in allPDisks)
            {
                // Show physical disk information
                Console.WriteLine("Disk {0} is model {1}, serial number {2}", 
                                  onePDisk.CimInstanceProperties["DeviceId"], 
                                  onePDisk.CimInstanceProperties["Model"].ToString().TrimEnd(), 
                                  onePDisk.CimInstanceProperties["SerialNumber"]);
            } 

            Console.ReadLine();
         }
     }
 }
```



## <a name="systemmanagement-example"></a>Ejemplo de System.Management

En el siguiente ejemplo de código de C# se describe una conexión remota general, mediante los objetos System.Management.


```CSharp
using System;
using System.Management;
public class RemoteConnect 
{
    public static void Main() 
    {
        ConnectionOptions options = new ConnectionOptions();
        options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

        
        ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
        scope.Connect();

        //Query system for Operating System information
        ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
        ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);

        ManagementObjectCollection queryCollection = searcher.Get();
        foreach ( ManagementObject m in queryCollection)
        {
            // Display the remote computer information
            Console.WriteLine("Computer Name     : {0}", m["csname"]);
            Console.WriteLine("Windows Directory : {0}", m["WindowsDirectory"]);
            Console.WriteLine("Operating System  : {0}", m["Caption"]);
            Console.WriteLine("Version           : {0}", m["Version"]);
            Console.WriteLine("Manufacturer      : {0}", m["Manufacturer"]);
        }
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
