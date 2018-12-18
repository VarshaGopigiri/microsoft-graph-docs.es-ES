---
title: tipo de recurso identityRiskEvent
description: 'Un evento de riesgo detectado por la protección de identidad de Azure Active Directory. Es el tipo base para cada tipo de evento de riesgo específico:'
author: cloudhandler
ms.openlocfilehash: 4abe473b47d3ce52fd5b75b6adfd08dbc4af54fc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351745"
---
# <a name="identityriskevent-resource-type"></a>tipo de recurso identityRiskEvent

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/). Es el tipo base para cada tipo de evento de riesgo específico:

| Tipo de evento         | Descripción|
|:---------------|:-----------|
|[anonymousipRiskEvent](anonymousipriskevent.md) | Inicios de sesión desde las direcciones IP anónimas. |
|[malwareRiskEvent](malwareriskevent.md) | Inicios de sesión desde dispositivos infectados con malware. |
|[impossibleTravelRiskEvent](impossibletravelriskevent.md) | Imposible desplazarse a ubicaciones atípicos. |
|[leakedCredentialsRiskEvent](leakedcredentialsriskevent.md) | Usuarios con credenciales perdidas. |
|[suspiciousIpRiskEvent](suspiciousipriskevent.md) | Inicios de sesión desde sospechosas direcciones IP. |
|[unfamiliarLocationRiskEvent](unfamiliarlocationriskevent.md) | Inicios de sesión desde ubicaciones no están familiarizadas. |

Obtener información completa acerca de los eventos de riesgo puede encontrarse en la [documentación de protección de la identidad de AD de Azure](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-risk-events).

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener identityRiskEvent](../api/identityriskevent-get.md) | [identityRiskEvent](identityriskevent.md) |Leer las propiedades y las relaciones del objeto identityRiskEvent.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|closedDateTime|dateTimeOffset| La fecha y hora en que se ha cerrado el evento de riesgo|
|createdDateTime|dateTimeOffset| La fecha y hora en que se creó el evento de riesgo. Siempre es mayor o igual que la fecha y hora del evento riesgo propio. Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.|
|id|string| Solo lectura|
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
  "@odata.type": "microsoft.graph.identityRiskEvent"
}-->

```json
{
  "closedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
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
  "description": "identityRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->