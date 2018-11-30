---
title: tipo de recurso oAuth2PermissionGrant
description: Representa los ámbitos de OAuth 2.0 (delegado permisos) que se hayan concedido a una aplicación (representada por una entidad de seguridad de servicio) como parte del proceso de consentimiento de usuario o un administrador.
ms.openlocfilehash: 8fc5154ddba1b78976dc3e24c6712f9fc8944f43
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084348"
---
# <a name="oauth2permissiongrant-resource-type"></a>tipo de recurso oAuth2PermissionGrant

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa los ámbitos de OAuth 2.0 (delegado permisos) que se hayan concedido a una aplicación (representada por una entidad de seguridad de servicio) como parte del proceso de consentimiento de usuario o un administrador.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.oAuth2Permissiongrant"
}-->

```json
{
  "clientId": "string",
  "consentType": "string",
  "expiryTime": "String (timestamp)",
  "id": "string (identifier)",
  "principalId": "string",
  "resourceId": "string",
  "scope": "string",
  "startTime": "String (timestamp)"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|clientId|String| El identificador de la entidad de seguridad de servicio concedido da su consentimiento para suplantar al usuario al obtener acceso a los recursos (representado por la propiedad resourceId). |
|consentType|String| Indica si su consentimiento le ha proporcionado por el administrador (en nombre de la organización) o de forma individual. Los valores posibles son *AllPrincipals* o *entidad de seguridad*. |
|expiryTime|DateTimeOffset| Actualmente, se ignora el valor de tiempo de expiración. |
|id|String| Identificador único. Solo lectura.|
|principalId|String| Si consentType es *AllPrincipals* este valor es null, y el consentimiento se aplica a todos los usuarios de la organización. Si consentType es *Principal*, esta propiedad especifica el identificador del usuario que concede el consentimiento y se aplica únicamente para ese usuario. |
|resourceId|cadena| Especifica el identificador de la entidad de seguridad de servicio de recurso al que se ha concedido acceso. |
|scope|String| Especifica el valor de la notificación de [ámbito](/graph/permissions-reference) que se debe esperar a que la aplicación de recursos en el token de acceso de OAuth 2.0. Por ejemplo, *User.Read* |
|startTime|DateTimeOffset| Actualmente, se ignora el valor de tiempo de inicio. |

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener oAuth2PermissionGrant](../api/oauth2permissiongrant-get.md) | [oAuth2PermissionGrant](oauth2permissiongrant.md) |Leer las propiedades y las relaciones del objeto oAuth2PermissionGrant.|
|[Lista oAuth2PermissionGrants](../api/oauth2permissiongrant-list.md) | colección de [oAuth2PermissionGrant](oauth2permissiongrant.md) | Recuperar una lista de objetos de oauth2PermissionGrant. |
|[Actualizar oAuth2PermissionGrant](../api/oauth2permissiongrant-update.md) | [oAuth2PermissionGrant](oauth2permissiongrant.md) |Actualizar el objeto oAuth2PermissionGrant. |
|[Eliminar oAuth2PermissionGrant](../api/oauth2permissiongrant-delete.md) | Ninguno |Eliminar el objeto oAuth2PermissionGrant. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "oAuth2PermissionGrant resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->