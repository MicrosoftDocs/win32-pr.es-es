---
title: Elemento Scale
description: Representa la preferencia de tamaño y diseño de un grupo de controles a través de un par Group, SizeDefinition.
ms.assetid: feef3721-c779-4c64-96c6-9d951ac32277
keywords:
- Escala del elemento Windows cinta de opciones
topic_type:
- apiref
api_name:
- Scale
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 580cfad910a727f7e4392489adc8cb8baec9a0bc
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630206"
---
# <a name="scale-element"></a>Elemento Scale

Representa el tamaño y la preferencia de diseño de [**un grupo de**](windowsribbon-element-group.md) controles a través de un par {**Group**, [**SizeDefinition**](windowsribbon-element-sizedefinition.md)}.

## <a name="usage"></a>Uso

``` syntax
<Scale
  Size = "xs:string"
  Group = "xs:positiveInteger or xs:string"
/>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Grupo</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>Sí<br/></td>
<td>Debe corresponder a un <a href="windowsribbon-element-group.md"><strong>elemento Group</strong></a> <em>CommandName existente.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Una cadena o un valor entero comprendido entre 2 y 59999, inclusivo o 0x2 y 0xea5f en hexadecimal, inclusivo. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Tamaño</strong><br/></td>
<td>xs:string<br/></td>
<td>Sí<br/></td>
<td>Este valor debe corresponder a uno de los tamaños <a href="windowsribbon-element-group.md"><strong></strong></a> válidos para el <em>atributo SizeDefinition</em> del grupo de controles asociado especificado en <em>group</em>. <br/> Restringido a uno de los siguientes valores: <br/> <br/>
<dt><span></span><span></span><strong></strong> (Popup)<br/> </dt> <dd> Diseño de control idéntico a pero hospedado en un panel emergente o <code>Large</code> desplegable.<br/> </dd> <dt><span></span><span></span><strong></strong> (Pequeño)<br/> </dt> <dd> Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> pequeña.<br/> </dd> <dt><span></span><span></span><strong></strong> (Medio)<br/> </dt> <dd> Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>Tamaño medioDefinición.</strong></a><br/> </dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd> Plantilla <a href="windowsribbon-element-sizedefinition.md"><strong>SizeDefinition</strong></a> grande.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md)<br/>                       |
| [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse una o varias veces para [**cada ScalingPolicy**](windowsribbon-element-scalingpolicy.md) o [**ScalingPolicy.IdealSizes.**](windowsribbon-element-scalingpolicy-idealsizes.md)

Cada par *de atributos (Group*, *Size)* debe ser único.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo se puede personalizar la apariencia de los controles de un grupo [**mediante**](windowsribbon-element-group.md) la funcionalidad de diseño adaptable de las plantillas [**SizeDefinition de**](windowsribbon-element-sizedefinition.md) la cinta de opciones.

El [**manifiesto ScalingPolicy**](windowsribbon-element-scalingpolicy.md) de este ejemplo especifica una preferencia [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada uno de los cuatro grupos de controles de una **pestaña** Inicio. Además, se **especifican elementos Scale** para influir en el comportamiento de conserción, en orden descendente, de cada grupo.


```XML
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



## <a name="element-information"></a>Información de elemento



* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** Sí



## <a name="see-also"></a>Vea también

<dl> <dt>

[Personalizar una cinta de opciones mediante definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> </dl>

 

 





