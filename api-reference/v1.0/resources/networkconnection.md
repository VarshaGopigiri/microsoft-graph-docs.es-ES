---
title: tipo de recurso networkConnection
description: Contiene información de estado acerca de la conexión de red relacionados con la alerta.
localization_priority: Normal
ms.openlocfilehash: 78ddcfd19d68b8dcd64c74a5beed6d1430f0ca38
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826512"
---
# <a name="networkconnection-resource-type"></a><span data-ttu-id="bb921-103">tipo de recurso networkConnection</span><span class="sxs-lookup"><span data-stu-id="bb921-103">networkConnection resource type</span></span>

<span data-ttu-id="bb921-104">Contiene información de estado acerca de la conexión de red relacionados con la alerta.</span><span class="sxs-lookup"><span data-stu-id="bb921-104">Contains stateful information about the network connection related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="bb921-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb921-105">Properties</span></span>

| <span data-ttu-id="bb921-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb921-106">Property</span></span>   | <span data-ttu-id="bb921-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb921-107">Type</span></span>|<span data-ttu-id="bb921-108">Description</span><span class="sxs-lookup"><span data-stu-id="bb921-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb921-109">applicationName</span><span class="sxs-lookup"><span data-stu-id="bb921-109">applicationName</span></span>|<span data-ttu-id="bb921-110">String</span><span class="sxs-lookup"><span data-stu-id="bb921-110">String</span></span>|<span data-ttu-id="bb921-111">Nombre de la aplicación de administración de la conexión de red (por ejemplo, Facebook, SMTP, etcetera).</span><span class="sxs-lookup"><span data-stu-id="bb921-111">Name of the application managing the network connection (for example, Facebook, SMTP, etc.).</span></span>|
|<span data-ttu-id="bb921-112">destinationAddress</span><span class="sxs-lookup"><span data-stu-id="bb921-112">destinationAddress</span></span>|<span data-ttu-id="bb921-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-113">String</span></span>|<span data-ttu-id="bb921-114">Dirección IP de destino (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="bb921-114">Destination IP address (of the network connection).</span></span>|
|<span data-ttu-id="bb921-115">destinationDomain</span><span class="sxs-lookup"><span data-stu-id="bb921-115">destinationDomain</span></span>|<span data-ttu-id="bb921-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-116">String</span></span>|<span data-ttu-id="bb921-117">Parte del dominio de destino de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="bb921-117">Destination domain portion of the destination URL.</span></span> <span data-ttu-id="bb921-118">(por ejemplo 'www.contoso.com').</span><span class="sxs-lookup"><span data-stu-id="bb921-118">(for example 'www.contoso.com').</span></span>|
|<span data-ttu-id="bb921-119">destinationPort</span><span class="sxs-lookup"><span data-stu-id="bb921-119">destinationPort</span></span>|<span data-ttu-id="bb921-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-120">String</span></span>|<span data-ttu-id="bb921-121">Puerto de destino (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="bb921-121">Destination port (of the network connection).</span></span>|
|<span data-ttu-id="bb921-122">destinationUrl</span><span class="sxs-lookup"><span data-stu-id="bb921-122">destinationUrl</span></span>|<span data-ttu-id="bb921-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-123">String</span></span>|<span data-ttu-id="bb921-124">Cadena de dirección URL o URI de conexión - excluyendo los parámetros de la red.</span><span class="sxs-lookup"><span data-stu-id="bb921-124">Network connection URL/URI string - excluding parameters.</span></span> <span data-ttu-id="bb921-125">(por ejemplo, 'www.contoso.com/products/default.html')</span><span class="sxs-lookup"><span data-stu-id="bb921-125">(for example 'www.contoso.com/products/default.html')</span></span>|
|<span data-ttu-id="bb921-126">dirección</span><span class="sxs-lookup"><span data-stu-id="bb921-126">direction</span></span>|<span data-ttu-id="bb921-127">connectionDirection</span><span class="sxs-lookup"><span data-stu-id="bb921-127">connectionDirection</span></span>|<span data-ttu-id="bb921-128">Dirección de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="bb921-128">Network connection direction.</span></span> <span data-ttu-id="bb921-129">Los valores posibles son: `unknown`, `inbound` y `outbound`.</span><span class="sxs-lookup"><span data-stu-id="bb921-129">Possible values are: `unknown`, `inbound`, `outbound`.</span></span>|
|<span data-ttu-id="bb921-130">domainRegisteredDateTime</span><span class="sxs-lookup"><span data-stu-id="bb921-130">domainRegisteredDateTime</span></span>|<span data-ttu-id="bb921-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb921-131">DateTimeOffset</span></span>|<span data-ttu-id="bb921-132">Fecha cuando se registró el dominio de destino.</span><span class="sxs-lookup"><span data-stu-id="bb921-132">Date when the destination domain was registered.</span></span> <span data-ttu-id="bb921-133">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="bb921-133">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="bb921-134">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="bb921-134">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="bb921-135">localDnsName</span><span class="sxs-lookup"><span data-stu-id="bb921-135">localDnsName</span></span>|<span data-ttu-id="bb921-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-136">String</span></span>|<span data-ttu-id="bb921-137">El equipo local resolución de nombres DNS tal como aparece en la memoria caché DNS local del host (por ejemplo, en caso de que se ha alterado el archivo 'hosts').</span><span class="sxs-lookup"><span data-stu-id="bb921-137">The local DNS name resolution as it appears in the host's local DNS cache (for example, in case the 'hosts' file was tampered with).</span></span>|
|<span data-ttu-id="bb921-138">natDestinationAddress</span><span class="sxs-lookup"><span data-stu-id="bb921-138">natDestinationAddress</span></span>|<span data-ttu-id="bb921-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-139">String</span></span>|<span data-ttu-id="bb921-140">Dirección IP de destino de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="bb921-140">Network Address Translation destination IP address.</span></span>|
|<span data-ttu-id="bb921-141">natDestinationPort</span><span class="sxs-lookup"><span data-stu-id="bb921-141">natDestinationPort</span></span>|<span data-ttu-id="bb921-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-142">String</span></span>|<span data-ttu-id="bb921-143">Puerto de destino de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="bb921-143">Network Address Translation destination port.</span></span>|
|<span data-ttu-id="bb921-144">natSourceAddress</span><span class="sxs-lookup"><span data-stu-id="bb921-144">natSourceAddress</span></span>|<span data-ttu-id="bb921-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-145">String</span></span>|<span data-ttu-id="bb921-146">Dirección IP de origen de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="bb921-146">Network Address Translation source IP address.</span></span>|
|<span data-ttu-id="bb921-147">natSourcePort</span><span class="sxs-lookup"><span data-stu-id="bb921-147">natSourcePort</span></span>|<span data-ttu-id="bb921-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-148">String</span></span>|<span data-ttu-id="bb921-149">Puerto de origen de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="bb921-149">Network Address Translation source port.</span></span>|
|<span data-ttu-id="bb921-150">protocol</span><span class="sxs-lookup"><span data-stu-id="bb921-150">protocol</span></span>|[<span data-ttu-id="bb921-151">securityNetworkProtocol</span><span class="sxs-lookup"><span data-stu-id="bb921-151">securityNetworkProtocol</span></span>](securitynetworkprotocol.md)|<span data-ttu-id="bb921-152">Protocolo de red.</span><span class="sxs-lookup"><span data-stu-id="bb921-152">Network protocol.</span></span> <span data-ttu-id="bb921-153">Los valores posibles son: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd` , `raw`, `ipx`, `spx`, `spxII`.</span><span class="sxs-lookup"><span data-stu-id="bb921-153">Possible values are: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd`, `raw`, `ipx`, `spx`, `spxII`.</span></span>|
|<span data-ttu-id="bb921-154">riskScore</span><span class="sxs-lookup"><span data-stu-id="bb921-154">riskScore</span></span>|<span data-ttu-id="bb921-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-155">String</span></span>|<span data-ttu-id="bb921-156">Proveedor generado/calcula el riesgo de puntuación de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="bb921-156">Provider generated/calculated risk score of the network connection.</span></span> <span data-ttu-id="bb921-157">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="bb921-157">Recommended value range of 0-1, which equates to a percentage.</span></span>|
|<span data-ttu-id="bb921-158">dirección de origen</span><span class="sxs-lookup"><span data-stu-id="bb921-158">sourceAddress</span></span>|<span data-ttu-id="bb921-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-159">String</span></span>|<span data-ttu-id="bb921-160">Dirección IP de origen (es decir, el origen) (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="bb921-160">Source (i.e. origin) IP address (of the network connection).</span></span>|
|<span data-ttu-id="bb921-161">puertoDeOrigen</span><span class="sxs-lookup"><span data-stu-id="bb921-161">sourcePort</span></span>|<span data-ttu-id="bb921-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-162">String</span></span>|<span data-ttu-id="bb921-163">Puerto de IP de origen (es decir, el origen) (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="bb921-163">Source (i.e. origin) IP port (of the network connection).</span></span>|
|<span data-ttu-id="bb921-164">status</span><span class="sxs-lookup"><span data-stu-id="bb921-164">status</span></span>|<span data-ttu-id="bb921-165">connectionStatus</span><span class="sxs-lookup"><span data-stu-id="bb921-165">connectionStatus</span></span>|<span data-ttu-id="bb921-166">Estado de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="bb921-166">Network connection status.</span></span> <span data-ttu-id="bb921-167">Los valores posibles son: `unknown`, `attempted`, `succeeded`, `blocked` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="bb921-167">Possible values are: `unknown`, `attempted`, `succeeded`, `blocked`, `failed`.</span></span>|
|<span data-ttu-id="bb921-168">urlParameters</span><span class="sxs-lookup"><span data-stu-id="bb921-168">urlParameters</span></span>|<span data-ttu-id="bb921-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb921-169">String</span></span>|<span data-ttu-id="bb921-170">Parámetros (sufijo) de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="bb921-170">Parameters (suffix) of the destination URL.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="bb921-171">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bb921-171">JSON representation</span></span>

<span data-ttu-id="bb921-172">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bb921-172">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.networkConnection"
}-->

```json
{
  "applicationName": "String",
  "destinationAddress": "String",
  "destinationDomain": "String",
  "destinationPort": "String",
  "destinationUrl": "String",
  "direction": "@odata.type: microsoft.graph.connectionDirection",
  "domainRegisteredDateTime": "String (timestamp)",
  "localDnsName": "String",
  "natDestinationAddress": "String",
  "natDestinationPort": "String",
  "natSourceAddress": "String",
  "natSourcePort": "String",
  "protocol": "@odata.type: microsoft.graph.securityNetworkProtocol",
  "riskScore": "String",
  "sourceAddress": "String",
  "sourcePort": "String",
  "status": "@odata.type: microsoft.graph.connectionStatus",
  "urlParameters": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "networkConnection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
