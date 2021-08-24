---
title: Certification-Authority clase
description: Representa un proceso que emite certificados de clave pública, por ejemplo, un servidor de certificados.
ms.assetid: 0392332c-3c6c-4060-9f9e-16cb8289b392
ms.tgt_platform: multiple
keywords:
- Certification-Authority esquema de AD de clase
- certificationAuthority class AD Schema
topic_type:
- apiref
api_name:
- Certification-Authority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52f87ec37e38ecc411db4330a35a775c926c979feee509850948f5e014b1133c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701965"
---
# <a name="certification-authority-class"></a>Certification-Authority clase

Representa un proceso que emite certificados de clave pública, por ejemplo, un servidor de certificados.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Certification-Authority              |
| Ldap-Display-Name | certificationAuthority               |
| Privilegio actualizar  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Schema-Id-Guid    | 3fdfee50-47f4-11d1-a9c3-0000f80367c1 |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Atributos](#windows-2000-server-attributes)



| Entrada | Valor |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.16                                                                                     |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**Contenedor**](c-container.md)                                                             |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Windows atributos de servidor 2000

Esta clase contiene los siguientes atributos para Windows 2000 Server:



| Atributo                                                                 | Mandatory | Derivado de                                                |
|---------------------------------------------------------------------------|-----------|-------------------------------------------------------------|
| [**Descripción del administrador**](a-admindescription.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Atributos permitidos**](a-allowedattributes.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md) | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Authority-Revocation-List**](a-authorityrevocationlist.md)            | Verdadero      | **Entidad de certificación**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**CERTIFICADO DE ENTIDAD DE CERTIFICACIÓN**](a-cacertificate.md)                                 | Verdadero      | **Entidad de certificación**                                 |
| [**CA-Certificate-DN**](a-cacertificatedn.md)                            | Falso     | **Entidad de certificación**                                 |
| [**Ca-Conectar**](a-caconnect.md)                                         | Falso     | **Entidad de certificación**                                 |
| [**Canonical-Name**](a-canonicalname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Usos de CA**](a-causages.md)                                           | Falso     | **Entidad de certificación**                                 |
| [**CA-WEB-URL**](a-caweburl.md)                                          | Falso     | **Entidad de certificación**                                 |
| [**Lista de revocación de certificados**](a-certificaterevocationlist.md)        | Verdadero      | **Entidad de certificación**                                 |
| [**Plantillas de certificado**](a-certificatetemplates.md)                   | Falso     | **Entidad de certificación**                                 |
| [**Nombre común**](a-cn.md)                                               | Verdadero      | **Entidad de certificación** [ **superior**](c-top.md)<br/> |
| [**Crear marca de tiempo**](a-createtimestamp.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**CRL-Object**](a-crlobject.md)                                         | Falso     | **Entidad de certificación**                                 |
| [**Par de certificados cruzados**](a-crosscertificatepair.md)                  | Falso     | **Entidad de certificación**                                 |
| [**Current-Parent-CA**](a-currentparentca.md)                            | Falso     | **Entidad de certificación**                                 |
| [**Delta-Revocation-List**](a-deltarevocationlist.md)                    | Falso     | **Entidad de certificación**                                 |
| [**Descripción**](a-description.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Nombre para mostrar**](a-displayname.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DNS-Host-Name**](a-dnshostname.md)                                    | Falso     | **Entidad de certificación**                                 |
| [**Id. de dominio**](a-domainid.md)                                           | Falso     | **Entidad de certificación**                                 |
| [**Domain-Policy-Object**](a-domainpolicyobject.md)                      | Falso     | **Entidad de certificación**                                 |
| [**Firma DSA**](a-dsasignature.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Proveedores de inscripción**](a-enrollmentproviders.md)                     | Falso     | **Entidad de certificación**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Banderas**](a-flags.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Desde entrada**](a-fromentry.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Tipo de instancia**](a-instancetype.md)                                   | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Se elimina**](a-isdeleted.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Último elemento primario conocido**](a-lastknownparent.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos administrados**](a-managedobjects.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mastered-By**](a-masteredby.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                  | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Category**](a-objectcategory.md)                               | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Class**](a-objectclass.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Guid de objeto**](a-objectguid.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Version**](a-objectversion.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Entidad de certificación principal**](a-parentca.md)                                           | Falso     | **Entidad de certificación**                                 |
| [**Cadena de certificados de entidad de certificación primaria**](a-parentcacertificatechain.md)         | Falso     | **Entidad de certificación**                                 |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md) | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Pending-CA-Certificates**](a-pendingcacertificates.md)                | Falso     | **Entidad de certificación**                                 |
| [**Pending-Parent-CA**](a-pendingparentca.md)                            | Falso     | **Entidad de certificación**                                 |
| [**Posibles inferiores**](a-possibleinferiors.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Certificados de entidad de certificación anteriores**](a-previouscacertificates.md)              | Falso     | **Entidad de certificación**                                 |
| [**Entidad de certificación principal anterior**](a-previousparentca.md)                          | Falso     | **Entidad de certificación**                                 |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Direcciones de proxy**](a-proxyaddresses.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Rdn**](a-name.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Informes**](a-directreports.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-From**](a-repsfrom.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-To**](a-repsto.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Revisión**](a-revision.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Search-Guide**](a-searchguide.md)                                     | Falso     | **Entidad de certificación**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Algoritmos de firma**](a-signaturealgorithms.md)                     | Falso     | **Entidad de certificación**                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Sub refs**](a-subrefs.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Supported-Application-Context**](a-supportedapplicationcontext.md)    | Falso     | **Entidad de certificación**                                 |
| [**Marcas del sistema**](a-systemflags.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)        | Falso     | **Entidad de certificación**                                 |
| [**USN cambiado**](a-usnchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Creado por USN**](a-usncreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Intersite**](a-usnintersite.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Source**](a-usnsource.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Wbem-Path**](a-wbempath.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos conocidos**](a-wellknownobjects.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuando se crea**](a-whencreated.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Página principal**](a-wwwhomepage.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Page-Other**](a-url.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Atributos](#windows-server-2003-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 0                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.16                                                                                     |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**Contenedor**](c-container.md)                                                             |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Atributos de Server 2003

Esta clase contiene los atributos siguientes para Windows Server 2003:



| Atributo                                                                   | Mandatory | Derivado de                                                |
|-----------------------------------------------------------------------------|-----------|-------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Authority-Revocation-List**](a-authorityrevocationlist.md)              | Verdadero      | **Entidad de certificación**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Ca-Certificate**](a-cacertificate.md)                                   | Verdadero      | **Entidad de certificación**                                 |
| [**CA-Certificate-DN**](a-cacertificatedn.md)                              | Falso     | **Entidad de certificación**                                 |
| [**Ca-Conectar**](a-caconnect.md)                                           | Falso     | **Entidad de certificación**                                 |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Usos de CA**](a-causages.md)                                             | Falso     | **Entidad de certificación**                                 |
| [**CA-WEB-URL**](a-caweburl.md)                                            | Falso     | **Entidad de certificación**                                 |
| [**Certificate-Revocation-List**](a-certificaterevocationlist.md)          | Verdadero      | **Entidad de certificación**                                 |
| [**Plantillas de certificado**](a-certificatetemplates.md)                     | Falso     | **Entidad de certificación**                                 |
| [**Common-Name**](a-cn.md)                                                 | Verdadero      | **Entidad de certificación** [ **superior**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**CRL-Object**](a-crlobject.md)                                           | Falso     | **Entidad de certificación**                                 |
| [**Par de certificados cruzados**](a-crosscertificatepair.md)                    | Falso     | **Entidad de certificación**                                 |
| [**Current-Parent-CA**](a-currentparentca.md)                              | Falso     | **Entidad de certificación**                                 |
| [**Delta-Revocation-List**](a-deltarevocationlist.md)                      | Falso     | **Entidad de certificación**                                 |
| [**Descripción**](a-description.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DNS-Host-Name**](a-dnshostname.md)                                      | Falso     | **Entidad de certificación**                                 |
| [**Id. de dominio**](a-domainid.md)                                             | Falso     | **Entidad de certificación**                                 |
| [**Domain-Policy-Object**](a-domainpolicyobject.md)                        | Falso     | **Entidad de certificación**                                 |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Proveedores de inscripción**](a-enrollmentproviders.md)                       | Falso     | **Entidad de certificación**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Banderas**](a-flags.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Entidad de certificación principal**](a-parentca.md)                                             | Falso     | **Entidad de certificación**                                 |
| [**Parent-CA-Certificate-Chain**](a-parentcacertificatechain.md)           | Falso     | **Entidad de certificación**                                 |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Pending-CA-Certificates**](a-pendingcacertificates.md)                  | Falso     | **Entidad de certificación**                                 |
| [**Pending-Parent-CA**](a-pendingparentca.md)                              | Falso     | **Entidad de certificación**                                 |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Certificados de entidad de certificación anteriores**](a-previouscacertificates.md)                | Falso     | **Entidad de certificación**                                 |
| [**Previous-Parent-CA**](a-previousparentca.md)                            | Falso     | **Entidad de certificación**                                 |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Direcciones proxy**](a-proxyaddresses.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Informes**](a-directreports.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Search-Guide**](a-searchguide.md)                                       | Falso     | **Entidad de certificación**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Algoritmos de firma**](a-signaturealgorithms.md)                       | Falso     | **Entidad de certificación**                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Supported-Application-Context**](a-supportedapplicationcontext.md)      | Falso     | **Entidad de certificación**                                 |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Entidad de certificación**                                 |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Creado por USN**](a-usncreated.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos conocidos**](a-wellknownobjects.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Atributos](#windows-server-2003-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 0                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.16                                                                                     |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**Contenedor**](c-container.md)                                                             |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Atributos de Server 2003 R2

Esta clase contiene los atributos siguientes para Windows Server 2003 R2:



| Atributo                                                                   | Mandatory | Derivado de                                                |
|-----------------------------------------------------------------------------|-----------|-------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Atributos permitidos**](a-allowedattributes.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Authority-Revocation-List**](a-authorityrevocationlist.md)              | Verdadero      | **Entidad de certificación**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Ca-Certificate**](a-cacertificate.md)                                   | Verdadero      | **Entidad de certificación**                                 |
| [**CA-Certificate-DN**](a-cacertificatedn.md)                              | Falso     | **Entidad de certificación**                                 |
| [**Ca-Conectar**](a-caconnect.md)                                           | Falso     | **Entidad de certificación**                                 |
| [**Canonical-Name**](a-canonicalname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Usos de CA**](a-causages.md)                                             | Falso     | **Entidad de certificación**                                 |
| [**CA-WEB-URL**](a-caweburl.md)                                            | Falso     | **Entidad de certificación**                                 |
| [**Lista de revocación de certificados**](a-certificaterevocationlist.md)          | Verdadero      | **Entidad de certificación**                                 |
| [**Plantillas de certificado**](a-certificatetemplates.md)                     | Falso     | **Entidad de certificación**                                 |
| [**Common-Name**](a-cn.md)                                                 | Verdadero      | **Entidad de certificación** [ **superior**](c-top.md)<br/> |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**CRL-Object**](a-crlobject.md)                                           | Falso     | **Entidad de certificación**                                 |
| [**Par de certificados cruzados**](a-crosscertificatepair.md)                    | Falso     | **Entidad de certificación**                                 |
| [**Current-Parent-CA**](a-currentparentca.md)                              | Falso     | **Entidad de certificación**                                 |
| [**Delta-Revocation-List**](a-deltarevocationlist.md)                      | Falso     | **Entidad de certificación**                                 |
| [**Descripción**](a-description.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Nombre para mostrar**](a-displayname.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DNS-Host-Name**](a-dnshostname.md)                                      | Falso     | **Entidad de certificación**                                 |
| [**Id. de dominio**](a-domainid.md)                                             | Falso     | **Entidad de certificación**                                 |
| [**Domain-Policy-Object**](a-domainpolicyobject.md)                        | Falso     | **Entidad de certificación**                                 |
| [**Firma DSA**](a-dsasignature.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Proveedores de inscripción**](a-enrollmentproviders.md)                       | Falso     | **Entidad de certificación**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Banderas**](a-flags.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Desde entrada**](a-fromentry.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Tipo de instancia**](a-instancetype.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Se elimina**](a-isdeleted.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Último elemento primario conocido**](a-lastknownparent.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos administrados**](a-managedobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mastered-By**](a-masteredby.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md) | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                    | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Category**](a-objectcategory.md)                                 | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Class**](a-objectclass.md)                                       | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Guid de objeto**](a-objectguid.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Version**](a-objectversion.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Entidad de certificación principal**](a-parentca.md)                                             | Falso     | **Entidad de certificación**                                 |
| [**Cadena de certificados de entidad de certificación primaria**](a-parentcacertificatechain.md)           | Falso     | **Entidad de certificación**                                 |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Pending-CA-Certificates**](a-pendingcacertificates.md)                  | Falso     | **Entidad de certificación**                                 |
| [**Pending-Parent-CA**](a-pendingparentca.md)                              | Falso     | **Entidad de certificación**                                 |
| [**Posibles inferiores**](a-possibleinferiors.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Certificados de entidad de certificación anteriores**](a-previouscacertificates.md)                | Falso     | **Entidad de certificación**                                 |
| [**Entidad de certificación principal anterior**](a-previousparentca.md)                            | Falso     | **Entidad de certificación**                                 |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Rdn**](a-name.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Informes**](a-directreports.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-From**](a-repsfrom.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-To**](a-repsto.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Revisión**](a-revision.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Search-Guide**](a-searchguide.md)                                       | Falso     | **Entidad de certificación**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Algoritmos de firma**](a-signaturealgorithms.md)                       | Falso     | **Entidad de certificación**                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Sub refs**](a-subrefs.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Supported-Application-Context**](a-supportedapplicationcontext.md)      | Falso     | **Entidad de certificación**                                 |
| [**Marcas del sistema**](a-systemflags.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)          | Falso     | **Entidad de certificación**                                 |
| [**USN cambiado**](a-usnchanged.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**UsN creado**](a-usncreated.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Intersite**](a-usnintersite.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Source**](a-usnsource.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Wbem-Path**](a-wbempath.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos conocidos**](a-wellknownobjects.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuando se crea**](a-whencreated.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Página principal**](a-wwwhomepage.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Page-Other**](a-url.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Atributos](#windows-server-2008-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 0                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.16                                                                                     |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**Contenedor**](c-container.md)                                                             |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Atributos de Server 2008

Esta clase contiene los siguientes atributos para Windows Server 2008:



| Atributo                                                                      | Mandatory | Derivado de                                                |
|--------------------------------------------------------------------------------|-----------|-------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Atributos permitidos**](a-allowedattributes.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Authority-Revocation-List**](a-authorityrevocationlist.md)                 | Verdadero      | **Entidad de certificación**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Ca-Certificate**](a-cacertificate.md)                                      | Verdadero      | **Entidad de certificación**                                 |
| [**CA-Certificate-DN**](a-cacertificatedn.md)                                 | Falso     | **Entidad de certificación**                                 |
| [**Ca-Conectar**](a-caconnect.md)                                              | Falso     | **Entidad de certificación**                                 |
| [**Canonical-Name**](a-canonicalname.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Usos de CA**](a-causages.md)                                                | Falso     | **Entidad de certificación**                                 |
| [**CA-WEB-URL**](a-caweburl.md)                                               | Falso     | **Entidad de certificación**                                 |
| [**Certificate-Revocation-List**](a-certificaterevocationlist.md)             | Verdadero      | **Entidad de certificación**                                 |
| [**Plantillas de certificado**](a-certificatetemplates.md)                        | Falso     | **Entidad de certificación**                                 |
| [**Common-Name**](a-cn.md)                                                    | Verdadero      | **Entidad de certificación** [ **superior**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**CRL-Object**](a-crlobject.md)                                              | Falso     | **Entidad de certificación**                                 |
| [**Par de certificados cruzados**](a-crosscertificatepair.md)                       | Falso     | **Entidad de certificación**                                 |
| [**Current-Parent-CA**](a-currentparentca.md)                                 | Falso     | **Entidad de certificación**                                 |
| [**Delta-Revocation-List**](a-deltarevocationlist.md)                         | Falso     | **Entidad de certificación**                                 |
| [**Descripción**](a-description.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Nombre para mostrar**](a-displayname.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DNS-Host-Name**](a-dnshostname.md)                                         | Falso     | **Entidad de certificación**                                 |
| [**Id. de dominio**](a-domainid.md)                                                | Falso     | **Entidad de certificación**                                 |
| [**Domain-Policy-Object**](a-domainpolicyobject.md)                           | Falso     | **Entidad de certificación**                                 |
| [**Firma DSA**](a-dsasignature.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Proveedores de inscripción**](a-enrollmentproviders.md)                          | Falso     | **Entidad de certificación**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Banderas**](a-flags.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Desde entrada**](a-fromentry.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Tipo de instancia**](a-instancetype.md)                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Se elimina**](a-isdeleted.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos administrados**](a-managedobjects.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mastered-By**](a-masteredby.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md) | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                       | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Category**](a-objectcategory.md)                                    | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Class**](a-objectclass.md)                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Guid de objeto**](a-objectguid.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Version**](a-objectversion.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Otros objetos well-known-objects**](a-otherwellknownobjects.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Entidad de certificación principal**](a-parentca.md)                                                | Falso     | **Entidad de certificación**                                 |
| [**Cadena de certificados de entidad de certificación primaria**](a-parentcacertificatechain.md)              | Falso     | **Entidad de certificación**                                 |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Pending-CA-Certificates**](a-pendingcacertificates.md)                     | Falso     | **Entidad de certificación**                                 |
| [**Pending-Parent-CA**](a-pendingparentca.md)                                 | Falso     | **Entidad de certificación**                                 |
| [**Posibles inferiores**](a-possibleinferiors.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Certificados de entidad de certificación anteriores**](a-previouscacertificates.md)                   | Falso     | **Entidad de certificación**                                 |
| [**Entidad de certificación principal anterior**](a-previousparentca.md)                               | Falso     | **Entidad de certificación**                                 |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Direcciones de proxy**](a-proxyaddresses.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Rdn**](a-name.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Informes**](a-directreports.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-From**](a-repsfrom.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-To**](a-repsto.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Revisión**](a-revision.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Search-Guide**](a-searchguide.md)                                          | Falso     | **Entidad de certificación**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Algoritmos de firma**](a-signaturealgorithms.md)                          | Falso     | **Entidad de certificación**                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Sub refs**](a-subrefs.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Supported-Application-Context**](a-supportedapplicationcontext.md)         | Falso     | **Entidad de certificación**                                 |
| [**Marcas del sistema**](a-systemflags.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)             | Falso     | **Entidad de certificación**                                 |
| [**USN cambiado**](a-usnchanged.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Creado por USN**](a-usncreated.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Intersite**](a-usnintersite.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Source**](a-usnsource.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Wbem-Path**](a-wbempath.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos conocidos**](a-wellknownobjects.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuando se crea**](a-whencreated.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Página principal**](a-wwwhomepage.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Page-Other**](a-url.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                             |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Atributos](#windows-server-2008-r2-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 0                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.16                                                                                     |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**Contenedor**](c-container.md)                                                             |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Atributos de Server 2008 R2

Esta clase contiene los atributos siguientes para Windows Server 2008 R2:



| Atributo                                                                        | Mandatory | Derivado de                                                |
|----------------------------------------------------------------------------------|-----------|-------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Atributos permitidos**](a-allowedattributes.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Authority-Revocation-List**](a-authorityrevocationlist.md)                   | Verdadero      | **Entidad de certificación**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**CERTIFICADO DE ENTIDAD DE CERTIFICACIÓN**](a-cacertificate.md)                                        | Verdadero      | **Entidad de certificación**                                 |
| [**CA-Certificate-DN**](a-cacertificatedn.md)                                   | Falso     | **Entidad de certificación**                                 |
| [**Ca-Conectar**](a-caconnect.md)                                                | Falso     | **Entidad de certificación**                                 |
| [**Canonical-Name**](a-canonicalname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Usos de CA**](a-causages.md)                                                  | Falso     | **Entidad de certificación**                                 |
| [**CA-WEB-URL**](a-caweburl.md)                                                 | Falso     | **Entidad de certificación**                                 |
| [**Lista de revocación de certificados**](a-certificaterevocationlist.md)               | Verdadero      | **Entidad de certificación**                                 |
| [**Plantillas de certificado**](a-certificatetemplates.md)                          | Falso     | **Entidad de certificación**                                 |
| [**Common-Name**](a-cn.md)                                                      | Verdadero      | **Entidad de certificación** [ **superior**](c-top.md)<br/> |
| [**Marca de tiempo de creación**](a-createtimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**CRL-Object**](a-crlobject.md)                                                | Falso     | **Entidad de certificación**                                 |
| [**Par de certificados cruzados**](a-crosscertificatepair.md)                         | Falso     | **Entidad de certificación**                                 |
| [**Current-Parent-CA**](a-currentparentca.md)                                   | Falso     | **Entidad de certificación**                                 |
| [**Delta-Revocation-List**](a-deltarevocationlist.md)                           | Falso     | **Entidad de certificación**                                 |
| [**Descripción**](a-description.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Nombre para mostrar**](a-displayname.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Nombre para mostrar imprimible**](a-displaynameprintable.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DNS-Host-Name**](a-dnshostname.md)                                           | Falso     | **Entidad de certificación**                                 |
| [**Id. de dominio**](a-domainid.md)                                                  | Falso     | **Entidad de certificación**                                 |
| [**Domain-Policy-Object**](a-domainpolicyobject.md)                             | Falso     | **Entidad de certificación**                                 |
| [**Firma DSA**](a-dsasignature.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Proveedores de inscripción**](a-enrollmentproviders.md)                            | Falso     | **Entidad de certificación**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Banderas**](a-flags.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Desde entrada**](a-fromentry.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Tipo de instancia**](a-instancetype.md)                                          | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Se elimina**](a-isdeleted.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Se recicla**](a-isrecycled.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos administrados**](a-managedobjects.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mastered-By**](a-masteredby.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Modify-Time-Stamp**](a-modifytimestamp.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md) | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                         | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Category**](a-objectcategory.md)                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Class**](a-objectclass.md)                                            | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Guid de objeto**](a-objectguid.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Version**](a-objectversion.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Entidad de certificación principal**](a-parentca.md)                                                  | Falso     | **Entidad de certificación**                                 |
| [**Parent-CA-Certificate-Chain**](a-parentcacertificatechain.md)                | Falso     | **Entidad de certificación**                                 |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Pending-CA-Certificates**](a-pendingcacertificates.md)                       | Falso     | **Entidad de certificación**                                 |
| [**Pending-Parent-CA**](a-pendingparentca.md)                                   | Falso     | **Entidad de certificación**                                 |
| [**Posibles inferiores**](a-possibleinferiors.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Certificados de entidad de certificación anteriores**](a-previouscacertificates.md)                     | Falso     | **Entidad de certificación**                                 |
| [**Previous-Parent-CA**](a-previousparentca.md)                                 | Falso     | **Entidad de certificación**                                 |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Direcciones proxy**](a-proxyaddresses.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Rdn**](a-name.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Informes**](a-directreports.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-From**](a-repsfrom.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-To**](a-repsto.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Revisión**](a-revision.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Search-Guide**](a-searchguide.md)                                            | Falso     | **Entidad de certificación**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mostrar solo en vista avanzada**](a-showinadvancedviewonly.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Algoritmos de firma**](a-signaturealgorithms.md)                            | Falso     | **Entidad de certificación**                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Sub refs**](a-subrefs.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Supported-Application-Context**](a-supportedapplicationcontext.md)           | Falso     | **Entidad de certificación**                                 |
| [**Marcas del sistema**](a-systemflags.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)               | Falso     | **Entidad de certificación**                                 |
| [**USN cambiado**](a-usnchanged.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**UsN creado**](a-usncreated.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Intersite**](a-usnintersite.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Source**](a-usnsource.md)                                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Wbem-Path**](a-wbempath.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Well-Known-Objects**](a-wellknownobjects.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuando se crea**](a-whencreated.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**PÁGINA PRINCIPAL DE WWW**](a-wwwhomepage.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Page-Other**](a-url.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Atributos](#windows-server-2012-attributes)



| Entrada | Value |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Falso                                                                                        |
| Object-Category             | 0                                                                                            |
| Default-Object-Category     | \-                                                                                           |
| Governs-Id                  | 2.5.6.16                                                                                     |
| Valor predeterminado de ocultación        | 1                                                                                            |
| Rdn-Att-Id                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Subclase de                 | [**Arriba**](c-top.md)<br/>                                                              |
| Posibles superiores          | [**Contenedor**](c-container.md)                                                             |
| Clases auxiliares           | \-                                                                                           |
| NT-Security-Descriptor      | O:BAG:BAD:S:                                                                                 |
| Descriptor de seguridad predeterminado | D:(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;;D A)(A;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY)(A;; RPLCLORC;;; AU) |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Atributos

Esta clase contiene los siguientes atributos para Windows Server 2012:



| Atributo                                                                                    | Mandatory | Derivado de                                                |
|----------------------------------------------------------------------------------------------|-----------|-------------------------------------------------------------|
| [**Admin-Description**](a-admindescription.md)                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Atributos permitidos**](a-allowedattributes.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Attributes-Effective**](a-allowedattributeseffective.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes**](a-allowedchildclasses.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Allowed-Child-Classes-Effective**](a-allowedchildclasseseffective.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Authority-Revocation-List**](a-authorityrevocationlist.md)                               | Verdadero      | **Entidad de certificación**                                 |
| [**Bridgehead-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Ca-Certificate**](a-cacertificate.md)                                                    | Verdadero      | **Entidad de certificación**                                 |
| [**CA-Certificate-DN**](a-cacertificatedn.md)                                               | Falso     | **Entidad de certificación**                                 |
| [**Ca-Conectar**](a-caconnect.md)                                                            | Falso     | **Entidad de certificación**                                 |
| [**Canonical-Name**](a-canonicalname.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Usos de CA**](a-causages.md)                                                              | Falso     | **Entidad de certificación**                                 |
| [**CA-WEB-URL**](a-caweburl.md)                                                             | Falso     | **Entidad de certificación**                                 |
| [**Certificate-Revocation-List**](a-certificaterevocationlist.md)                           | Verdadero      | **Entidad de certificación**                                 |
| [**Plantillas de certificado**](a-certificatetemplates.md)                                      | Falso     | **Entidad de certificación**                                 |
| [**Common-Name**](a-cn.md)                                                                  | Verdadero      | **Entidad de certificación** [ **superior**](c-top.md)<br/> |
| [**Create-Time-Stamp**](a-createtimestamp.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**CRL-Object**](a-crlobject.md)                                                            | Falso     | **Entidad de certificación**                                 |
| [**Par de certificados cruzados**](a-crosscertificatepair.md)                                     | Falso     | **Entidad de certificación**                                 |
| [**Current-Parent-CA**](a-currentparentca.md)                                               | Falso     | **Entidad de certificación**                                 |
| [**Delta-Revocation-List**](a-deltarevocationlist.md)                                       | Falso     | **Entidad de certificación**                                 |
| [**Descripción**](a-description.md)                                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Nombre para mostrar**](a-displayname.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Display-Name-Printable**](a-displaynameprintable.md)                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DNS-Host-Name**](a-dnshostname.md)                                                       | Falso     | **Entidad de certificación**                                 |
| [**Id. de dominio**](a-domainid.md)                                                              | Falso     | **Entidad de certificación**                                 |
| [**Domain-Policy-Object**](a-domainpolicyobject.md)                                         | Falso     | **Entidad de certificación**                                 |
| [**Firma DSA**](a-dsasignature.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**DS-Core-Propagation-Data**](a-dscorepropagationdata.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Proveedores de inscripción**](a-enrollmentproviders.md)                                        | Falso     | **Entidad de certificación**                                 |
| [**Nombre de extensión**](a-extensionname.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Banderas**](a-flags.md)                                                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Desde entrada**](a-fromentry.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Frs-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Tipo de instancia**](a-instancetype.md)                                                      | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Se elimina**](a-isdeleted.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Member-Of-DL**](a-memberof.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Is-Privilege-Holder**](a-isprivilegeholder.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Se recicla**](a-isrecycled.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Último elemento primario conocido**](a-lastknownparent.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos administrados**](a-managedobjects.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Mastered-By**](a-masteredby.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Modificación de marca de tiempo**](a-modifytimestamp.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-COM-UserLink**](a-mscom-userlink.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Approx-Immed-Subordinates**](a-msds-approx-immed-subordinates.md)                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-AuthenticatedTo-Accountlist**](a-msds-authenticatedtoaccountlist.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Claim-Shares-Possible-Values-With-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Child-Count**](a-ms-ds-consistencychildcount.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Enabled-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Domain-For**](a-msds-isdomainfor.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Full-Replica-For**](a-msds-isfullreplicafor.md)                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Partial-Replica-For**](a-msds-ispartialreplicafor.md)                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Is-Primary-Computer-For**](a-msds-isprimarycomputerfor.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-local-Effective-Deletion-Time**](a-msds-localeffectivedeletiontime.md)             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-local-Effective-Recycle-Time**](a-msds-localeffectiverecycletime.md)               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Mastered-By**](a-msds-masteredby.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Members-For-Az-Role-BL**](a-msds-membersforazrolebl.md)                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Members-Of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Cursors**](a-msds-ncreplcursors.md)                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Inbound-Neighbors**](a-msds-ncreplinboundneighbors.md)                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Repl-Outbound-Neighbors**](a-msds-ncreploutboundneighbors.md)                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-NC-Type**](a-msds-nctype.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Non-Members-BL**](a-msds-nonmembersbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Role-BL**](a-msds-operationsforazrolebl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Operations-For-Az-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Principal-Name**](a-msds-principalname.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-PSO-Applied**](a-msds-psoapplied.md)                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Repl-Value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Revealed-DSA**](a-msds-revealeddsas.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Revealed-List-BL**](a-msds-revealedlistbl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Role-BL**](a-msds-tasksforazrolebl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Tasks-For-Az-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-TDO-Ingress-BL**](a-msds-tdoingressbl.md)                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-DS-Value-Type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**ms-Exch-Owner-BL**](a-ownerbl.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**msSFU-30-Posix-Member-Of**](a-mssfu30posixmemberof.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Miembro no de seguridad-BL**](a-nonsecuritymemberbl.md)                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md)                                     | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Category**](a-objectcategory.md)                                                  | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Class**](a-objectclass.md)                                                        | Verdadero      | [**Arriba**](c-top.md)<br/>                             |
| [**Guid de objeto**](a-objectguid.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Object-Version**](a-objectversion.md)                                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Otros objetos conocidos**](a-otherwellknownobjects.md)                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Entidad de certificación principal**](a-parentca.md)                                                              | Falso     | **Entidad de certificación**                                 |
| [**Parent-CA-Certificate-Chain**](a-parentcacertificatechain.md)                            | Falso     | **Entidad de certificación**                                 |
| [**Partial-Attribute-Deletion-List**](a-partialattributedeletionlist.md)                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Partial-Attribute-Set**](a-partialattributeset.md)                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Pending-CA-Certificates**](a-pendingcacertificates.md)                                   | Falso     | **Entidad de certificación**                                 |
| [**Pending-Parent-CA**](a-pendingparentca.md)                                               | Falso     | **Entidad de certificación**                                 |
| [**Posibles inferiores**](a-possibleinferiors.md)                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Certificados de entidad de certificación anteriores**](a-previouscacertificates.md)                                 | Falso     | **Entidad de certificación**                                 |
| [**Previous-Parent-CA**](a-previousparentca.md)                                             | Falso     | **Entidad de certificación**                                 |
| [**Proxied-Object-Name**](a-proxiedobjectname.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Direcciones proxy**](a-proxyaddresses.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Query-Policy-BL**](a-querypolicybl.md)                                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Rdn**](a-name.md)                                                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Repl-UpToDate-Vector**](a-repluptodatevector.md)                                         | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Informes**](a-directreports.md)                                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-From**](a-repsfrom.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Reps-To**](a-repsto.md)                                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Revisión**](a-revision.md)                                                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SD-Rights-Effective**](a-sdrightseffective.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Search-Guide**](a-searchguide.md)                                                        | Falso     | **Entidad de certificación**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Show-In-Advanced-View-Only**](a-showinadvancedviewonly.md)                               | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Algoritmos de firma**](a-signaturealgorithms.md)                                        | Falso     | **Entidad de certificación**                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Sub refs**](a-subrefs.md)                                                                | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Supported-Application-Context**](a-supportedapplicationcontext.md)                       | Falso     | **Entidad de certificación**                                 |
| [**Marcas del sistema**](a-systemflags.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Teletex-Terminal-Identifier**](a-teletexterminalidentifier.md)                           | Falso     | **Entidad de certificación**                                 |
| [**USN cambiado**](a-usnchanged.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Creado por USN**](a-usncreated.md)                                                          | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-DSA-Last-Obj-Removed**](a-usndsalastobjremoved.md)                                   | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Intersite**](a-usnintersite.md)                                                      | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Last-Obj-Rem**](a-usnlastobjrem.md)                                                  | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**USN-Source**](a-usnsource.md)                                                            | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Wbem-Path**](a-wbempath.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Objetos conocidos**](a-wellknownobjects.md)                                             | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuándo se ha cambiado**](a-whenchanged.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**Cuando se crea**](a-whencreated.md)                                                        | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Página principal**](a-wwwhomepage.md)                                                       | Falso     | [**Arriba**](c-top.md)<br/>                             |
| [**WWW-Page-Other**](a-url.md)                                                              | Falso     | [**Arriba**](c-top.md)<br/>                             |



 

 





