---
description: El <searchConnectorDescriptionType> elemento es el contenedor de nivel superior para la definición del conector de búsqueda.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f228097e905ea6e60bb9197bcf8b8b381671a52f3375849af992f903df6e8b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937915"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a>Elemento searchConnectorDescriptionType (esquema del conector de búsqueda)

El <searchConnectorDescriptionType> elemento es el contenedor de nivel superior para la definición del conector de búsqueda.

-   [Sintaxis](#syntax)
-   [Información de elemento](#element-information)
-   [Atributos](#attributes)
-   [Comentarios:](#remarks)
-   [Ejemplo de un archivo de descripción del conector de búsqueda](#example-of-a-search-connector-description-file)
-   [Temas relacionados](#related-topics)

## <a name="syntax"></a>Syntax


```
<!-- searchConnectorDescriptionType -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```



## <a name="element-information"></a>Información de elemento



| Elemento primario | Elementos secundarios                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [Elemento isSearchOnlyItem (esquema del conector de búsqueda)](search-schema-sconn-issearchonlyitem.md)                           |
|                | [Elemento isDefaultSaveLocation (esquema del conector de búsqueda)](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [Elemento isDefaultNonOwnerSaveLocation (esquema del conector de búsqueda)](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [elemento description (Esquema del conector de búsqueda)](search-schema-sconn-description.md)                                     |
|                | [Elemento iconReference (Esquema del conector de búsqueda)](search-schema-sconn-iconreference.md)                                 |
|                | [Elemento imageLink (esquema del conector de búsqueda)](search-schema-sconn-imagelink.md)                                         |
|                | [elemento author (Esquema del conector de búsqueda)](search-schema-sconn-author.md)                                               |
|                | [elemento dateCreated (esquema del conector de búsqueda)](search-schema-sconn-datecreated.md)                                     |
|                | [Elemento templateInfo (esquema del conector de búsqueda)](search-schema-sconn-templateinfo.md)                                   |
|                | [Elemento locationProvider (esquema del conector de búsqueda)](search-schema-sconn-locationprovider.md)                           |
|                | [elemento scope (esquema del conector de búsqueda)](search-schema-sconn-scope.md)                                                 |
|                | [elemento propertyStore (esquema del conector de búsqueda)](search-schema-sconn-propertystore.md)                                 |
|                | [Elemento includeInStartMenuScope (esquema del conector de búsqueda)](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [elemento domain (esquema del conector de búsqueda)](search-schema-sconn-domain.md)                                               |
|                | [Elemento supportsAdvancedQuerySyntax (esquema del conector de búsqueda)](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [Elemento isIndexed (esquema del conector de búsqueda)](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | Opcional. Nombre para mostrar del publicador que proporciona el conector de búsqueda.      |
| product   | Opcional. Nombre para mostrar del producto al que se aplica el conector de búsqueda. |



 

## <a name="remarks"></a>Comentarios

Los conectores de búsqueda para la búsqueda federada no se pueden usar en bibliotecas. El esquema para los conectores de búsqueda de bibliotecas es una extensión del esquema descrito aquí e incluye información específica de las bibliotecas.

## <a name="example-of-a-search-connector-description-file"></a>Ejemplo de un archivo de descripción del conector de búsqueda

A continuación se muestra un ejemplo de un archivo de descripción del conector de búsqueda para un servicio web de búsqueda federado.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



A continuación se muestra un ejemplo de un archivo de descripción del conector de búsqueda para un controlador de protocolo SMTP.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Información general del esquema de descripción del conector de búsqueda](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> </dl>

 

 



