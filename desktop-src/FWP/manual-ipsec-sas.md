---
title: SA manual
description: El escenario de la directiva IPsec de la Asociación de seguridad manual (SA) permite que los autores de llamadas omitan los módulos de creación de claves IPsec integrados (IKE y AuthIP) especificando directamente las SA de IPsec para proteger el tráfico de red.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161447ff5cfd98878ab4ee0f4b18cbcc3a53643
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995159"
---
# <a name="manual-sa"></a><span data-ttu-id="7ead1-103">SA manual</span><span class="sxs-lookup"><span data-stu-id="7ead1-103">Manual SA</span></span>

<span data-ttu-id="7ead1-104">El escenario de la directiva IPsec de la Asociación de seguridad manual (SA) permite que los autores de llamadas omitan los módulos de creación de claves IPsec integrados (IKE y AuthIP) especificando directamente las SA de IPsec para proteger el tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="7ead1-104">The Manual Security Association (SA) IPsec policy scenario allows callers to bypass the built-in IPsec keying modules (IKE and AuthIP) by directly specifying IPsec SAs to secure any network traffic.</span></span>

<span data-ttu-id="7ead1-105">Un ejemplo de un posible escenario de SA manual es "agregar un par de SA de IPsec para proteger todo el tráfico de datos de unidifusión entre & las direcciones IP de la 2.2.2.2, a excepción de ICMP, mediante el modo de transporte IPsec".</span><span class="sxs-lookup"><span data-stu-id="7ead1-105">An example of a possible Manual SA scenario is "Add an IPsec SA pair to secure all unicast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode."</span></span>

> [!Note]  
> <span data-ttu-id="7ead1-106">Los siguientes pasos deben ejecutarse en ambos equipos con direcciones IP establecidas correctamente.</span><span class="sxs-lookup"><span data-stu-id="7ead1-106">The following steps must be executed on both machines with IP addresses appropriately set.</span></span>

 

<span data-ttu-id="7ead1-107">Para implementar este ejemplo mediante programación, utilice la siguiente configuración de WFP.</span><span class="sxs-lookup"><span data-stu-id="7ead1-107">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="7ead1-108">**En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquete de entrada**</span><span class="sxs-lookup"><span data-stu-id="7ead1-108">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="7ead1-109">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ead1-109">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="7ead1-110">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="7ead1-110">Filter property</span></span>                                                   | <span data-ttu-id="7ead1-111">Value</span><span class="sxs-lookup"><span data-stu-id="7ead1-111">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="7ead1-112">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="7ead1-112">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="7ead1-113">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="7ead1-113">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="7ead1-114">**\_ \_ \_ dirección local IP de condición FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="7ead1-114">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS**</span></span>                           | <span data-ttu-id="7ead1-115">La dirección local adecuada (2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="7ead1-115">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>           |
    | <span data-ttu-id="7ead1-116">**\_ \_ \_ dirección remota IP de condición FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="7ead1-116">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS**</span></span>                          | <span data-ttu-id="7ead1-117">La dirección remota adecuada (2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="7ead1-117">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>          |
    | <span data-ttu-id="7ead1-118">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="7ead1-118">**action.type**</span></span>                                                   | <span data-ttu-id="7ead1-119">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="7ead1-119">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                         |
    | <span data-ttu-id="7ead1-120">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="7ead1-120">**action.calloutKey**</span></span>                                             | <span data-ttu-id="7ead1-121">**Llamada de FWPM de \_ \_ transporte de entrada de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="7ead1-121">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>         |

        
2.  <span data-ttu-id="7ead1-122">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ead1-122">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="7ead1-123">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="7ead1-123">Filter property</span></span>                                                   | <span data-ttu-id="7ead1-124">Value</span><span class="sxs-lookup"><span data-stu-id="7ead1-124">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="7ead1-125">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="7ead1-125">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="7ead1-126">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="7ead1-126">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="7ead1-127">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="7ead1-127">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="7ead1-128">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="7ead1-128">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="7ead1-129">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="7ead1-129">**action.type**</span></span>                                                   | <span data-ttu-id="7ead1-130">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="7ead1-130">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="7ead1-131">**weight**</span><span class="sxs-lookup"><span data-stu-id="7ead1-131">**weight**</span></span>                                                        | [<span data-ttu-id="7ead1-132">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="7ead1-132">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="7ead1-133">**En el nivel de FWPM de \_ \_ transporte de salida \_ \_ V {4 \| 6} configuración de reglas de filtrado por paquetes salientes**</span><span class="sxs-lookup"><span data-stu-id="7ead1-133">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="7ead1-134">Agregue un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ead1-134">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="7ead1-135">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="7ead1-135">Filter property</span></span>                                                   | <span data-ttu-id="7ead1-136">Value</span><span class="sxs-lookup"><span data-stu-id="7ead1-136">Value</span></span>                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="7ead1-137">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="7ead1-137">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="7ead1-138">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="7ead1-138">NlatUnicast</span></span>                                            |
    | <span data-ttu-id="7ead1-139">**FWPM \_ Condición de filtrado de \_ \_ \_ dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="7ead1-139">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS** filtering condition</span></span>       | <span data-ttu-id="7ead1-140">La dirección local adecuada (2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="7ead1-140">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>    |
    | <span data-ttu-id="7ead1-141">**FWPM \_ Condición de filtrado de \_ \_ \_ direcciones remotas IP de condición**</span><span class="sxs-lookup"><span data-stu-id="7ead1-141">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS** filtering condition</span></span>      | <span data-ttu-id="7ead1-142">La dirección remota adecuada (2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="7ead1-142">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>   |
    | <span data-ttu-id="7ead1-143">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="7ead1-143">**action.type**</span></span>                                                   | <span data-ttu-id="7ead1-144">**\_ \_ terminando llamada de acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="7ead1-144">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                  |
    | <span data-ttu-id="7ead1-145">**Action. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="7ead1-145">**action.calloutKey**</span></span>                                             | <span data-ttu-id="7ead1-146">**Llamada de FWPM de \_ \_ transporte de salida de IPSec \_ \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="7ead1-146">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="7ead1-147">Excluya el tráfico ICMP de IPsec agregando un filtro con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="7ead1-147">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="7ead1-148">Propiedad Filter</span><span class="sxs-lookup"><span data-stu-id="7ead1-148">Filter property</span></span>                                                   | <span data-ttu-id="7ead1-149">Value</span><span class="sxs-lookup"><span data-stu-id="7ead1-149">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="7ead1-150">**FWPM \_ Condición de filtrado de \_ \_ \_ \_ tipo de dirección local IP de condición**</span><span class="sxs-lookup"><span data-stu-id="7ead1-150">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="7ead1-151">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="7ead1-151">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="7ead1-152">**FWPM \_ Condición de filtrado de \_ \_ protocolo IP de condición**</span><span class="sxs-lookup"><span data-stu-id="7ead1-152">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="7ead1-153">**IPPROTO \_ ICMP {V6}** estas constantes se definen en WinSock2. h.</span><span class="sxs-lookup"><span data-stu-id="7ead1-153">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="7ead1-154">**Action. Type**</span><span class="sxs-lookup"><span data-stu-id="7ead1-154">**action.type**</span></span>                                                   | <span data-ttu-id="7ead1-155">**\_permitir acción de FWP \_**</span><span class="sxs-lookup"><span data-stu-id="7ead1-155">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="7ead1-156">**weight**</span><span class="sxs-lookup"><span data-stu-id="7ead1-156">**weight**</span></span>                                                        | <span data-ttu-id="7ead1-157">**\_ \_ exenciones IKE de intervalo de peso \_ de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="7ead1-157">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="7ead1-158">**Configuración de asociaciones de seguridad entrantes y salientes**</span><span class="sxs-lookup"><span data-stu-id="7ead1-158">**Setup inbound and outbound security associations**</span></span>

1.  <span data-ttu-id="7ead1-159">Llame a [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), con el parámetro *outboundTraffic* que contiene las direcciones IP como a la vez & 2.2.2.2 y **ipsecFilterId** como LUID del filtro de llamada IPSec de la capa de transporte saliente agregada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7ead1-159">Call [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), with the *outboundTraffic* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the outbound transport layer IPsec callout filter added above.</span></span>
2.  <span data-ttu-id="7ead1-160">Llame a [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), con el parámetro *ID* que contiene el ID. de contexto devuelto desde [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), y el parámetro *getSpi* que contiene las direcciones IP como el valor de la enumeración & 2.2.2.2 y **ipsecFilterId** como LUID del filtro de llamada IPSec de la capa de transporte de entrada agregada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7ead1-160">Call [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *getSpi* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the inbound transport layer IPsec callout filter added above.</span></span> <span data-ttu-id="7ead1-161">El valor de SPI devuelto está pensado para que lo use el equipo local y como el SPI de la SA de salida en el equipo remoto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7ead1-161">The returned SPI value is meant to be used as the inbound SA SPI by the local machine and as the outbound SA SPI by the corresponding remote machine.</span></span> <span data-ttu-id="7ead1-162">Ambos equipos deben usar algunos medios fuera de banda para intercambiar los valores de SPI.</span><span class="sxs-lookup"><span data-stu-id="7ead1-162">Both machines must use some out-of-band means to exchange the SPI values.</span></span>
3.  <span data-ttu-id="7ead1-163">Llame a [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), con el parámetro *ID* que contiene el identificador de contexto devuelto desde [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), y el parámetro *INBOUNDBUNDLE* que describe las propiedades del paquete SA entrante (por ejemplo, el SPI de SA entrante, el tipo de transformación, los tipos de algoritmo, las claves, etc.).</span><span class="sxs-lookup"><span data-stu-id="7ead1-163">Call [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *inboundBundle* parameter describing the properties of the inbound SA bundle (such as the inbound SA SPI, transform type, algorithm types, keys, etc).</span></span>
4.  <span data-ttu-id="7ead1-164">Llame a [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), con el parámetro *ID* que contiene el ID. de contexto devuelto desde [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), y el parámetro *OUTBOUNDBUNDLE* que describe las propiedades del paquete SA saliente (como el IRP de salida SA, el tipo de transformación, los tipos de algoritmo, las claves, etc.).</span><span class="sxs-lookup"><span data-stu-id="7ead1-164">Call [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *outboundBundle* parameter describing the properties of the outbound SA bundle (such as the outbound SA SPI, transform type, algorithm types, keys, etc).</span></span>

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="7ead1-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ead1-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ead1-166">Código de ejemplo: creación manual de claves SA</span><span class="sxs-lookup"><span data-stu-id="7ead1-166">Sample code: Manual SA Keying</span></span>](manual-sa-keying.md)
</dt> <dt>

[<span data-ttu-id="7ead1-167">**Identificadores de llamada integrados**</span><span class="sxs-lookup"><span data-stu-id="7ead1-167">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="7ead1-168">**Filtrado de identificadores de capas**</span><span class="sxs-lookup"><span data-stu-id="7ead1-168">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="7ead1-169">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="7ead1-169">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

