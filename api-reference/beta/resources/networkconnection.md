---
title: tipo de recurso networkConnection
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 7dfc055c7603adc8d60908df58ce3995927316cd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089317"
---
# <a name="networkconnection-resource-type"></a><span data-ttu-id="e6e80-104">tipo de recurso networkConnection</span><span class="sxs-lookup"><span data-stu-id="e6e80-104">networkConnection resource type</span></span>

 > <span data-ttu-id="e6e80-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6e80-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6e80-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6e80-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e6e80-107">Contiene información de estado acerca de la conexión de red relacionados con la alerta.</span><span class="sxs-lookup"><span data-stu-id="e6e80-107">Contains stateful information about the network connection related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="e6e80-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6e80-108">Properties</span></span>

| <span data-ttu-id="e6e80-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6e80-109">Property</span></span>   | <span data-ttu-id="e6e80-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6e80-110">Type</span></span>|<span data-ttu-id="e6e80-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6e80-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e6e80-112">applicationName</span><span class="sxs-lookup"><span data-stu-id="e6e80-112">applicationName</span></span>|<span data-ttu-id="e6e80-113">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-113">String</span></span>|<span data-ttu-id="e6e80-114">Nombre de la aplicación de administración de la conexión de red (por ejemplo, Facebook, SMTP, etcetera).</span><span class="sxs-lookup"><span data-stu-id="e6e80-114">Name of the application managing the network connection (for example, Facebook, SMTP, etc.).</span></span>|
|<span data-ttu-id="e6e80-115">destinationAddress</span><span class="sxs-lookup"><span data-stu-id="e6e80-115">destinationAddress</span></span>|<span data-ttu-id="e6e80-116">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-116">String</span></span>|<span data-ttu-id="e6e80-117">Dirección IP de destino (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="e6e80-117">Destination IP address (of the network connection).</span></span>|
|<span data-ttu-id="e6e80-118">destinationDomain</span><span class="sxs-lookup"><span data-stu-id="e6e80-118">destinationDomain</span></span>|<span data-ttu-id="e6e80-119">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-119">String</span></span>|<span data-ttu-id="e6e80-120">Parte del dominio de destino de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="e6e80-120">Destination domain portion of the destination URL.</span></span> <span data-ttu-id="e6e80-121">(por ejemplo 'www.contoso.com').</span><span class="sxs-lookup"><span data-stu-id="e6e80-121">(for example 'www.contoso.com').</span></span>|
|<span data-ttu-id="e6e80-122">destinationPort</span><span class="sxs-lookup"><span data-stu-id="e6e80-122">destinationPort</span></span>|<span data-ttu-id="e6e80-123">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-123">String</span></span>|<span data-ttu-id="e6e80-124">Puerto de destino (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="e6e80-124">Destination port (of the network connection).</span></span>|
|<span data-ttu-id="e6e80-125">destinationUrl</span><span class="sxs-lookup"><span data-stu-id="e6e80-125">destinationUrl</span></span>|<span data-ttu-id="e6e80-126">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-126">String</span></span>|<span data-ttu-id="e6e80-127">Cadena de dirección URL o URI de conexión - excluyendo los parámetros de la red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-127">Network connection URL/URI string - excluding parameters.</span></span> <span data-ttu-id="e6e80-128">(por ejemplo, 'www.contoso.com/products/default.html')</span><span class="sxs-lookup"><span data-stu-id="e6e80-128">(for example 'www.contoso.com/products/default.html')</span></span>|
|<span data-ttu-id="e6e80-129">dirección</span><span class="sxs-lookup"><span data-stu-id="e6e80-129">direction</span></span>|<span data-ttu-id="e6e80-130">connectionDirection</span><span class="sxs-lookup"><span data-stu-id="e6e80-130">connectionDirection</span></span>|<span data-ttu-id="e6e80-131">Dirección de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-131">Network connection direction.</span></span> <span data-ttu-id="e6e80-132">Los valores posibles son: `unknown`, `inbound` y `outbound`.</span><span class="sxs-lookup"><span data-stu-id="e6e80-132">Possible values are: `unknown`, `inbound`, `outbound`.</span></span>|
|<span data-ttu-id="e6e80-133">domainRegisteredDateTime</span><span class="sxs-lookup"><span data-stu-id="e6e80-133">domainRegisteredDateTime</span></span>|<span data-ttu-id="e6e80-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6e80-134">DateTimeOffset</span></span>|<span data-ttu-id="e6e80-135">Fecha cuando se registró el dominio de destino.</span><span class="sxs-lookup"><span data-stu-id="e6e80-135">Date when the destination domain was registered.</span></span> <span data-ttu-id="e6e80-136">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="e6e80-136">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="e6e80-137">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="e6e80-137">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="e6e80-138">localDnsName</span><span class="sxs-lookup"><span data-stu-id="e6e80-138">localDnsName</span></span>|<span data-ttu-id="e6e80-139">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-139">String</span></span>|<span data-ttu-id="e6e80-140">El equipo local resolución de nombres DNS tal como aparece en la memoria caché DNS local del host (por ejemplo, en caso de que se ha alterado el archivo 'hosts').</span><span class="sxs-lookup"><span data-stu-id="e6e80-140">The local DNS name resolution as it appears in the host's local DNS cache (for example, in case the 'hosts' file was tampered with).</span></span>|
|<span data-ttu-id="e6e80-141">natDestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e6e80-141">natDestinationAddress</span></span>|<span data-ttu-id="e6e80-142">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-142">String</span></span>|<span data-ttu-id="e6e80-143">Dirección IP de destino de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-143">Network Address Translation destination IP address.</span></span>|
|<span data-ttu-id="e6e80-144">natDestinationPort</span><span class="sxs-lookup"><span data-stu-id="e6e80-144">natDestinationPort</span></span>|<span data-ttu-id="e6e80-145">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-145">String</span></span>|<span data-ttu-id="e6e80-146">Puerto de destino de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-146">Network Address Translation destination port.</span></span>|
|<span data-ttu-id="e6e80-147">natSourceAddress</span><span class="sxs-lookup"><span data-stu-id="e6e80-147">natSourceAddress</span></span>|<span data-ttu-id="e6e80-148">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-148">String</span></span>|<span data-ttu-id="e6e80-149">Dirección IP de origen de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-149">Network Address Translation source IP address.</span></span>|
|<span data-ttu-id="e6e80-150">natSourcePort</span><span class="sxs-lookup"><span data-stu-id="e6e80-150">natSourcePort</span></span>|<span data-ttu-id="e6e80-151">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-151">String</span></span>|<span data-ttu-id="e6e80-152">Puerto de origen de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-152">Network Address Translation source port.</span></span>|
|<span data-ttu-id="e6e80-153">protocol</span><span class="sxs-lookup"><span data-stu-id="e6e80-153">protocol</span></span>|[<span data-ttu-id="e6e80-154">securityNetworkProtocol</span><span class="sxs-lookup"><span data-stu-id="e6e80-154">securityNetworkProtocol</span></span>](securitynetworkprotocolenumtype.md)|<span data-ttu-id="e6e80-155">Protocolo de red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-155">Network protocol.</span></span> <span data-ttu-id="e6e80-156">Los valores posibles son: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd` , `raw`, `ipx`, `spx`, `spxII`.</span><span class="sxs-lookup"><span data-stu-id="e6e80-156">Possible values are: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd`, `raw`, `ipx`, `spx`, `spxII`.</span></span>|
|<span data-ttu-id="e6e80-157">riskScore</span><span class="sxs-lookup"><span data-stu-id="e6e80-157">riskScore</span></span>|<span data-ttu-id="e6e80-158">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-158">String</span></span>|<span data-ttu-id="e6e80-159">Proveedor generado/calcula el riesgo de puntuación de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-159">Provider generated/calculated risk score of the network connection.</span></span> <span data-ttu-id="e6e80-160">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="e6e80-160">Recommended value range of 0-1, which equates to a percentage.</span></span>|
|<span data-ttu-id="e6e80-161">dirección de origen</span><span class="sxs-lookup"><span data-stu-id="e6e80-161">sourceAddress</span></span>|<span data-ttu-id="e6e80-162">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-162">String</span></span>|<span data-ttu-id="e6e80-163">Dirección IP de origen (es decir, el origen) (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="e6e80-163">Source (i.e. origin) IP address (of the network connection).</span></span>|
|<span data-ttu-id="e6e80-164">puertoDeOrigen</span><span class="sxs-lookup"><span data-stu-id="e6e80-164">sourcePort</span></span>|<span data-ttu-id="e6e80-165">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-165">String</span></span>|<span data-ttu-id="e6e80-166">Puerto de IP de origen (es decir, el origen) (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="e6e80-166">Source (i.e. origin) IP port (of the network connection).</span></span>|
|<span data-ttu-id="e6e80-167">status</span><span class="sxs-lookup"><span data-stu-id="e6e80-167">status</span></span>|<span data-ttu-id="e6e80-168">connectionStatus</span><span class="sxs-lookup"><span data-stu-id="e6e80-168">connectionStatus</span></span>|<span data-ttu-id="e6e80-169">Estado de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="e6e80-169">Network connection status.</span></span> <span data-ttu-id="e6e80-170">Los valores posibles son: `unknown`, `attempted`, `succeeded`, `blocked` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="e6e80-170">Possible values are: `unknown`, `attempted`, `succeeded`, `blocked`, `failed`.</span></span>|
|<span data-ttu-id="e6e80-171">urlParameters</span><span class="sxs-lookup"><span data-stu-id="e6e80-171">urlParameters</span></span>|<span data-ttu-id="e6e80-172">String</span><span class="sxs-lookup"><span data-stu-id="e6e80-172">String</span></span>|<span data-ttu-id="e6e80-173">Parámetros (sufijo) de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="e6e80-173">Parameters (suffix) of the destination URL.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e6e80-174">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e6e80-174">JSON representation</span></span>

<span data-ttu-id="e6e80-175">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e6e80-175">The following is a JSON representation of the resource.</span></span>

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
