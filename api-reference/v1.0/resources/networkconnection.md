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
# <a name="networkconnection-resource-type"></a>tipo de recurso networkConnection

Contiene información de estado acerca de la conexión de red relacionados con la alerta.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Description|
|:---------------|:--------|:----------|
|applicationName|String|Nombre de la aplicación de administración de la conexión de red (por ejemplo, Facebook, SMTP, etcetera).|
|destinationAddress|Cadena|Dirección IP de destino (de la conexión de red).|
|destinationDomain|Cadena|Parte del dominio de destino de la dirección URL de destino. (por ejemplo 'www.contoso.com').|
|destinationPort|Cadena|Puerto de destino (de la conexión de red).|
|destinationUrl|Cadena|Cadena de dirección URL o URI de conexión - excluyendo los parámetros de la red. (por ejemplo, 'www.contoso.com/products/default.html')|
|dirección|connectionDirection|Dirección de la conexión de red. Los valores posibles son: `unknown`, `inbound` y `outbound`.|
|domainRegisteredDateTime|DateTimeOffset|Fecha cuando se registró el dominio de destino. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|localDnsName|Cadena|El equipo local resolución de nombres DNS tal como aparece en la memoria caché DNS local del host (por ejemplo, en caso de que se ha alterado el archivo 'hosts').|
|natDestinationAddress|Cadena|Dirección IP de destino de la traducción de direcciones de red.|
|natDestinationPort|Cadena|Puerto de destino de la traducción de direcciones de red.|
|natSourceAddress|Cadena|Dirección IP de origen de la traducción de direcciones de red.|
|natSourcePort|Cadena|Puerto de origen de la traducción de direcciones de red.|
|protocol|[securityNetworkProtocol](securitynetworkprotocol.md)|Protocolo de red. Los valores posibles son: `unknown`, `ip`, `icmp`, `igmp`, `ggp`, `ipv4`, `tcp`, `pup`, `udp`, `idp`, `ipv6`, `ipv6RoutingHeader`, `ipv6FragmentHeader`, `ipSecEncapsulatingSecurityPayload`, `ipSecAuthenticationHeader`, `icmpV6`, `ipv6NoNextHeader`, `ipv6DestinationOptions`, `nd` , `raw`, `ipx`, `spx`, `spxII`.|
|riskScore|Cadena|Proveedor generado/calcula el riesgo de puntuación de la conexión de red. Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.|
|dirección de origen|Cadena|Dirección IP de origen (es decir, el origen) (de la conexión de red).|
|puertoDeOrigen|Cadena|Puerto de IP de origen (es decir, el origen) (de la conexión de red).|
|status|connectionStatus|Estado de conexión de red. Los valores posibles son: `unknown`, `attempted`, `succeeded`, `blocked` y `failed`.|
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
