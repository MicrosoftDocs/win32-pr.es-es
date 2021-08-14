---
title: Métodos de propiedad IADsPropertyEntry (Iads.h)
description: Proporcione acceso a las siguientes propiedades.
ms.assetid: 73b0f6d4-55db-46cf-a781-e10bc4fcf2db
ms.tgt_platform: multiple
keywords:
- AdsI de los métodos de propiedad IADsPropertyEntry
topic_type:
- apiref
api_name:
- IADsPropertyEntry Property Methods
- IADsPropertyEntry.Name
- IADsPropertyEntry.get_Name
- IADsPropertyEntry.put_Name
- IADsPropertyEntry.ADsType
- IADsPropertyEntry.get_ADsType
- IADsPropertyEntry.put_ADsType
- IADsPropertyEntry.ControlCode
- IADsPropertyEntry.get_ControlCode
- IADsPropertyEntry.put_ControlCode
- IADsPropertyEntry.Values
- IADsPropertyEntry.get_Values
- IADsPropertyEntry.put_Values
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b4fd6459ff2aa0a93ea050fa8e5d2133c09484c697d17fab204762e8765039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427658"
---
# <a name="iadspropertyentry-property-methods"></a>Métodos de propiedad IADsPropertyEntry

Los métodos de propiedad [**de la interfaz IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) proporcionan acceso a las propiedades siguientes. Para obtener más información sobre los métodos de propiedad, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**ADsType**
</dt> <dd> <dl>

Tipo de datos de la **propiedad** Name. Los valores del tipo de datos se definen en la [**enumeración ADSTYPEENUM.**](/windows/win32/api/iads/ne-iads-adstypeenum)

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* plADsType
);
HRESULT put_ADsType(
  [in] LONG lADsType
);
```


</dt> </dl> </dd> <dt>

**ControlCode**
</dt> <dd> <dl>

Constante que especifica la operación que se va a realizar en la propiedad con nombre. El valor se define en la [**enumeración ADS \_ PROPERTY OPERATION \_ \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ControlCode(
  [out] LONG* pControlCode
);
HRESULT put_ControlCode(
  [in] LONG lnControlCode
);
```


</dt> </dl> </dd> <dt>

**Nombre**
</dt> <dd> <dl>

Nombre de la entrada de propiedad. Este nombre debe corresponder al nombre de un atributo tal y como se define en el esquema.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
HRESULT put_Name(
  [in] BSTR bstrName
);
```


</dt> </dl> </dd> <dt>

**Valores**
</dt> <dd> <dl>

Matriz **VARIANT.** Cada elemento de esta matriz representa un valor de la propiedad con nombre. Estos valores de propiedad se representan mediante objetos ADSI que implementan las [**interfaces IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) e [**IADsPropertyValue2.**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) Por lo tanto, la matriz **VARIANT** contiene una matriz de punteros a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en los objetos ADSI que implementan las **interfaces IADsPropertyValue** e **IADsPropertyValue2.**

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Values(
  [out] VARIANT* pvValues
);
HRESULT put_Values(
  [in] VARIANT vValues
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentarios

Cada método de propiedad admite los **valores devueltos HRESULT** estándar, incluido S \_ OK. Para obtener más información sobre otros valores devueltos, vea [AdsI Error Codes](adsi-error-codes.md).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo recuperar una propiedad con nombre de la memoria caché y crear una nueva entrada de propiedad.


```VB
 
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup

'------------------------------------------------------------
'----- Getting IADsPropertyEntry ----------------------------
'------------------------------------------------------------
 
' Create the property list object.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a named property entry object.
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)

' Insert code to do something with propEntry
Set propEntry = Nothing
 
'------------------------------------------------------------
'---- Setting IADsPropertyEntry -----------------------------
'------------------------------------------------------------
 
' Create a property value object.
Set propVal = New PropertyValue
 
'---- Property Value -----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'---- Create a new Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' ---- Put the newly created property entry to the cache ----
propList.PutPropertyItem (propEntry)
 
' Commit the entry to the directory store.
propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



En el ejemplo de código siguiente se muestra cómo obtener una propiedad con nombre de una memoria caché.


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADs *pObj = NULL;
VARIANT var;
long valType = ADSTYPE_CASE_IGNORE_STRING;
 
VariantInit(&var);
 
// Bind to directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){return;}
 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), valType, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Get the name and the type of the property entry.
BSTR nm = NULL;
hr = pEntry->get_Name(&nm);
printf("Property name = %S\n",nm);
VariantClear(&var);
long at;
hr = pEntry->get_ADsType(&at);
printf("Property type = %d\n",a);

Cleanup:
    if(nm)
        SysFreeString(nm);

    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pObj)
        pObj->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID IADsPropertyEntry se define como \_ 05792C8E-941F-11D0-8529-00C04FD8D503<br/>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ENUMERACIÓN \_ DE OPERACIÓN DE PROPIEDAD DE \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)
</dt> <dt>

[Códigos de error ADSI](adsi-error-codes.md)
</dt> <dt>

[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

