---
title: tipo de recurso de inicio de sesión
description: 'Este recurso detalla usuario o aplicación de inicio de sesión de actividad en el directorio. '
localization_priority: Priority
ms.openlocfilehash: a2ccb84daee642d207919217aa2857745846c769
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889071"
---
# <a name="signin-resource-type"></a>tipo de recurso de inicio de sesión
Este recurso detalla usuario o aplicación de inicio de sesión de actividad en el directorio. 

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Inicio de sesión de lista](../api/signin-list.md) | [inicio de sesión](signin.md) |Leer las propiedades y las relaciones de objetos de inicio de sesión.|
|[Obtener el inicio de sesión](../api/signin-get.md) | [inicio de sesión](signin.md) |Leer las propiedades y relaciones de objeto de inicio de sesión.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|appDisplayName|Cadena|Hace referencia al nombre de la aplicación que se muestra en el Portal de Azure.|
|appId|cadena|Hace referencia a los GUID único que representa el identificador de aplicación en Azure Active Directory.|
|clientAppUsed|Cadena|Proporciona al cliente heredado usado para inicio de sesión de activty.E.g. incluye el explorador, Active Sync de Exchange, los clientes modernos, IMAP, MAPI, SMTP, POP.|
|appliedConditionalAccessPolicy|colección de [conditionalAccessPolicy](conditionalaccesspolicy.md)|Proporciona una lista de las directivas de acceso condicional que se desencadenan por la actividad de inicio de sesión correspondiente.|
|conditionalAccessStatus|string| Proporciona el estado de la directiva de acceso condicional desencadenada. Los valores posibles son: `success`, `failure`, `notApplied` y `unknownFutureValue`.|
|originalRequestId|Cadena|El identificador de la solicitud de la primera solicitud en la secuencia de autenticación.|
|isInteractive|Booleano|Indica si un inicio de sesión es interactivo o no.|
|tokenIssuerName|Cadena|Nombre de la identidad del proveedor (por ejemplo, sts.microsoft.com)|
|tokenIssuerType|Cadena|Proporciona el tipo de identityProvider. Los valores posibles son `AzureAD`, `ADFederationServices`, `UnknownFutureValue`.|
|correlationId|Cadena|Hace referencia al identificador que se envía desde el cliente cuando se inicia en el inicio de sesión. Esto se usa para solucionar problemas de la actividad de inicio de sesión correspondiente al llamar al departamento de soporte técnico o soporte técnico.|
|createdDateTime|DateTimeOffset|Proporciona la fecha y hora que en el inicio de sesión se ha iniciado. El tipo de marca de tiempo es siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|deviceDetail|[deviceDetail](devicedetail.md)|Proporciona la información del dispositivo desde donde se produjo el inicio de sesión. Se inclules información como deviceId, sistema operativo, explorador. |
|id|Cadena|Indica el identificador único que representa la actividad de inicio de sesión.|
|ipAddress|cadena|Proporciona la dirección IP del cliente desde donde se produjo el inicio de sesión.|
|location|[signInLocation](signinlocation.md)|Proporciona la ciudad, estado y código de país de carta 2 desde donde se produjo el inicio de sesión.|
|processingTimeInMilliseconds|Int|Proporciona la solicitud de tiempo en milisegundos de STS de AD de procesamiento|
|riskDetail|`riskDetail`|Proporciona la razón de' ' detrás de un estado específico de un usuario arriesgado, inicio de sesión o un evento de riesgo. Los valores posibles son: `none`, `adminGeneratedTemporaryPassword`, `userPerformedSecuredPasswordChange`, `userPerformedSecuredPasswordReset`, `adminConfirmedSigninSafe`, `aiConfirmedSigninSafe`, `userPassedMFADrivenByRiskBasedPolicy`, `adminDismissedAllRiskForUser`, `adminConfirmedSigninCompromised`, `unknownFutureValue`. El valor `none` significa que ninguna acción se ha realizado hasta el momento en que el usuario o el inicio de sesión. **Nota:** Detalles de esta propiedad sólo están disponibles para los clientes de P2 de Azure AD Premium. Se devolverán todos los demás clientes `hidden`.|
|riskLevelAggregated|`riskLevel`|Proporciona el nivel de riesgo agregada. Los valores posibles son: `none`, `low`, `medium`, `high`, `hidden`, y `unknownFutureValue`. El valor `hidden` significa que el usuario o el inicio de sesión no se ha habilitado para protección de la identidad de AD de Azure. **Nota:** Detalles de esta propiedad sólo están disponibles para los clientes de P2 de Azure AD Premium. Se devolverán todos los demás clientes `hidden`.|
|riskLevelDuringSignIn|`riskLevel`|Proporciona el nivel de riesgo durante el inicio de sesión. Los valores posibles son: `none`, `low`, `medium`, `high`, `hidden`, y `unknownFutureValue`. El valor `hidden` significa que el usuario o el inicio de sesión no se ha habilitado para protección de la identidad de AD de Azure. **Nota:** Detalles de esta propiedad sólo están disponibles para los clientes de P2 de Azure AD Premium. Se devolverán todos los demás clientes `hidden`.|
|riskEventTypes|`riskEventTypes`|Proporciona la lista de tipos de eventos de riesgo asociado con el inicio de sesión. Los valores posibles son: `unlikelyTravel`, `anonymizedIPAddress`, `maliciousIPAddress`, `unfamiliarFeatures`, `malwareInfectedIPAddress`, `suspiciousIPAddress`, `leakedCredentials`, `investigationsThreatIntelligence`, `generic`, y `unknownFutureValue`.|
|riskState|`riskState`|Proporciona el estado riesgo de un usuario arriesgado, inicio de sesión o un evento de riesgo. Los valores posibles son: `none`, `confirmedSafe`, `remediated`, `dismissed`, `atRisk`, `confirmedCompromised`, `unknownFutureValue`.|
|mfaDetail|[mfaDetail](mfadetail.md)|Proporciona la MFA relacionadas con la información como es necesario MFA, estado de MFA para el inicio de sesión de correspondiente.|
|networkLocationDetail|[networkLocationDetail](networklocationdetail.md)|Proporciona información detallada acerca de la ubicación de red.|
|riskLevel|string| Proporciona el nivel de riesgo asociado con el inicio de sesión. Los valores posibles son: `low`, `medium`, `high`.|
|status|[signInStatus](signinstatus.md)|Proporciona el estado de inicio de sesión. Los valores posibles son `Success` y `Failure`.|
|userDisplayName|Cadena|Indica el nombre del usuario de la presentación.|
|userId|Cadena|Indica el identificador de usuario del usuario.|
|userPrincipalName|Cadena|Indica el UPN del usuario.|
|resourceDisplayName|Cadena|Indica el nombre del recurso que el usuario inició sesión en|
|resourceId|cadena|Indica el identificador del recurso que el usuario inició sesión en.|
|authenticationMethodsUsed|Cadena|Indica la lista de métodos de autenticación que se usan|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signIn"
}-->

```json
{
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "userDisplayName": "String",
  "userPrincipalName": "String",
  "userId": "String",
  "appDisplayName": "String",
  "appId": "String",
  "ipAddress": "String",
  "clientAppUsed": "String",
  "mfaDetail": {"@odata.type": "microsoft.graph.mfaDetail"},
  "correlationId": "String",
  "conditionalAccessStatus": "string",
  "appliedConditionalAccessPolicy": [{"@odata.type": "microsoft.graph.appliedConditionalAccessPolicy"}],
  "originalRequestId": "String",
  "isInteractive": "String",
  "tokenIssuerName": "String",
  "tokenIssuerType": "String",
  "deviceDetail": {"@odata.type": "microsoft.graph.deviceDetail"},
  "location": {"@odata.type": "microsoft.graph.signInLocation"},
  "riskDetail": "string",
  "riskLevelAggregated": "string",
  "riskLevelDuringSignIn": "string",
  "riskState": "string",
  "riskEventTypes": "string",
  "resourceDisplayName": "string",
  "resourceId": "string",
  "authenticationMethodsUsed": "string",
  "status": {"@odata.type": "microsoft.graph.signInStatus"},
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signIn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
