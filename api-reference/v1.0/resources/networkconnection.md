# <a name="networkconnection-resource-type"></a><span data-ttu-id="008bc-101">Tipo de recurso networkConnection</span><span class="sxs-lookup"><span data-stu-id="008bc-101">networkConnection resource type</span></span>

<span data-ttu-id="008bc-102">Contiene información de estado acerca de la conexión de red relacionada con la alerta.</span><span class="sxs-lookup"><span data-stu-id="008bc-102">Contains stateful information about the network connection related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="008bc-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="008bc-103">Properties</span></span>

| <span data-ttu-id="008bc-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="008bc-104">Property</span></span>   | <span data-ttu-id="008bc-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="008bc-105">Type</span></span>|<span data-ttu-id="008bc-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="008bc-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="008bc-107">applicationName</span><span class="sxs-lookup"><span data-stu-id="008bc-107">applicationName</span></span>|<span data-ttu-id="008bc-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-108">String</span></span>|<span data-ttu-id="008bc-109">Nombre de la aplicación que administra la conexión de red (por ejemplo, Facebook, SMTP, etcetera).</span><span class="sxs-lookup"><span data-stu-id="008bc-109">Name of the application managing the network connection (for example, Facebook, SMTP, etc.).</span></span>|
|<span data-ttu-id="008bc-110">destinationAddress</span><span class="sxs-lookup"><span data-stu-id="008bc-110">destinationAddress</span></span>|<span data-ttu-id="008bc-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-111">String</span></span>|<span data-ttu-id="008bc-112">Dirección IP de destino (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="008bc-112">Destination IP address (of the network connection).</span></span>|
|<span data-ttu-id="008bc-113">destinationDomain</span><span class="sxs-lookup"><span data-stu-id="008bc-113">destinationDomain</span></span>|<span data-ttu-id="008bc-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-114">String</span></span>|<span data-ttu-id="008bc-115">Parte del dominio de destino de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="008bc-115">Destination domain portion of the destination URL.</span></span> <span data-ttu-id="008bc-116">(por ejemplo 'www.contoso.com').</span><span class="sxs-lookup"><span data-stu-id="008bc-116">(for example 'www.contoso.com').</span></span>|
|<span data-ttu-id="008bc-117">destinationPort</span><span class="sxs-lookup"><span data-stu-id="008bc-117">destinationPort</span></span>|<span data-ttu-id="008bc-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-118">String</span></span>|<span data-ttu-id="008bc-119">Puerto de destino (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="008bc-119">Destination port (of the network connection).</span></span>|
|<span data-ttu-id="008bc-120">destinationUrl</span><span class="sxs-lookup"><span data-stu-id="008bc-120">destinationUrl</span></span>|<span data-ttu-id="008bc-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-121">String</span></span>|<span data-ttu-id="008bc-122">Cadena de dirección URL o URI de conexión - excluyendo los parámetros.</span><span class="sxs-lookup"><span data-stu-id="008bc-122">Network connection URL/URI string - excluding parameters.</span></span> <span data-ttu-id="008bc-123">(por ejemplo, 'www.contoso.com/products/default.html')</span><span class="sxs-lookup"><span data-stu-id="008bc-123">(for example 'www.contoso.com/products/default.html')</span></span>|
|<span data-ttu-id="008bc-124">direction</span><span class="sxs-lookup"><span data-stu-id="008bc-124">direction</span></span>|<span data-ttu-id="008bc-125">connectionDirection</span><span class="sxs-lookup"><span data-stu-id="008bc-125">connectionDirection</span></span>|<span data-ttu-id="008bc-126">Dirección de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="008bc-126">Network connection direction.</span></span> <span data-ttu-id="008bc-127">Los valores posibles son: `unknown`, `inbound` y `outbound`.</span><span class="sxs-lookup"><span data-stu-id="008bc-127">Possible values are: `unknown`, `inbound`, `outbound`.</span></span>|
|<span data-ttu-id="008bc-128">domainRegisteredDateTime</span><span class="sxs-lookup"><span data-stu-id="008bc-128">domainRegisteredDateTime</span></span>|<span data-ttu-id="008bc-129">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="008bc-129">DateTimeOffset</span></span>|<span data-ttu-id="008bc-130">Fecha de registro del dominio de destino.</span><span class="sxs-lookup"><span data-stu-id="008bc-130">Date when the destination domain was registered.</span></span> <span data-ttu-id="008bc-131">El tipo de marca de hora representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="008bc-131">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="008bc-132">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="008bc-132">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="008bc-133">localDnsName</span><span class="sxs-lookup"><span data-stu-id="008bc-133">localDnsName</span></span>|<span data-ttu-id="008bc-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-134">String</span></span>|<span data-ttu-id="008bc-135">L resolución de nombres DNS local tal como aparece en la memoria caché DNS local del host (por ejemplo, en caso de que se haya alterado el archivo 'hosts').</span><span class="sxs-lookup"><span data-stu-id="008bc-135">The local DNS name resolution as it appears in the host's local DNS cache (for example, in case the 'hosts' file was tampered with).</span></span>|
|<span data-ttu-id="008bc-136">natDestinationAddress</span><span class="sxs-lookup"><span data-stu-id="008bc-136">natDestinationAddress</span></span>|<span data-ttu-id="008bc-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-137">String</span></span>|<span data-ttu-id="008bc-138">Dirección IP de destino de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="008bc-138">Network Address Translation destination IP address.</span></span>|
|<span data-ttu-id="008bc-139">natDestinationPort</span><span class="sxs-lookup"><span data-stu-id="008bc-139">natDestinationPort</span></span>|<span data-ttu-id="008bc-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-140">String</span></span>|<span data-ttu-id="008bc-141">Puerto de destino de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="008bc-141">Network Address Translation destination port.</span></span>|
|<span data-ttu-id="008bc-142">natSourceAddress</span><span class="sxs-lookup"><span data-stu-id="008bc-142">natSourceAddress</span></span>|<span data-ttu-id="008bc-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-143">String</span></span>|<span data-ttu-id="008bc-144">Dirección IP de origen de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="008bc-144">Network Address Translation source IP address.</span></span>|
|<span data-ttu-id="008bc-145">natSourcePort</span><span class="sxs-lookup"><span data-stu-id="008bc-145">natSourcePort</span></span>|<span data-ttu-id="008bc-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-146">String</span></span>|<span data-ttu-id="008bc-147">Puerto de origen de la traducción de direcciones de red.</span><span class="sxs-lookup"><span data-stu-id="008bc-147">Network Address Translation source port.</span></span>|
|<span data-ttu-id="008bc-148">protocol</span><span class="sxs-lookup"><span data-stu-id="008bc-148">protocol</span></span>|[<span data-ttu-id="008bc-149">securityNetworkProtocol</span><span class="sxs-lookup"><span data-stu-id="008bc-149">securityNetworkProtocol</span></span>](securitynetworkprotocol.md)|<span data-ttu-id="008bc-150">Protocolo de red.</span><span class="sxs-lookup"><span data-stu-id="008bc-150">Network protocol analysis</span></span> <span data-ttu-id="008bc-151">Los valores posibles son: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd`, `raw`, `ipx`, `spx` y `spxII`.</span><span class="sxs-lookup"><span data-stu-id="008bc-151">Possible values are: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd`, `raw`, `ipx`.</span></span>|
|<span data-ttu-id="008bc-152">riskScore</span><span class="sxs-lookup"><span data-stu-id="008bc-152">riskScore</span></span>|<span data-ttu-id="008bc-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-153">String</span></span>|<span data-ttu-id="008bc-154">Puntuación de riesgo calculado/generado por el proveedor de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="008bc-154">Provider generated/calculated risk score of the network connection.</span></span> <span data-ttu-id="008bc-155">Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="008bc-155">Recommended value range of 0-1, which equates to a percentage.</span></span>|
|<span data-ttu-id="008bc-156">sourceAddress</span><span class="sxs-lookup"><span data-stu-id="008bc-156">sourceAddress</span></span>|<span data-ttu-id="008bc-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-157">String</span></span>|<span data-ttu-id="008bc-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-158">Source (i.e. origin) IP address (of the network connection).</span></span>|
|<span data-ttu-id="008bc-159">sourcePort</span><span class="sxs-lookup"><span data-stu-id="008bc-159">sourcePort</span></span>|<span data-ttu-id="008bc-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-160">String</span></span>|<span data-ttu-id="008bc-161">Puerto de IP de origen (es decir, el origen) (de la conexión de red).</span><span class="sxs-lookup"><span data-stu-id="008bc-161">Source (i.e. origin) IP port (of the network connection).</span></span>|
|<span data-ttu-id="008bc-162">status</span><span class="sxs-lookup"><span data-stu-id="008bc-162">status</span></span>|<span data-ttu-id="008bc-163">connectionStatus</span><span class="sxs-lookup"><span data-stu-id="008bc-163">ConnectionStatus</span></span>|<span data-ttu-id="008bc-164">Estado de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="008bc-164">Network connection status.</span></span> <span data-ttu-id="008bc-165">Los valores posibles son: `unknown`, `attempted`, `succeeded`, `blocked` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="008bc-165">Possible values are: `unknown`, `attempted`, `succeeded`, `blocked`, `failed`.</span></span>|
|<span data-ttu-id="008bc-166">urlParameters</span><span class="sxs-lookup"><span data-stu-id="008bc-166">urlParameters</span></span>|<span data-ttu-id="008bc-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="008bc-167">String</span></span>|<span data-ttu-id="008bc-168">Parámetros (sufijo) de la dirección URL de destino.</span><span class="sxs-lookup"><span data-stu-id="008bc-168">Parameters (suffix) of the destination URL.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="008bc-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="008bc-169">JSON representation</span></span>

<span data-ttu-id="008bc-170">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="008bc-170">The following is a JSON representation of the resource.</span></span>

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