---
description: 'Paso 3: reutilización de componentes'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Paso 3: reutilización de componentes'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104555615"
---
# <a name="step-3-reusing-components"></a><span data-ttu-id="39b01-103">Paso 3: reutilización de componentes</span><span class="sxs-lookup"><span data-stu-id="39b01-103">Step 3: Reusing Components</span></span>

## <a name="objectives"></a><span data-ttu-id="39b01-104">Objetivos</span><span class="sxs-lookup"><span data-stu-id="39b01-104">Objectives</span></span>

<span data-ttu-id="39b01-105">En este paso, obtendrá información sobre lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="39b01-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="39b01-106">Componentes reutilizables.</span><span class="sxs-lookup"><span data-stu-id="39b01-106">Reusable components.</span></span>
-   <span data-ttu-id="39b01-107">Cómo planear la reutilización.</span><span class="sxs-lookup"><span data-stu-id="39b01-107">How to plan for reusability.</span></span>

## <a name="description"></a><span data-ttu-id="39b01-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="39b01-108">Description</span></span>

<span data-ttu-id="39b01-109">Dos partes anteriores de este manual de servicios COM+, [paso 1: crear un componente transaccional](step-1--creating-a-transactional-component.md) y [paso 2: extender una transacción en varios componentes](step-2--extending-a-transaction-across-multiple-components.md) mostrar cómo escribir un componente que llame a un segundo componente para ayudar a completar algún trabajo, actualizar la información de autor en la base de datos de Microsoft SQL Server pubs; todo el trabajo está protegido por una sola transacción.</span><span class="sxs-lookup"><span data-stu-id="39b01-109">Two previous parts of this COM+ services primer, [Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) and [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md) show how to write one component that calls a second component to assist in completing some work, updating author information in the Microsoft SQL Server Pubs database; all work is protected by a single transaction.</span></span> <span data-ttu-id="39b01-110">Los componentes de ejemplo se centran en el trabajo de actualización de los datos de un autor y en la comprobación de la dirección del autor, y en el procesamiento de transacciones proporcionado por COM+, la [activación JIT](com--just-in-time-activation.md)y la [protección de simultaneidad](com--synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="39b01-110">The sample components focused on the work of updating an author's data and verifying the author's address, and COM+ provided transaction processing, [JIT activation](com--just-in-time-activation.md), and [concurrency protection](com--synchronization.md).</span></span>

<span data-ttu-id="39b01-111">En este paso se muestra cómo reutilizar los componentes creados en los pasos 1 y 2 y se examina lo que esto significa para el diseño de esos componentes.</span><span class="sxs-lookup"><span data-stu-id="39b01-111">This step demonstrates how to reuse the components created in steps 1 and 2 and looks at what this means to the design of those components.</span></span> <span data-ttu-id="39b01-112">Como se muestra en la siguiente ilustración, esto significa que se crea un nuevo componente, `AddNewAuthor` , que agrega nuevos autores a la base de datos mediante una llamada a `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="39b01-112">As shown in the following illustration, this means creating a new component, `AddNewAuthor`, that adds new authors to the database by calling `UpdateAuthorAddress`.</span></span>

![Diagrama que muestra el flujo cuando se reutilizan los componentes.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

<span data-ttu-id="39b01-114">Además de reutilizar la funcionalidad de componentes existente, `AddNewAuthor` llama a otro nuevo componente denominado `ValidateAuthorName` .</span><span class="sxs-lookup"><span data-stu-id="39b01-114">In addition to reusing existing component functionality, `AddNewAuthor` calls another new component called `ValidateAuthorName`.</span></span> <span data-ttu-id="39b01-115">Como muestra la ilustración anterior, `ValidateAuthorName` es no transaccional.</span><span class="sxs-lookup"><span data-stu-id="39b01-115">As the preceding illustration shows, `ValidateAuthorName` is non-transactional.</span></span> <span data-ttu-id="39b01-116">El valor del atributo de transacción para este componente se deja en su configuración predeterminada (**no se admite**) para excluir su trabajo de la transacción.</span><span class="sxs-lookup"><span data-stu-id="39b01-116">The transaction attribute value for this component is left at its default setting (**Not Supported**) to exclude its work from the transaction.</span></span> <span data-ttu-id="39b01-117">Como se muestra en el código de ejemplo del paso 3, `ValidateAuthorName` realiza consultas de solo lectura en la base de datos y el error de esta tarea secundaria no debe tener la posibilidad de anular la transacción.</span><span class="sxs-lookup"><span data-stu-id="39b01-117">As shown in the step 3 sample code, `ValidateAuthorName` performs read-only queries on the database, and the failure of this minor task should not have the potential to abort the transaction.</span></span> <span data-ttu-id="39b01-118">Sin embargo, el valor de atributo de transacción del `AddNewAuthor` componente se establece en **required**.</span><span class="sxs-lookup"><span data-stu-id="39b01-118">However, the transaction attribute value of the `AddNewAuthor` component is set to **Required**.</span></span>

<span data-ttu-id="39b01-119">`AddNewAuthor`Todos los componentes de, `UpdateAuthorAddress` y `ValidateAuthorAddress` votan en la transacción.</span><span class="sxs-lookup"><span data-stu-id="39b01-119">The `AddNewAuthor`, `UpdateAuthorAddress`, and `ValidateAuthorAddress` components all vote in the transaction.</span></span> <span data-ttu-id="39b01-120">En esta transacción, `AddNewAuthor` es el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="39b01-120">In this transaction, `AddNewAuthor` is the root object.</span></span> <span data-ttu-id="39b01-121">COM+ siempre hace que el primer objeto creado en la transacción sea el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="39b01-121">COM+ always makes the first object created in the transaction the root object.</span></span>

<span data-ttu-id="39b01-122">En este ejemplo, la reutilización del `UpdateAuthorAddress` componente es fácil: com + proporciona automáticamente los servicios esperados.</span><span class="sxs-lookup"><span data-stu-id="39b01-122">In this example, reusing the `UpdateAuthorAddress` component is easy—COM+ automatically delivers the expected services.</span></span> <span data-ttu-id="39b01-123">Sin embargo, los resultados serían diferentes si el valor del atributo de transacción del `UpdateAuthorAddress` componente se hubiera establecido inicialmente en **requiere New** en lugar de **required**.</span><span class="sxs-lookup"><span data-stu-id="39b01-123">However, the results would be different if the transaction attribute value of the `UpdateAuthorAddress` component were initially set to **Requires New** instead of **Required**.</span></span> <span data-ttu-id="39b01-124">En la superficie, ambos valores aparecen de forma similar. ambos garantizan una transacción.</span><span class="sxs-lookup"><span data-stu-id="39b01-124">On the surface, both settings appear similar; both guarantee a transaction.</span></span> <span data-ttu-id="39b01-125">**Requiere New**, sin embargo, siempre inicia una nueva transacción, mientras que **required** inicia una nueva transacción solo cuando el autor de la llamada del objeto es no transaccional.</span><span class="sxs-lookup"><span data-stu-id="39b01-125">**Requires New**, however, always starts a new transaction, while **Required** starts a new transaction only when the object's caller is non-transactional.</span></span> <span data-ttu-id="39b01-126">Puede ver, en este aspecto, lo importante que conviene configurar con `UpdateAuthorAddress` cuidado y de forma minuciosa.</span><span class="sxs-lookup"><span data-stu-id="39b01-126">You can see from this how important it was to configure `UpdateAuthorAddress` carefully and thoughtfully.</span></span> <span data-ttu-id="39b01-127">De lo contrario, COM+ podría haber interpretado la solicitud de servicio de forma diferente, generando dos transacciones no relacionadas, tal como se muestra en la siguiente ilustración, en lugar de una.</span><span class="sxs-lookup"><span data-stu-id="39b01-127">Otherwise, COM+ might have interpreted the service request differently, generating two unrelated transactions, as shown in the following illustration, instead of one.</span></span>

![Diagrama que muestra el flujo al reutilizar los componentes con "requires New".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> <span data-ttu-id="39b01-129">Cuando vuelva a usar los componentes, asegúrese de que los servicios estén configurados para admitir el resultado deseado.</span><span class="sxs-lookup"><span data-stu-id="39b01-129">When you reuse components, make sure the services are configured to support your desired outcome.</span></span>

 

## <a name="sample-code"></a><span data-ttu-id="39b01-130">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="39b01-130">Sample code</span></span>

<span data-ttu-id="39b01-131">El componente AddNewAuthor realiza agregaciones por lotes de nuevos autores permitiendo que el objeto permanezca activo hasta que el cliente libere su referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="39b01-131">The AddNewAuthor component performs batch additions of new authors by allowing the object to remain active until the client releases its reference to the object.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



<span data-ttu-id="39b01-132">El `ValidateAuthorName` componente valida los nombres de autor antes de `AddNewAuthor` Agregar el nombre a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="39b01-132">The `ValidateAuthorName` component validates author names before `AddNewAuthor` adds the name to the database.</span></span> <span data-ttu-id="39b01-133">Este componente produce un error en el autor de la llamada si se produce algo inesperado.</span><span class="sxs-lookup"><span data-stu-id="39b01-133">This component throws an error back to its caller if something unexpected happens.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a><span data-ttu-id="39b01-134">Resumen</span><span class="sxs-lookup"><span data-stu-id="39b01-134">Summary</span></span>

-   <span data-ttu-id="39b01-135">Hay ocasiones en las que no desea que un componente vote en la transacción.</span><span class="sxs-lookup"><span data-stu-id="39b01-135">There are times when you don't want a component to vote in the transaction.</span></span>
-   <span data-ttu-id="39b01-136">COM+ no aplica la activación JIT ni la protección de simultaneidad en componentes no transaccionales.</span><span class="sxs-lookup"><span data-stu-id="39b01-136">COM+ does not enforce JIT activation or concurrency protection on non-transactional components.</span></span> <span data-ttu-id="39b01-137">Puede configurar estos servicios por separado.</span><span class="sxs-lookup"><span data-stu-id="39b01-137">You may configure these services separately.</span></span>
-   <span data-ttu-id="39b01-138">La configuración de un componente que realiza la llamada afecta a cómo COM+ interpreta las solicitudes de servicio del componente al que se ha llamado.</span><span class="sxs-lookup"><span data-stu-id="39b01-138">A calling component's configuration affects how COM+ interprets the service requests of the called component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39b01-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39b01-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39b01-140">Paso 1: crear un componente transaccional</span><span class="sxs-lookup"><span data-stu-id="39b01-140">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="39b01-141">Paso 2: extensión de una transacción en varios componentes</span><span class="sxs-lookup"><span data-stu-id="39b01-141">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="39b01-142">Configuración de transacciones</span><span class="sxs-lookup"><span data-stu-id="39b01-142">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="39b01-143">Diseño para la escalabilidad</span><span class="sxs-lookup"><span data-stu-id="39b01-143">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> </dl>

 

 



