---
title: tipo de recurso de API
description: Especifica la configuración para una aplicación Web API.
ms.openlocfilehash: b5b07ccb5a66027f9eb755754842f6e2e2ae708e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085466"
---
# <a name="api-resource-type"></a>tipo de recurso de API

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica la configuración para una aplicación Web API.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|requestedAccessTokenVersion|Int32| Especifica la versión de token de acceso aceptados para el recurso de API actual. Los valores posibles son 1 ó 2.  |
|oauth2PermissionScopes|colección de [permissionScope](permissionscope.md)| La colección de los ámbitos de permiso de OAuth 2.0 que expone la web de aplicación de la API (recurso) a las aplicaciones cliente. Estos ámbitos de permisos pueden concederse a las aplicaciones cliente durante su consentimiento. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.api"
}-->

```json
{
  "requestedAccessTokenVersion": 1,
  "oauth2PermissionScopes": [{"@odata.type": "microsoft.graph.permissionScope"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "api resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->