---
description: En C++, el valor devuelto suele ser de tipo HRESULT.
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: Valores devueltos en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276801"
---
# <a name="return-values-in-c"></a><span data-ttu-id="e15a7-103">Valores devueltos en C++</span><span class="sxs-lookup"><span data-stu-id="e15a7-103">Return Values in C++</span></span>

<span data-ttu-id="e15a7-104">En C++, el valor devuelto suele ser de tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e15a7-104">In C++, the return value is typically of type **HRESULT**.</span></span> <span data-ttu-id="e15a7-105">Es de este valor devuelto que se puede determinar si el método se realizó correctamente o no, y si no es así, cuál fue el error.</span><span class="sxs-lookup"><span data-stu-id="e15a7-105">It is from this return value that it can be determined whether the method succeeded or not, and if not, what the error was.</span></span> <span data-ttu-id="e15a7-106">Los servicios de Certificate Server normalmente devuelven \_ los valores correctos para **HRESULT** cuando el método se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e15a7-106">Certificate Services typically returns S\_OK for the **HRESULT** when the method has completed successfully.</span></span> <span data-ttu-id="e15a7-107">Los valores de programación que se deben devolver se devuelven a través de los parámetros "out" en el método.</span><span class="sxs-lookup"><span data-stu-id="e15a7-107">Programmatic values that need to be returned are returned through "out" parameters in the method.</span></span> <span data-ttu-id="e15a7-108">En el ejemplo siguiente se muestra una llamada al método de C++ para recuperar una propiedad de solicitud:</span><span class="sxs-lookup"><span data-stu-id="e15a7-108">The following example shows a C++ method call to retrieve a request property:</span></span>


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



<span data-ttu-id="e15a7-109">En el fragmento de código anterior, se devuelve SUCCESS o Failure a la variable **HRESULT** , *HR*.</span><span class="sxs-lookup"><span data-stu-id="e15a7-109">In the preceding code fragment, success or failure is returned to the **HRESULT** variable, *hr*.</span></span> <span data-ttu-id="e15a7-110">Es imperativo comprobar que la variable **HRESULT** se ha \[ controlado correctamente en el código por la condición (S \_ OK! = hr) \] .</span><span class="sxs-lookup"><span data-stu-id="e15a7-110">It is imperative to check the **HRESULT** variable for success \[handled in the code by the condition (S\_OK != hr)\].</span></span> <span data-ttu-id="e15a7-111">Si el método se completó correctamente, el valor de la propiedad de solicitud se devuelve en el parámetro **Variant** *varProp* .</span><span class="sxs-lookup"><span data-stu-id="e15a7-111">If the method completed successfully, the request property value is returned in the **VARIANT** *varProp* parameter.</span></span>

 

 



