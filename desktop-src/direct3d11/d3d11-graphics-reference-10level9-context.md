---
title: Métodos 10Level9 ID3D11DeviceContext
description: En esta sección se enumeran las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ 11 \_ 0 y el nivel de características superior para los métodos ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075258"
---
# <a name="10level9-id3d11devicecontext-methods"></a>Métodos 10Level9 ID3D11DeviceContext

En esta sección se enumeran las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ 11 \_ 0 y el nivel de características superior para los métodos [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

-   [ID3D11DeviceContext:: CopySubresourceRegion](#id3d11devicecontextcopysubresourceregion)
-   [ID3D11DeviceContext:: CopyResource](#id3d11devicecontextcopyresource)
-   [ID3D11DeviceContext:: CopyStructureCount](#id3d11devicecontextcopystructurecount)
-   [ID3D11DeviceContext:: ClearUnorderedAccessViewFloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [ID3D11DeviceContext:: ClearUnorderedAccessViewUint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [ID3D11DeviceContext:: ClearRenderTargetView](#id3d11devicecontextclearrendertargetview)
-   [ID3D11DeviceContext:: CSSetConstantBuffers](#id3d11devicecontextcssetconstantbuffers)
-   [ID3D11DeviceContext:: CSSetSamplers](#id3d11devicecontextcssetsamplers)
-   [ID3D11DeviceContext:: CSSetShader](#id3d11devicecontextcssetshader)
-   [ID3D11DeviceContext:: CSSetShaderResources](#id3d11devicecontextcssetshaderresources)
-   [ID3D11DeviceContext:: CSSetUnorderedAccessViews](#id3d11devicecontextcssetunorderedaccessviews)
-   [ID3D11DeviceContext::D ispatch](#id3d11devicecontextdispatch)
-   [ID3D11DeviceContext::D ispatchIndirect](#id3d11devicecontextdispatchindirect)
-   [ID3D11DeviceContext::D RAW](#id3d11devicecontextdraw)
-   [ID3D11DeviceContext::D rawAuto](#id3d11devicecontextdrawauto)
-   [ID3D11DeviceContext::D rawIndexed](#id3d11devicecontextdrawindexed)
-   [ID3D11DeviceContext::D rawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [ID3D11DeviceContext::D rawIndexedInstancedIndirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [ID3D11DeviceContext::D rawInstanced](#id3d11devicecontextdrawinstanced)
-   [ID3D11DeviceContext::D rawInstancedIndirect](#id3d11devicecontextdrawinstancedindirect)
-   [ID3D11DeviceContext::D SSetConstantBuffers](#id3d11devicecontextdssetconstantbuffers)
-   [ID3D11DeviceContext::D SSetSamplers](#id3d11devicecontextdssetsamplers)
-   [ID3D11DeviceContext::D SSetShader](#id3d11devicecontextdssetshader)
-   [ID3D11DeviceContext::D SSetShaderResources](#id3d11devicecontextdssetshaderresources)
-   [ID3D11DeviceContext:: GSSetConstantBuffers](#id3d11devicecontextgssetconstantbuffers)
-   [ID3D11DeviceContext:: GSSetSamplers](#id3d11devicecontextgssetsamplers)
-   [ID3D11DeviceContext:: GSSetShader](#id3d11devicecontextgssetshader)
-   [ID3D11DeviceContext:: GSSetShaderResources](#id3d11devicecontextgssetshaderresources)
-   [ID3D11DeviceContext:: HSSetConstantBuffers](#id3d11devicecontexthssetconstantbuffers)
-   [ID3D11DeviceContext:: HSSetSamplers](#id3d11devicecontexthssetsamplers)
-   [ID3D11DeviceContext:: HSSetShader](#id3d11devicecontexthssetshader)
-   [ID3D11DeviceContext:: HSSetShaderResources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [ID3D11DeviceContext:: IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [ID3D11DeviceContext:: OMSetBlendState](#id3d11devicecontextomsetblendstate)
-   [ID3D11DeviceContext:: OMSetRenderTargets](#id3d11devicecontextomsetrendertargets)
-   [ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [ID3D11DeviceContext::P SSetConstantBuffers](#id3d11devicecontextpssetconstantbuffers)
-   [ID3D11DeviceContext::P SSetSamplers](#id3d11devicecontextpssetsamplers)
-   [ID3D11DeviceContext::P SSetShader](#id3d11devicecontextpssetshader)
-   [ID3D11DeviceContext::P SSetShaderResources](#id3d11devicecontextpssetshaderresources)
-   [ID3D11DeviceContext:: RSSetScissorRects](#id3d11devicecontextrssetscissorrects)
-   [ID3D11DeviceContext:: RSSetViewports](#id3d11devicecontextrssetviewports)
-   [ID3D11DeviceContext:: SetPredication](#id3d11devicecontextsetpredication)
-   [ID3D11DeviceContext:: SOSetTargets](#id3d11devicecontextsosettargets)
-   [ID3D11DeviceContext:: VSSetConstantBuffers](#id3d11devicecontextvssetconstantbuffers)
-   [ID3D11DeviceContext:: VSSetSamplers](#id3d11devicecontextvssetsamplers)
-   [ID3D11DeviceContext:: VSSetShader](#id3d11devicecontextvssetshader)
-   [ID3D11DeviceContext:: VSSetShaderResources](#id3d11devicecontextvssetshaderresources)
-   [Temas relacionados](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>ID3D11DeviceContext:: CopySubresourceRegion



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Solo se pueden copiar Texture2D y búferes en la memoria accesible desde la GPU.<br/> Texture3D no se puede copiar desde la memoria accesible desde la GPU a la memoria accesible desde la CPU.<br/> Los recursos que solo tienen D3D10_BIND_SHADER_RESOURCE no se pueden copiar desde la memoria accesible desde la GPU a la memoria accesible desde la CPU.<br/> No se pueden copiar texturas de volumen de mipmapped. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a>ID3D11DeviceContext:: CopyResource



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Solo se pueden copiar Texture2D y búferes en la memoria accesible desde la GPU.<br/> Texture3D no se puede copiar desde la memoria accesible desde la GPU a la memoria accesible desde la CPU.<br/> Los recursos que solo tienen D3D10_BIND_SHADER_RESOURCE no se pueden copiar desde la memoria accesible desde la GPU a la memoria accesible desde la CPU.<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a>ID3D11DeviceContext:: CopyStructureCount



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>ID3D11DeviceContext:: ClearUnorderedAccessViewFloat



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>ID3D11DeviceContext:: ClearUnorderedAccessViewUint



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a>ID3D11DeviceContext:: ClearRenderTargetView



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Solo se borrará el primer segmento de la matriz. Las aplicaciones deben crear una vista de destino de representación para cada superficie o segmento de matriz y, a continuación, borrar cada vista individualmente. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>ID3D11DeviceContext:: CSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a>ID3D11DeviceContext:: CSSetSamplers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a>ID3D11DeviceContext:: CSSetShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a>ID3D11DeviceContext:: CSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>ID3D11DeviceContext:: CSSetUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a>ID3D11DeviceContext::D ispatch



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a>ID3D11DeviceContext::D ispatchIndirect



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext::D RAW



| Nivel de características             | Diferencias de comportamiento                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | El número de primitivas no puede superar 65535.<br/> Las texturas no se pueden repetir más de 128 veces en un primitivo.<br/>    |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | El número de primitivas no puede superar 1048575.<br/> Las texturas no se pueden repetir más de 2048 veces en un primitivo.<br/> |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | El número de primitivas no puede superar 1048575.<br/> Las texturas no se pueden repetir más de 8192 veces en un primitivo.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext::D rawAuto



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext::D rawIndexed



| Nivel de características             | Diferencias de comportamiento                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | El número de primitivas no puede superar 65535.<br/> Las texturas no se pueden repetir más de 128 veces en un primitivo.<br/> Los valores de índice no pueden superar 65534.<br/> No se admiten las listas de puntos indexados.<br/>      |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | El número de primitivas no puede superar 1048575.<br/> Las texturas no se pueden repetir más de 2048 veces en un primitivo.<br/> Los valores de índice no pueden superar 1048575.<br/> No se admiten las listas de puntos indexados.<br/> |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | El número de primitivas no puede superar 1048575.<br/> Las texturas no se pueden repetir más de 8192 veces en un primitivo.<br/> Los valores de índice no pueden superar 1048575.<br/> No se admiten las listas de puntos indexados.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext::D rawIndexedInstanced



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">No se admite $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>El número de primitivas no puede superar 1048575.<br/> Las texturas no se pueden repetir más de 8192 veces en un primitivo.<br/> Los valores de índice no pueden superar 1048575.<br/>
<blockquote>
[!Note]<br />
Cuando se llama al método <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> con un sombreador de vértices que está enlazado a la canalización y que no importa ningún dato por instancia, es posible que algún hardware gráfico de Direct3D 9 no dibuje nada. En concreto, si el sombreador de vértices no usa ningún dato por instancia, llamar a <strong>DrawIndexedInstanced</strong> con 1 instancia no es equivalente a llamar a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>ID3D11DeviceContext::D rawIndexedInstancedIndirect



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext::D rawInstanced



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>ID3D11DeviceContext::D rawInstancedIndirect



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>ID3D11DeviceContext::D SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a>ID3D11DeviceContext::D SSetSamplers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a>ID3D11DeviceContext::D SSetShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a>ID3D11DeviceContext::D SSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>ID3D11DeviceContext:: GSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a>ID3D11DeviceContext:: GSSetSamplers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a>ID3D11DeviceContext:: GSSetShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a>ID3D11DeviceContext:: GSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>ID3D11DeviceContext:: HSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a>ID3D11DeviceContext:: HSSetSamplers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a>ID3D11DeviceContext:: HSSetShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a>ID3D11DeviceContext:: HSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>El formato puede ser diferente del especificado al crear el búfer, pero se incurrirá en una traducción costosa.<br/> Solo permite búferes de índice con el formato de DXGI_FORMAT_R16_UINT. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> El formato puede ser diferente del especificado al crear el búfer, pero se incurrirá en una traducción costosa.<br/> Permite búferes de índice con los formatos DXGI_FORMAT_R16_UINT y DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 y versiones posteriores. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext:: IASetPrimitiveTopology



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admiten topologías primitivas con adyacen $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a>ID3D11DeviceContext:: OMSetBlendState



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">SampleMask no puede ser cero $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a>ID3D11DeviceContext:: OMSetRenderTargets



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Solo se admite un destino de representación $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Solo se admiten cuatro destinos de representación, y todos los recursos enlazados deben tener la misma profundidad de bits.</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>ID3D11DeviceContext::P SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Vea el nivel de característica 10,0, pero el número total de constantes usadas por el sombreador no puede superar los 32 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a>ID3D11DeviceContext::P SSetSamplers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se pueden enlazar más de 16 muestras enlazadas $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a>ID3D11DeviceContext::P SSetShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Solo ps_4_0_level_9_1 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Solo ps_4_0_level_9_3 o ps_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a>ID3D11DeviceContext::P SSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No más de 8 recursos de sombreador enlazados simultáneamente $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a>ID3D11DeviceContext:: RSSetScissorRects



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Solo el rectángulo de tijeras de inicial está disponible $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a>ID3D11DeviceContext:: RSSetViewports



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Solo está disponible la ventanilla de inicial $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

Aunque se especifican valores Float para los miembros de la estructura de la [**\_ ventanilla de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) para la matriz *pViewports* en una llamada a [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para [los niveles de características](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **RSSetViewports** usa los DWords internamente. Debido a este comportamiento, cuando se usa una esquina superior izquierda negativa para la ventanilla, se produce un error en la llamada a **RSSetViewports** para los niveles de características 9 \_ x. Este error se produce porque **RSSetViewports** para 9 \_ x convierte los valores de punto flotante en enteros sin signo sin validación, lo que da como resultado un desbordamiento de enteros.

La llamada a [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para [los niveles de característica](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x y 11 \_ x funciona como se espera, incluso cuando se usa una esquina superior izquierda negativa para la ventanilla.

## <a name="id3d11devicecontextsetpredication"></a>ID3D11DeviceContext:: SetPredication



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a>ID3D11DeviceContext:: SOSetTargets



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>ID3D11DeviceContext:: VSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Vea el nivel de característica 10,0, pero el número total de constantes usadas por el sombreador no puede superar los 255 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a>ID3D11DeviceContext:: VSSetSamplers



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a>ID3D11DeviceContext:: VSSetShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Solo vs_4_0_level_9_1 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Solo vs_4_0_level_9_3 o vs_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a>ID3D11DeviceContext:: VSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





