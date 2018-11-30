---
title: tipo de recurso userSecurityState
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: f530ac1a657b4049c17bdcdd40f1dd5ea734f278
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086833"
---
# <a name="usersecuritystate-resource-type"></a>tipo de recurso userSecurityState

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene información de estado acerca de la cuenta de usuario.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|aadUserId|String|AAD usuario identificador (GUID) - objeto representa la entidad de usuario físicos/multi-account.|
|accountName|String|Nombre de cuenta de la cuenta de usuario (sin dominio de Active Directory o dominio DNS) - (también denominada `mailNickName`).|
|domainName|String|Dominio de NetBIOS o Active Directory de la cuenta de usuario (es decir, el formato dominio\cuenta).|
|emailRole|emailRole|Para las alertas relacionadas con el correo electrónico - correo electrónico de una cuenta de usuario 'rol'. Los valores posibles son: `unknown`, `sender` y `recipient`.|
|isVpn|Booleano|Indica si el usuario se conectó a través de una red privada virtual.|
|logonDateTime|DateTimeOffset|Hora a la que el inicio de sesión se produjo. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|ID de registro|String|Identificador de usuario de inicio de sesión.|
|logonIp|String|Dirección IP de. que la solicitud de inicio de sesión se originó.|
|logonLocation|String|Ubicación (mediante la asignación de direcciones IP) asociado a un evento de inicio de sesión de usuario por este usuario.|
|logonType|logonType|Método de inicio de sesión de usuario en. Los valores posibles son: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.|
|onPremisesSecurityIdentifier|String|Active Directory (local) identificador de seguridad (SID) del usuario.|
|riskScore|String|Puntuación de proveedor generado/calculada en el riesgo de la cuenta de usuario. Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.|
|userAccountType|userAccountSecurityType|Tipo de cuenta de usuario (pertenencia a grupos), por definición de Windows. Los valores posibles son: `unknown`, `standard`, `power` y `administrator`.|
|userPrincipalName|String|Inicio de sesión de nombre de usuario - formato de internet: (nombre de cuenta de usuario) @(nombre de dominio DNS de cuenta de usuario).|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.userSecurityState"
}-->

```json
{
  "aadUserId": "String",
  "accountName": "String",
  "domainName": "String",
  "emailRole": "@odata.type: microsoft.graph.emailRole",
  "isVpn": true,
  "logonDateTime": "String (timestamp)",
  "logonId": "String",
  "logonIp": "String",
  "logonLocation": "String",
  "logonType": "@odata.type: microsoft.graph.logonType",
  "onPremisesSecurityIdentifier": "String",
  "riskScore": "String",
  "userAccountType": "@odata.type: microsoft.graph.userAccountSecurityType",
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
