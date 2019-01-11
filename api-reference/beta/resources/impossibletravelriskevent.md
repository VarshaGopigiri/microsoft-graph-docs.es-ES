---
title: tipo de recurso impossibleTravelRiskEvent
description: Un evento de riesgo detectado por Azure Active Directory protección de identidad donde se producen inicios de sesión de cuenta dos desde ubicaciones atípicos para el usuario y sería imposible de viajes entre las ubicaciones de la duración entre la información de inicio de sesión complementos. completa acerca de eventos de riesgo pueden encontrarse en la documentación de protección de la identidad de AD de Azure.
localization_priority: Normal
ms.openlocfilehash: e9ce064a5ea724b498f3290f630a4169b1aef897
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846455"
---
# <a name="impossibletravelriskevent-resource-type"></a>tipo de recurso impossibleTravelRiskEvent

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) donde se producen inicios de sesión de cuenta dos desde ubicaciones atípicos para el usuario y sería imposible de viajes entre las ubicaciones de la duración entre el completo de inicio de sesión complementos. puede encontrar información acerca de los eventos de riesgo en la [documentación de protección de la identidad de Azure AD](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener impossibleTravelRiskEvent](../api/impossibletravelriskevent-get.md) | [impossibleTravelRiskEvent](impossibletravelriskevent.md) |Leer las propiedades y las relaciones del objeto impossibleTravelRiskEvent.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|closedDateTime|dateTimeOffset| La fecha y hora en que se ha cerrado el evento de riesgo|
|createdDateTime|dateTimeOffset| La fecha y hora en que se creó el evento de riesgo. Siempre es mayor o igual que la fecha y hora del evento riesgo propio. Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.|
|deviceInformation|string| Información sobre el dispositivo|
|id|string| Solo lectura|
|ipAddress|string| La dirección IP del segundo inicio de sesión de|
|isAtypicalLocation|boolean| Si una de las ubicaciones es atípica para el usuario|
|location|string| La ubicación que se adjunta a la dirección IP del segundo inicio de sesión de|
|previousIPAddress|string| La dirección IP del primer inicio de sesión de|
|previousLocation|string| La ubicación que se adjunta a la dirección IP del primer inicio de sesión de|
|previousSigninDateTime|dateTimeOffset| La fecha y hora de inicio de sesión de la primera vez|
|riskEventDateTime|dateTimeOffset| La fecha y hora de inicio de sesión de la segunda vez|
|riskEventStatus|string| Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.|
|riskLevel|string| Los valores posibles son: `low`, `medium` y `high`.|
|riskEventType|string| El tipo de riesgo|
|userAgent|string| Cadena del agente de usuario del explorador|
|userDisplayName|string| El nombre del usuario en riesgo|
|userId|string| El identificador del usuario en riesgo|
|userPrincipalName|string| El nombre principal de usuario del usuario en riesgo|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Description|
|:---------------|:--------|:----------|
|impactedUser|[user](user.md)| Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.impossibleTravelRiskEvent"
}-->

```json
{
  "closedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "deviceInformation": "string",
  "id": "string (identifier)",
  "ipAddress": "string",
  "isAtypicalLocation": true,
  "location": "string",
  "previousIPAddress": "string",
  "previousLocation": "string",
  "previousSigninDateTime": "String (timestamp)",
  "riskEventDateTime": "String (timestamp)",
  "riskEventStatus": "string",
  "riskLevel": "string",
  "riskType": "string",
  "userAgent": "string",
  "userDisplayName": "string",
  "userId": "string",
  "userPrincipalName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "impossibleTravelRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
