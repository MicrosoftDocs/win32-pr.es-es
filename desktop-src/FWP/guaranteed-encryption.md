---
title: Cifrado garantizado
description: El escenario de directiva IPsec de cifrado garantizado requiere cifrado IPsec para todo el tráfico correspondiente. Esta directiva debe especificarse junto con una de las opciones de directiva de modo de transporte.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d029b3bebc6fc6e0a438c5123bb6703bc45dd457195fa7ff8fc7268bba16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069155"
---
# <a name="guaranteed-encryption"></a>Cifrado garantizado

El escenario de directiva IPsec de cifrado garantizado requiere cifrado IPsec para todo el tráfico correspondiente. Esta directiva debe especificarse junto con una de las opciones de directiva de modo de transporte.

El cifrado garantizado se usa normalmente para cifrar el tráfico confidencial por aplicación.

Un ejemplo de un posible escenario de cifrado garantizado es "Proteger todo el tráfico de datos de unidifusión, excepto ICMP, usar el modo de transporte IPsec, habilitar la detección de negociación y requerir cifrado garantizado para todo el tráfico de unidifusión correspondiente al puerto local TCP 5555".

Para implementar este ejemplo mediante programación, use la siguiente configuración de WFP.

<dl>

**En FWPM \_ LAYER \_ IXTXT \_ V{4 \| 6} configuración de la directiva de negociación mm**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas MM.  
    -   Para IKE, un contexto de proveedor de directivas de tipo FWPM \_ \_ IPSEC IKE \_ MM \_ CONTEXT.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT.

    > [!Note]  
    > Se negociará un módulo de claves común y se aplicará la directiva MM correspondiente. AuthIP es el módulo de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.

    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor mm agregado en el paso 1. |

        

**En FWPM \_ LAYER \_ IPSEC \_ V{4 6} setup QM and EM negotiation policy (Directiva de negociación de QM y EM de FWPM LAYER IPSEC V{4 \| 6} )**  

1.  Agregue uno o ambos de los siguientes contextos de proveedor de directivas de modo de transporte QM y establezca la marca ND SECURE de [**\_ \_ \_ IPSEC \_ POLICY FLAG.**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)  
    -   Para IKE, un contexto de proveedor de directivas de tipo **FWPM \_ \_ IPSEC IKE \_ QM \_ TRANSPORT \_ CONTEXT**.
    -   Para AuthIP, un contexto de proveedor de directivas de tipo **FWPM \_ IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT**. Opcionalmente, este contexto puede contener la directiva de negociación del modo extendido AuthIP (EM).

    > [!Note]  
    > Se negociará un módulo de claves común y se aplicará la directiva QM correspondiente. AuthIP es el módulo de claves preferido si se admiten IKE y AuthIP.

     

2.  Para cada uno de los contextos agregados en el paso 1, agregue un filtro con las siguientes propiedades.

    | Propiedad Filter        | Value                                            |
    |------------------------|--------------------------------------------------|
    | Condiciones de filtrado   | Vacía. Todo el tráfico coincidirá con el filtro.        |
    | **providerContextKey** | GUID del contexto del proveedor QM agregado en el paso 1. |

        

**En FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6} configure reglas de filtrado de entrada por paquete**  

1.  Agregue un filtro con las siguientes propiedades. 

    | Propiedad Filter                                               | Value                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | Condición de filtrado \_ FWPM CONDITION \_ IP LOCAL \_ ADDRESS \_ \_ TYPE | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action.type**                                               | **TERMINACIÓN DE LLAMADA \_ \_ DE ACCIÓN \_ FWP**                                                              |
    | **action.calloutKey**                                         | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TRANSPORT \_ \_ V{4 \| 6}**                                              |
    | **rawContext**                                                | [**FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PERSIST \_ CONNECTION \_ SECURITY**](filter-context-identifiers.md) |

        
2.  Excón el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ CONDICIÓN \_ Condición de filtrado de IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISO DE \_ ACCIÓN FWP \_**                                                    |
    | **weight**                                                        | [**EXENCIONES DE IKE DEL INTERVALO DE PESO FWPM \_ \_ \_ \_**](filter-weight-identifiers.md)  |

        

**En FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} configure las reglas de filtrado de salida por paquete**  

1.  Agregue un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                               |
    | **action.type**                                                   | **TERMINACIÓN DE LLAMADA \_ \_ DE ACCIÓN \_ FWP**                                                     |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}**                                    |
    | **rawContext**                                                    | [**DESCUCIÓN \_ DE \_ NEGOCIACIÓN SALIENTE DE IPSEC DE CONTEXTO \_ \_ FWPM \_**](filter-context-identifiers.md) |

        
2.  Excón el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ CONDICIÓN \_ Condición de filtrado de IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **PERMISO DE \_ ACCIÓN FWP \_**                                                    |
    | **weight**                                                        | **EXENCIONES DE IKE DEL INTERVALO DE PESO FWPM \_ \_ \_ \_**                                   |

        

**En FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} setup inbound per-connection filtering rules**  

1.  Agregue un filtro con las siguientes propiedades. Este filtro solo permitirá los intentos de conexión entrantes si IPsec los protege. 

    | Propiedad Filter                                                   | Value                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                  |
    | **action.type**                                                   | **TERMINACIÓN DE LLAMADA \_ \_ DE ACCIÓN \_ FWP**                        |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND INITIATE SECURE \_ \_ \_ V{4 \| 6}** |

        
2.  Excón el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.

    | Propiedad Filter                                                   | Value                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condición \_ de filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Estas constantes se definen en winsock2.h.<br/> |
    | **action.type**                                                   | **FWP \_ ACTION \_ PERMIT**                                                    |
    | **weight**                                                        | **EXENCIONES \_ DE \_ \_ IKE DE \_ INTERVALO DE PESO FWPM**                                   |

        
3.  Agregue un filtro con las siguientes propiedades. Este filtro solo permitirá conexiones entrantes al puerto TCP 5555 si están cifradas.

    | Propiedad Filter                                                   | Value                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                                           |
    | **FWPM \_ Condición \_ de filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ TCP** Esta constante se define en winsock2.h.<br/>                                    |
    | **FWPM \_ Condición de \_ filtrado de PUERTO LOCAL \_ \_ DE** LA DIRECCIÓN IP DE CONDICIÓN          | 5555                                                                                                  |
    | **action.type**                                                   | **TERMINACIÓN DE \_ LLAMADA \_ DE ACCIÓN \_ FWP**                                                                 |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ INBOUND INITIATE SECURE \_ \_ \_ V{4 \| 6}**                                          |
    | **rawContext**                                                    | [**LA CONEXIÓN DE CONJUNTO DE ALE DE CONTEXTO \_ \_ \_ \_ FWPM REQUIERE \_ CIFRADO \_ \_ IPSEC**](filter-context-identifiers.md) |

        

**En FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6} configure reglas de filtrado de salida por conexión**

-   Agregue un filtro con las siguientes propiedades. Este filtro solo permitirá conexiones salientes desde el puerto TCP 5555 si están cifradas.

    | Propiedad Filter                                                   | Value                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condición de \_ filtrado CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                                           |
    | **FWPM \_ Condición \_ de filtrado de CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ TCP** Esta constante se define en winsock2.h.<br/>                                    |
    | **FWPM \_ Condición de \_ filtrado de PUERTO LOCAL \_ \_ DE** LA DIRECCIÓN IP DE CONDICIÓN          | 5555                                                                                                  |
    | **action.type**                                                   | **TERMINACIÓN DE \_ LLAMADA \_ DE ACCIÓN \_ FWP**                                                                 |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ ALE \_ CONNECT \_ V{4 \| 6}**                                                       |
    | **rawContext**                                                    | [**LA CONEXIÓN DE CONJUNTO DE ALE DE CONTEXTO \_ \_ \_ \_ FWPM REQUIERE \_ CIFRADO \_ \_ IPSEC**](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Código de ejemplo: Uso del modo de transporte](using-transport-mode.md)
</dt> <dt>

[Capas de ALE](ale-layers.md)
</dt> <dt>

[**Identificadores de llamada integrados**](built-in-callout-identifiers.md)
</dt> <dt>

[Condiciones de filtrado](filtering-conditions.md)
</dt> <dt>

[**Filtrado de identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**TIPO DE CONTEXTO \_ DEL \_ PROVEEDOR \_ FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

