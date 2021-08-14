---
title: Código de ejemplo para usar una búsqueda de VLV
description: Este tema contiene ejemplos de código de C++ que se usan para realizar una búsqueda de VLV.
ms.assetid: 9bad8f71-80e3-446f-9be3-c00defbe1ea5
ms.tgt_platform: multiple
keywords:
- Código de ejemplo para usar una búsqueda de VLV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e3714216e985ac4b45227fa1d9db10826d0fe1f32ab636a711fe98790647238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428438"
---
# <a name="example-code-for-using-a-vlv-search"></a>Código de ejemplo para usar una búsqueda de VLV

En los ejemplos de código siguientes se usan búsquedas de VLV para obtener resultados de búsqueda.

-   **GetVLVItemCount**
-   **GetVLVItemText**
-   **GetVLVItemsByString**

## <a name="utility-functions"></a>Funciones de la utilidad

Las funciones de ejemplo de este tema usan los siguientes ejemplos de código.


```C++
/***************************************************************************

    CopyContextID()

***************************************************************************/

BOOL CopyContextID(LPBYTE pContextID, 
                   DWORD dwContextIDLength, 
                   LPBYTE* ppContextIDOut)
{
    
    /*
    Ensure that the context ID buffer is large enough and copy the context ID 
    into it. Reallocation of the buffer is not required if the same size is 
    required.
    */
    if(*ppContextIDOut && (LocalSize(*ppContextIDOut) != dwContextIDLength))
    {
        FreeContextID(ppContextIDOut);
        *ppContextIDOut = NULL;
    }

    // If the buffer does not exist, allocate it.
    if(!*ppContextIDOut)
    {
        *ppContextIDOut = (LPBYTE)LocalAlloc(LPTR, dwContextIDLength);
    }

    // Copy the memory.
    if(*ppContextIDOut)
    {
        CopyMemory(*ppContextIDOut, pContextID, dwContextIDLength);
    }

    return (NULL != *ppContextIDOut);
}

/***************************************************************************

    FreeContextID()

***************************************************************************/

void FreeContextID(LPBYTE* ppContextID)
{
        LocalFree(*ppContextID);
        *ppContextID = NULL;
}

/**************************************************************************

   WideCharToLocal()
   
**************************************************************************/

int WideCharToLocal(LPTSTR pLocal, LPCWSTR pWide, DWORD dwChars)
{
    if(!pLocal || !pWide)
    {
        return 0;
    }

    *pLocal = 0;

#ifdef UNICODE
    wcsncpy_s(pLocal, pWide, dwChars);
#else
    WideCharToMultiByte( CP_ACP, 
                        0, 
                        pWide, 
                        -1, 
                        pLocal, 
                        dwChars, 
                        NULL, 
                        NULL);
#endif

    return lstrlen(pLocal);
}

```



## <a name="getvlvitemcount-example-function"></a>Función de ejemplo GetVLVItemCount

En el ejemplo de código siguiente se muestra cómo usar una búsqueda de VLV para obtener una estimación del número de elementos resultantes de la búsqueda.


```C++
/***************************************************************************

    GetVLVItemCount()

***************************************************************************/

HRESULT GetVLVItemCount(IDirectorySearch *pSearch, 
                        LPCWSTR pwszSearchFilter, 
                        LPCWSTR pwszAttribute,
                        DWORD *pdwCount,
                        LPBYTE* ppContextID)
{
    HRESULT hr;

    if(!pSearch || !pdwCount)
    {
        return E_INVALIDARG;
    }

    *pdwCount = 0;

    // Initialize the ADS_VLV structure.
    ADS_VLV vlvPref;
    ZeroMemory(&vlvPref, sizeof(vlvPref));

    // Using these values will retrieve the approximate number of items returned by the search.
    vlvPref.dwOffset = 0;
    vlvPref.dwContentCount = 0;
    vlvPref.dwContextIDLength = 0;

    // Set the VLV search preference.
    ADS_SEARCHPREF_INFO SearchPrefs[2];
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_VLV;
    SearchPrefs[0].vValue.dwType = ADSTYPE_PROV_SPECIFIC;
    SearchPrefs[0].vValue.ProviderSpecific.dwLength = sizeof(ADS_VLV);
    SearchPrefs[0].vValue.ProviderSpecific.lpValue = (LPBYTE)&vlvPref;

    /*
    Have the server perform the sorting. This option must be explicitly added 
    when using VLV searching.
    */
    ADS_SORTKEY sortKey;
    sortKey.pszAttrType = (LPWSTR)pwszAttribute;
    sortKey.pszReserved = NULL;
    sortKey.fReverseorder = 0;

    SearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SORT_ON;
    SearchPrefs[1].vValue.dwType = ADSTYPE_PROV_SPECIFIC;
    SearchPrefs[1].vValue.ProviderSpecific.dwLength = sizeof(ADS_SORTKEY);
    SearchPrefs[1].vValue.ProviderSpecific.lpValue = (LPBYTE)&sortKey;

    // Set the search preferences.
    hr = pSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(SearchPrefs[0]));
    if(S_OK != hr)
    {
        return hr;
    }

    // Execute the search.
    ADS_SEARCH_HANDLE hSearchHandle;
    LPWSTR rgAttributes[1];
    rgAttributes[0] = (LPWSTR)pwszAttribute;
    hr = pSearch->ExecuteSearch((LPWSTR)pwszSearchFilter, 
        rgAttributes, 
        sizeof(rgAttributes)/sizeof(rgAttributes[0]), 
        &hSearchHandle);
    if(S_OK != hr)
    {
        return hr;
    }

    // Get the first result row.
    hr = pSearch->GetFirstRow(hSearchHandle);
    if(S_OK != hr)
    {
        return hr;
    }

    // Get the VLV response data.
    ADS_SEARCH_COLUMN column;
    hr = pSearch->GetColumn(hSearchHandle, ADS_VLV_RESPONSE, &column);
    if(S_OK != hr)
    {
        return hr;
    }

    ADS_VLV *pVlv = (ADS_VLV*)column.pADsValues->ProviderSpecific.lpValue;
    *pdwCount = pVlv->dwContentCount;

    /*
    Allocate or reallocate the buffer if required and copy the context ID 
    to the buffer.
    */
    CopyContextID(pVlv->lpContextID, pVlv->dwContextIDLength, ppContextID);

    // Release the column.
    pSearch->FreeColumn(&column);

    // Close the search handle.
    pSearch->CloseSearchHandle(hSearchHandle);

    return hr;
}
```



## <a name="getvlvitemtext-example-function"></a>Función de ejemplo GetVLVItemText

En el ejemplo de código siguiente se muestra cómo usar una búsqueda de VLV para obtener el texto de un solo elemento basado en un índice.


```C++
/***************************************************************************

    GetVLVItemText()

***************************************************************************/

HRESULT GetVLVItemText(IDirectorySearch *pSearch, 
                       LPCWSTR pwszSearchFilter, 
                       LPCWSTR pwszAttribute,
                       DWORD dwIndex,
                       LPTSTR pszADsPath,
                       DWORD dwChars,
                       LPBYTE* ppContextID)
{
    HRESULT hr;

    if(!pSearch)
    {
        return E_INVALIDARG;
    }

    // Initialize the ADS_VLV structure.
    ADS_VLV vlvPref;
    ZeroMemory(&vlvPref, sizeof(vlvPref));

    // This index is one-based, but the index passed is zero-based.
    vlvPref.dwOffset = dwIndex + 1;
    vlvPref.dwBeforeCount = 0;
    vlvPref.dwAfterCount = 0;
    vlvPref.dwContentCount = 0;
    if(*ppContextID)
    {
        vlvPref.lpContextID = *ppContextID;
        vlvPref.dwContextIDLength = (DWORD)LocalSize(*ppContextID);
    }

    // Set the VLV search preference.
    ADS_SEARCHPREF_INFO SearchPrefs[2];
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_VLV;
    SearchPrefs[0].vValue.dwType = ADSTYPE_PROV_SPECIFIC;
    SearchPrefs[0].vValue.ProviderSpecific.dwLength = sizeof(ADS_VLV);
    SearchPrefs[0].vValue.ProviderSpecific.lpValue = (LPBYTE)&vlvPref;

    /*
    Instruct the server to perform the sort. This option must be explicitly added 
    when using a VLV search.
    */
    ADS_SORTKEY sortKey;
    sortKey.pszAttrType = (LPWSTR)pwszAttribute;
    sortKey.pszReserved = NULL;
    sortKey.fReverseorder = 0;

    SearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SORT_ON;
    SearchPrefs[1].vValue.dwType = ADSTYPE_PROV_SPECIFIC;
    SearchPrefs[1].vValue.ProviderSpecific.dwLength = sizeof(ADS_SORTKEY);
    SearchPrefs[1].vValue.ProviderSpecific.lpValue = (LPBYTE)&sortKey;

    // Set the search preferences.
    hr = pSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(SearchPrefs[0]));
    if(S_OK != hr)
    {
        return hr;
    }

    // Execute the search.
    ADS_SEARCH_HANDLE hSearchHandle;
    LPWSTR rgAttributes[1];
    rgAttributes[0] = (LPWSTR)pwszAttribute;
    hr = pSearch->ExecuteSearch((LPWSTR)pwszSearchFilter, 
        rgAttributes, 
        sizeof(rgAttributes)/sizeof(rgAttributes[0]), 
        &hSearchHandle);
    if(S_OK != hr)
    {
        return hr;
    }

    // Get the first result row.
    hr = pSearch->GetFirstRow(hSearchHandle);
    if(S_OK == hr)
    {
        ADS_SEARCH_COLUMN column;

        // Get the ADsPath.
        hr = pSearch->GetColumn(hSearchHandle, (LPWSTR)pwszAttribute, &column);
        if(SUCCEEDED(hr))
        {
            WideCharToLocal(pszADsPath, column.pADsValues->CaseIgnoreString, dwChars);
            pSearch->FreeColumn(&column);
        }
    
        // Get the VLV response data.
        hr = pSearch->GetColumn(hSearchHandle, ADS_VLV_RESPONSE, &column);
        if(SUCCEEDED(hr))
        {
            ADS_VLV *pVlv = (ADS_VLV*)column.pADsValues->ProviderSpecific.lpValue;
        
            /*
            Allocate or reallocate the buffer if required and copy the context ID 
            to the buffer.
            */
            CopyContextID(pVlv->lpContextID, pVlv->dwContextIDLength, ppContextID);

            pSearch->FreeColumn(&column);
        }

    }

    // Close the search handle.
    pSearch->CloseSearchHandle(hSearchHandle);

    return hr;
}
```



## <a name="getvlvitemsbystring-example-function"></a>Función de ejemplo GetVLVItemsByString

En el ejemplo de código siguiente se muestra cómo usar una búsqueda de VLV para obtener el texto de un número especificado de elementos basado en una cadena. En este ejemplo se agregarán las ordenaciones recuperadas a un cuadro de lista.


```C++
/***************************************************************************

    GetVLVItemsByString()

***************************************************************************/

HRESULT GetVLVItemsByString(HWND hwndListbox,
                            IDirectorySearch *pSearch, 
                            LPCWSTR pwszSearchFilter, 
                            DWORD dwNumToRetrieve,
                            LPCWSTR pwszAttribute,
                            LPCWSTR pwszFilter,
                            LPBYTE* ppContextID)
{
    HRESULT hr;

    if(!pSearch || (0 == dwNumToRetrieve))
    {
        return E_INVALIDARG;
    }

    // Clear the list box.
    SendMessage(hwndListbox, LB_RESETCONTENT, 0, 0);

    // Initialize the ADS_VLV structure.
    ADS_VLV vlvPref;
    ZeroMemory(&vlvPref, sizeof(vlvPref));

    vlvPref.pszTarget = (LPWSTR)pwszFilter;
    vlvPref.dwBeforeCount = 0;
    vlvPref.dwAfterCount = dwNumToRetrieve - 1;
    vlvPref.dwContentCount = 0;

    // Set the VLV search preference.
    ADS_SEARCHPREF_INFO SearchPrefs[2];
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_VLV;
    SearchPrefs[0].vValue.dwType = ADSTYPE_PROV_SPECIFIC;
    SearchPrefs[0].vValue.ProviderSpecific.dwLength = sizeof(ADS_VLV);
    SearchPrefs[0].vValue.ProviderSpecific.lpValue = (LPBYTE)&vlvPref;

    /*
    Instruct the server to perform the sort. This option must be explicitly added 
    when using VLV search.
    */
    ADS_SORTKEY sortKey;
    sortKey.pszAttrType = (LPWSTR)pwszAttribute;
    sortKey.pszReserved = NULL;
    sortKey.fReverseorder = 0;

    SearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SORT_ON;
    SearchPrefs[1].vValue.dwType = ADSTYPE_PROV_SPECIFIC;
    SearchPrefs[1].vValue.ProviderSpecific.dwLength = sizeof(ADS_SORTKEY);
    SearchPrefs[1].vValue.ProviderSpecific.lpValue = (LPBYTE)&sortKey;

    // Set the search preferences.
    hr = pSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(SearchPrefs[0]));
    if(S_OK != hr)
    {
        return hr;
    }

    // Execute the search.
    ADS_SEARCH_HANDLE hSearchHandle;
    hr = pSearch->ExecuteSearch((LPWSTR)pwszSearchFilter, 
        NULL, 
        -1, 
        &hSearchHandle);
    if(S_OK != hr)
    {
        return hr;
    }

    ADS_SEARCH_COLUMN column;

    // Get the first result row.
    hr = pSearch->GetFirstRow(hSearchHandle);
    while(S_OK == hr)
    {
        // Get the data.
        hr = pSearch->GetColumn(hSearchHandle, (LPWSTR)pwszAttribute, &column);
        if(SUCCEEDED(hr))
        {
            TCHAR szItemText[MAX_PATH];
            WideCharToLocal(szItemText, column.pADsValues->CaseIgnoreString, MAX_PATH);
            SendMessage(hwndListbox, LB_ADDSTRING, 0, (LPARAM)szItemText);

            pSearch->FreeColumn(&column);
        }
    
        // Get the next row.
        hr = pSearch->GetNextRow(hSearchHandle);
    }

    // Get the VLV response data.
    hr = pSearch->GetColumn(hSearchHandle, ADS_VLV_RESPONSE, &column);
    if(S_OK != hr)
    {
        return hr;
    }

    ADS_VLV *pVlv = (ADS_VLV*)column.pADsValues->ProviderSpecific.lpValue;

    /*
    Allocate or reallocate the buffer if required and copy the context ID 
    to the buffer.
    */
    CopyContextID(pVlv->lpContextID, pVlv->dwContextIDLength, ppContextID);

    // Release the column.
    pSearch->FreeColumn(&column);

    // Close the search handle.
    pSearch->CloseSearchHandle(hSearchHandle);

    return hr;
}
```



 

 




