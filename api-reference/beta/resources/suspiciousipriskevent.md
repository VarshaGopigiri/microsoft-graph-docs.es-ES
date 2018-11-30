---
title: tipo de recurso suspiciousIpRiskEvent
description: Un evento de riesgo detectado por Azure Active Directory identidad protección donde un inicio de sesión de cuenta se intentó desde una dirección IP sospechosa. Obtener información completa acerca de los eventos de riesgo puede encontrarse en la documentación de protección de la identidad de AD de Azure.
ms.openlocfilehash: 5d5b2da25c926a88eb7b589d562e6fa9ec914338
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089141"
---
# <a name="suspiciousipriskevent-resource-type"></a>tipo de recurso suspiciousIpRiskEvent

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) donde un inicio de sesión de cuenta se intentó desde una dirección IP sospechosa. Obtener información completa acerca de los eventos de riesgo puede encontrarse en la [documentación de protección de la identidad de AD de Azure](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener suspiciousIpRiskEvent](../api/suspiciousipriskevent-get.md) | [suspiciousIpRiskEvent](suspiciousipriskevent.md) |Leer las propiedades y las relaciones del objeto suspiciousIpRiskEvent.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|closedDateTime|dateTimeOffset| La fecha y hora en que se ha cerrado el evento de riesgo|
|createdDateTime|dateTimeOffset| La fecha y hora en que se creó el evento de riesgo. Siempre es mayor o igual que la fecha y hora del evento riesgo propio. Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.|
|id|string| Solo lectura|
|ipAddress|string| La dirección IP de inicio de sesión de|
|location|string| La ubicación que se adjunta a la dirección IP de inicio de sesión de|
|riskEventDateTime|dateTimeOffset| Fecha y hora en que se produjo el evento de riesgo|
|riskEventStatus|string| Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.|
|riskLevel|string| Los valores posibles son: `low`, `medium` y `high`.|
|riskEventType|string| El tipo de riesgo|
|userDisplayName|string| El nombre del usuario en riesgo|
|userId|string| El identificador del usuario en riesgo|
|userPrincipalName|string| El nombre principal de usuario del usuario en riesgo|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|impactedUser|[user](user.md)| Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.suspiciousIpRiskEvent"
}-->

```json
{
  "closedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "ipAddress": "string",
  "location": "string",
  "riskEventDateTime": "String (timestamp)",
  "riskEventStatus": "string",
  "riskLevel": "string",
  "riskType": "string",
  "userDisplayName": "string",
  "userId": "string",
  "userPrincipalName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "suspiciousIpRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->