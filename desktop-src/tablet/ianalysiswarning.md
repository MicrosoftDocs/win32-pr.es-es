---
description: Representa una advertencia o un error que se produce durante una operación de análisis de tinta.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interfaz IAnalysisWarning (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154445"
---
# <a name="ianalysiswarning-interface"></a>Interfaz IAnalysisWarning

Representa una advertencia o un error que se produce durante una operación de análisis de tinta.

## <a name="members"></a>Miembros

La interfaz **IAnalysisWarning** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisWarning** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAnalysisWarning** tiene estos métodos.



| Método                                                            | Descripción                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBackgroundError**](ianalysiswarning-getbackgrounderror.md) | Recupera el código de error de la operación de análisis de tinta de fondo si se produce un error.<br/>                                    |
| [**GetHint**](ianalysiswarning-gethint.md)                       | Recupera la sugerencia de análisis que produjo esta advertencia<br/>                                                                        |
| [**GetNodeIds**](ianalysiswarning-getnodeids.md)                 | Recupera los identificadores de los nodos de contexto pertinentes que están asociados a esta advertencia.<br/>                              |
| [**GetWarningCode**](ianalysiswarning-getwarningcode.md)         | Recupera el tipo de advertencia que se produjo mediante la enumeración [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .<br/> |



 

## <a name="remarks"></a>Observaciones

Los tipos de advertencias que se pueden producir se describen en la enumeración [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) . A menudo se producen advertencias al intentar usar una característica que no es compatible con el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que usa [**IInkAnalyzer**](iinkanalyzer.md) .

Algunas advertencias indican que el [**IInkAnalyzer**](iinkanalyzer.md) no completó la operación de análisis. Para obtener más información, vea [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un esquema de un controlador de eventos para el evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) . El controlador comprueba [**IAnalysisStatus:: IsSuccessful**](ianalysisstatus-issuccessful.md). Si la operación de análisis genera advertencias, el controlador recorre en iteración la colección de objetos **IAnalysisWarning** .


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisWarnings**](ianalysiswarnings.md)
</dt> <dt>

[**AnalysisWarningCode**](analysiswarningcode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

