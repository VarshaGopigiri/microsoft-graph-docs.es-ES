---
title: tipo de recurso hostSecurityState
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: ae64d4e0f13e39cb344fd54f5e600cfbfe0dc4f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086565"
---
# <a name="hostsecuritystate-resource-type"></a>tipo de recurso hostSecurityState

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene información de estado acerca del host (incluidos los dispositivos, equipos y así sucesivamente).

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|FQDN|String|Host FQDN (nombre de dominio completo) (por ejemplo, machine.company.com).|
|isAzureAadJoined|Booleano|Es True si el host es el dominio unido a Azure los servicios de dominio de Active Directory.|
|isAzureAadRegistered|Booleano|Es True si el host registrado con Azure Active Directory dispositivo de registro (BYOD dispositivos - es decir, no totalmente administrados por empresa).|
|isHybridAzureDomainJoined|Booleano|Es True si el host está unido a un dominio de Active Directory local de dominio.|
|nombreNetBIOS|String|El nombre de host local, sin el nombre de dominio DNS.|
|sistema operativo|String|Sistema operativo del host. (Por ejemplo, Windows10, Mac OS, RHEL, etcetera.).|
|privateIpAddress|String|Dirección de IPv4 o IPv6 (no enrutable) privada (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.|
|publicIpAddress|String|Dirección IPv4 o IPv6 enrutable públicamente (consulte [RFC 1918](https://tools.ietf.org/html/rfc1918)) en el momento de la alerta.|
|riskScore|String|Puntuación de riesgo proveedor-generado/calculado del host.  Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.hostSecurityState"
}-->

```json
{
  "fqdn": "String",
  "isAzureAadJoined": true,
  "isAzureAadRegistered": true,
  "isHybridAzureDomainJoined": true,
  "netBiosName": "String",
  "os": "String",
  "privateIpAddress": "String",
  "publicIpAddress": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "hostSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
