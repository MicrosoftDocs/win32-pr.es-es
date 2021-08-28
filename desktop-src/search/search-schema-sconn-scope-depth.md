---
description: El elemento depth especifica si el ámbito del conector de búsqueda &lt; debe incluir direcciones URL &gt; secundarias. Los valores permitidos son Deep y Shallow. Este elemento no tiene elementos secundarios ni atributos.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: elemento depth (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 430ad3d047331a4bb3ffc58bd134d2364aaa0838
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886768"
---
# <a name="depth-element-search-connector-schema"></a>elemento depth (esquema del conector de búsqueda)

El elemento depth especifica si el ámbito del conector de búsqueda &lt; debe incluir direcciones URL &gt; secundarias. Los valores permitidos son `Deep` y `Shallow`. Este elemento no tiene elementos secundarios ni atributos.

## <a name="syntax"></a>Syntax


```
<!-- depth -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario                                                                   | Elementos secundarios |
|----------------------------------------------------------------------------------|----------------|
| [elemento scopeItem (esquema del conector de búsqueda)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Comentarios

Si la profundidad es profunda, los usuarios pueden examinar o buscar elementos en el nivel de dirección URL de scopeItem o en cualquier dirección URL secundaria.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra un ámbito de búsqueda que incluye C: CarpetaA y todas sus carpetas secundarias y \\ C: \\ CarpetaB, pero ninguna de sus carpetas secundarias.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



