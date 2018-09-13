# <a name="networkconnection-resource-type"></a>Tipo de recurso networkConnection

Contiene información de estado acerca de la conexión de red relacionada con la alerta.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|applicationName|Cadena|Nombre de la aplicación que administra la conexión de red (por ejemplo, Facebook, SMTP, etcetera).|
|destinationAddress|Cadena|Dirección IP de destino (de la conexión de red).|
|destinationDomain|Cadena|Parte del dominio de destino de la dirección URL de destino. (por ejemplo 'www.contoso.com').|
|destinationPort|Cadena|Puerto de destino (de la conexión de red).|
|destinationUrl|Cadena|Cadena de dirección URL o URI de conexión - excluyendo los parámetros. (por ejemplo, 'www.contoso.com/products/default.html')|
|direction|connectionDirection|Dirección de la conexión de red. Los valores posibles son: `unknown`, `inbound` y `outbound`.|
|domainRegisteredDateTime|DateTimeOffset|Fecha de registro del dominio de destino. El tipo de marca de hora representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|localDnsName|Cadena|L resolución de nombres DNS local tal como aparece en la memoria caché DNS local del host (por ejemplo, en caso de que se haya alterado el archivo 'hosts').|
|natDestinationAddress|Cadena|Dirección IP de destino de la traducción de direcciones de red.|
|natDestinationPort|Cadena|Puerto de destino de la traducción de direcciones de red.|
|natSourceAddress|Cadena|Dirección IP de origen de la traducción de direcciones de red.|
|natSourcePort|Cadena|Puerto de origen de la traducción de direcciones de red.|
|protocol|[securityNetworkProtocol](securitynetworkprotocol.md)|Protocolo de red. Los valores posibles son: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd`, `raw`, `ipx`, `spx` y `spxII`.|
|riskScore|Cadena|Puntuación de riesgo calculado/generado por el proveedor de la conexión de red. Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.|
|sourceAddress|Cadena|Cadena|
|sourcePort|Cadena|Puerto de IP de origen (es decir, el origen) (de la conexión de red).|
|status|connectionStatus|Estado de la conexión de red. Los valores posibles son: `unknown`, `attempted`, `succeeded`, `blocked` y `failed`.|
|urlParameters|Cadena|Parámetros (sufijo) de la dirección URL de destino.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

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