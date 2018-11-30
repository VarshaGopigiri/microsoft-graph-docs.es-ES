---
title: tipo de recurso networkConnection
description: Contiene información de estado acerca de la conexión de red relacionados con la alerta.
ms.openlocfilehash: e3352cbda430412691285c209c566fb379045681
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032286"
---
# <a name="networkconnection-resource-type"></a><span data-ttu-id="6d10b-103">tipo de recurso networkConnection</span><span class="sxs-lookup"><span data-stu-id="6d10b-103">networkConnection resource type</span></span>

<span data-ttu-id="6d10b-104">Contiene información de estado acerca de la conexión de red relacionados con la alerta.</span><span class="sxs-lookup"><span data-stu-id="6d10b-104">Contains stateful information about the network connection related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="6d10b-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6d10b-105">Properties</span></span>

| <span data-ttu-id="6d10b-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6d10b-106">Property</span></span>   | <span data-ttu-id="6d10b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d10b-107">Type</span></span>|<span data-ttu-id="6d10b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d10b-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6d10b-109">applicationName</span><span class="sxs-lookup"><span data-stu-id="6d10b-109">applicationName</span></span>|<span data-ttu-id="6d10b-110">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-110">String</span></span>|<span data-ttu-id="6d10b-111">Nombre de la aplicación de administración de la conexión de red (por ejemplo, Facebook, SMTP, etcetera).</span><span class="sxs-lookup"><span data-stu-id="6d10b-111">Name of the application managing the network connection (for example, Facebook, SMTP, etc.).</span></span>|
|<span data-ttu-id="6d10b-112">destinationAddress</span><span class="sxs-lookup"><span data-stu-id="6d10b-112">destinationAddress</span></span>|<span data-ttu-id="6d10b-113">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-113">String</span></span>|<span data-ttu-id="6d10b-114">Dirección IP de destino (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="6d10b-114">Destination IP address (of the network connection).</span></span>|
|<span data-ttu-id="6d10b-115">destinationDomain</span><span class="sxs-lookup"><span data-stu-id="6d10b-115">destinationDomain</span></span>|<span data-ttu-id="6d10b-116">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-116">String</span></span>|<span data-ttu-id="6d10b-117">Parte del dominio de destino de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="6d10b-117">Destination domain portion of the destination URL.</span></span> <span data-ttu-id="6d10b-118">(por ejemplo 'www.contoso.com').</span><span class="sxs-lookup"><span data-stu-id="6d10b-118">(for example 'www.contoso.com').</span></span>|
|<span data-ttu-id="6d10b-119">destinationPort</span><span class="sxs-lookup"><span data-stu-id="6d10b-119">destinationPort</span></span>|<span data-ttu-id="6d10b-120">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-120">String</span></span>|<span data-ttu-id="6d10b-121">Puerto de destino (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="6d10b-121">Destination port (of the network connection).</span></span>|
|<span data-ttu-id="6d10b-122">destinationUrl</span><span class="sxs-lookup"><span data-stu-id="6d10b-122">destinationUrl</span></span>|<span data-ttu-id="6d10b-123">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-123">String</span></span>|<span data-ttu-id="6d10b-124">Cadena de dirección URL o URI de conexión - excluyendo los parámetros de la red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-124">Network connection URL/URI string - excluding parameters.</span></span> <span data-ttu-id="6d10b-125">(por ejemplo, 'www.contoso.com/products/default.html')</span><span class="sxs-lookup"><span data-stu-id="6d10b-125">(for example 'www.contoso.com/products/default.html')</span></span>|
|<span data-ttu-id="6d10b-126">dirección</span><span class="sxs-lookup"><span data-stu-id="6d10b-126">direction</span></span>|<span data-ttu-id="6d10b-127">connectionDirection</span><span class="sxs-lookup"><span data-stu-id="6d10b-127">connectionDirection</span></span>|<span data-ttu-id="6d10b-128">Dirección de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-128">Network connection direction.</span></span> <span data-ttu-id="6d10b-129">Los valores posibles son: `unknown`, `inbound` y `outbound`.</span><span class="sxs-lookup"><span data-stu-id="6d10b-129">Possible values are: `unknown`, `inbound`, `outbound`.</span></span>|
|<span data-ttu-id="6d10b-130">domainRegisteredDateTime</span><span class="sxs-lookup"><span data-stu-id="6d10b-130">domainRegisteredDateTime</span></span>|<span data-ttu-id="6d10b-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6d10b-131">DateTimeOffset</span></span>|<span data-ttu-id="6d10b-132">Fecha cuando se registró el dominio de destino.</span><span class="sxs-lookup"><span data-stu-id="6d10b-132">Date when the destination domain was registered.</span></span> <span data-ttu-id="6d10b-133">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="6d10b-133">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="6d10b-134">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="6d10b-134">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="6d10b-135">localDnsName</span><span class="sxs-lookup"><span data-stu-id="6d10b-135">localDnsName</span></span>|<span data-ttu-id="6d10b-136">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-136">String</span></span>|<span data-ttu-id="6d10b-137">El equipo local resolución de nombres DNS tal como aparece en la memoria caché DNS local del host (por ejemplo, en caso de que se ha alterado el archivo 'hosts').</span><span class="sxs-lookup"><span data-stu-id="6d10b-137">The local DNS name resolution as it appears in the host's local DNS cache (for example, in case the 'hosts' file was tampered with).</span></span>|
|<span data-ttu-id="6d10b-138">natDestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6d10b-138">natDestinationAddress</span></span>|<span data-ttu-id="6d10b-139">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-139">String</span></span>|<span data-ttu-id="6d10b-140">Dirección IP de destino de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-140">Network Address Translation destination IP address.</span></span>|
|<span data-ttu-id="6d10b-141">natDestinationPort</span><span class="sxs-lookup"><span data-stu-id="6d10b-141">natDestinationPort</span></span>|<span data-ttu-id="6d10b-142">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-142">String</span></span>|<span data-ttu-id="6d10b-143">Puerto de destino de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-143">Network Address Translation destination port.</span></span>|
|<span data-ttu-id="6d10b-144">natSourceAddress</span><span class="sxs-lookup"><span data-stu-id="6d10b-144">natSourceAddress</span></span>|<span data-ttu-id="6d10b-145">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-145">String</span></span>|<span data-ttu-id="6d10b-146">Dirección IP de origen de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-146">Network Address Translation source IP address.</span></span>|
|<span data-ttu-id="6d10b-147">natSourcePort</span><span class="sxs-lookup"><span data-stu-id="6d10b-147">natSourcePort</span></span>|<span data-ttu-id="6d10b-148">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-148">String</span></span>|<span data-ttu-id="6d10b-149">Puerto de origen de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-149">Network Address Translation source port.</span></span>|
|<span data-ttu-id="6d10b-150">protocol</span><span class="sxs-lookup"><span data-stu-id="6d10b-150">protocol</span></span>|[<span data-ttu-id="6d10b-151">securityNetworkProtocol</span><span class="sxs-lookup"><span data-stu-id="6d10b-151">securityNetworkProtocol</span></span>](securitynetworkprotocol.md)|<span data-ttu-id="6d10b-152">Protocolo de red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-152">Network protocol.</span></span> <span data-ttu-id="6d10b-153">Los valores posibles son: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd` , `raw`, `ipx`, `spx`, `spxII`.</span><span class="sxs-lookup"><span data-stu-id="6d10b-153">Possible values are: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd`, `raw`, `ipx`, `spx`, `spxII`.</span></span>|
|<span data-ttu-id="6d10b-154">riskScore</span><span class="sxs-lookup"><span data-stu-id="6d10b-154">riskScore</span></span>|<span data-ttu-id="6d10b-155">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-155">String</span></span>|<span data-ttu-id="6d10b-156">Proveedor generado/calcula el riesgo de puntuación de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-156">Provider generated/calculated risk score of the network connection.</span></span> <span data-ttu-id="6d10b-157">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="6d10b-157">Recommended value range of 0-1, which equates to a percentage.</span></span>|
|<span data-ttu-id="6d10b-158">dirección de origen</span><span class="sxs-lookup"><span data-stu-id="6d10b-158">sourceAddress</span></span>|<span data-ttu-id="6d10b-159">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-159">String</span></span>|<span data-ttu-id="6d10b-160">Dirección IP de origen (es decir, el origen) (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="6d10b-160">Source (i.e. origin) IP address (of the network connection).</span></span>|
|<span data-ttu-id="6d10b-161">puertoDeOrigen</span><span class="sxs-lookup"><span data-stu-id="6d10b-161">sourcePort</span></span>|<span data-ttu-id="6d10b-162">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-162">String</span></span>|<span data-ttu-id="6d10b-163">Puerto de IP de origen (es decir, el origen) (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="6d10b-163">Source (i.e. origin) IP port (of the network connection).</span></span>|
|<span data-ttu-id="6d10b-164">status</span><span class="sxs-lookup"><span data-stu-id="6d10b-164">status</span></span>|<span data-ttu-id="6d10b-165">connectionStatus</span><span class="sxs-lookup"><span data-stu-id="6d10b-165">connectionStatus</span></span>|<span data-ttu-id="6d10b-166">Estado de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="6d10b-166">Network connection status.</span></span> <span data-ttu-id="6d10b-167">Los valores posibles son: `unknown`, `attempted`, `succeeded`, `blocked` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="6d10b-167">Possible values are: `unknown`, `attempted`, `succeeded`, `blocked`, `failed`.</span></span>|
|<span data-ttu-id="6d10b-168">urlParameters</span><span class="sxs-lookup"><span data-stu-id="6d10b-168">urlParameters</span></span>|<span data-ttu-id="6d10b-169">String</span><span class="sxs-lookup"><span data-stu-id="6d10b-169">String</span></span>|<span data-ttu-id="6d10b-170">Parámetros (sufijo) de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="6d10b-170">Parameters (suffix) of the destination URL.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6d10b-171">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6d10b-171">JSON representation</span></span>

<span data-ttu-id="6d10b-172">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6d10b-172">The following is a JSON representation of the resource.</span></span>

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