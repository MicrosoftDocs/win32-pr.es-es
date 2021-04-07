---
description: En Administrador de autorización, un rol representa una categoría de usuarios y las tareas a las que están autorizados los usuarios.
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: Agrupar tareas en roles en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c84ec45bba8da9d76e2a4fe0b31324429374a74b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002752"
---
# <a name="grouping-tasks-into-roles-in-script"></a>Agrupar tareas en roles en el script

En Administrador de autorización, un rol representa una categoría de usuarios y las tareas a las que están autorizados los usuarios. Las tareas se agrupan y se asignan a una definición de roles, que se representa mediante un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) con su propiedad [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) establecida en **true**. La definición de roles se puede asignar a un objeto [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) y, a continuación, se asignan usuarios o grupos de usuarios a ese objeto. Para obtener más información sobre tareas y roles, vea [roles](roles.md).

En el ejemplo siguiente se muestra cómo asignar tareas a una definición de roles, crear un objeto de rol y asignar la definición de rol al objeto de rol. En el ejemplo se da por supuesto que hay un almacén de directivas XML con el nombre MyStore.xml en el directorio raíz de la unidad C, que este almacén contiene una aplicación denominada gasto y que esta aplicación contiene tareas denominadas enviar gastos y aprobar gastos.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a task object to act as a role definition.
Dim roleTask
Set roleTask = expenseApp.CreateTask("Expense Admin")

'  Set the IsRoleDefinition property of roleTask to True.
roleTask.IsRoleDefinition = True

'  Add two tasks to the role definition.
roleTask.AddTask CStr("Submit Expense")
roleTask.AddTask CStr("Approve Expense")

'  Save the role definition to the store.
roleTask.Submit

'  Create a role object.
Dim role1
Set role1 = expenseApp.CreateRole("Expense Administrator")

'  Add the role definition to the role object.
role1.AddTask(roleTask.Name)

'  Save the role object to the store.
role1.Submit
```



 

 



