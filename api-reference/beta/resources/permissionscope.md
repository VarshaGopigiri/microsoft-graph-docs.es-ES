---
title: tipo de recurso permissionScope
description: Representa una OAuth 2.0 habían delegada ámbito de permisos. La versión 2.0 de OAuth especificado ámbitos de permisos delegado pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** en el objeto Application) cuando se llama a una aplicación de recursos. La propiedad **oauth2Permissions** de la entidad ServicePrincipal y de la entidad de la aplicación es una colección de **OAuth2Permission**.
ms.openlocfilehash: b15ee9901632fca113d944000847c953e85be58c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088643"
---
# <a name="permissionscope-resource-type"></a>tipo de recurso permissionScope

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una OAuth 2.0 habían delegada ámbito de permisos. La versión 2.0 de OAuth especificado ámbitos de permisos delegado pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** en el objeto [Application](application.md) ) cuando se llama a una aplicación de recursos. La propiedad **oauth2Permissions** de la entidad [ServicePrincipal](serviceprincipal.md) y de la entidad de la [aplicación](application.md) es una colección de **OAuth2Permission**.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|adminConsentDescription|String| Texto de Ayuda de permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración. |
|adminConsentDisplayName|String| Nombre para mostrar para el permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración. |
|id|Guid| Identificador de permiso de ámbito único dentro de la colección oauth2Permissions. |
|isEnabled|Boolean| Al crear o actualizar un permiso, se debe establecer esta propiedad en **true** (que es el valor predeterminado). Para eliminar un permiso, primero se debe establecer esta propiedad en **false**. En ese momento, en una llamada posterior, se puede quitar el permiso. |
|origen|String| Para uso interno. |
|type|String| Especifica si se puede aceptado este permiso ámbito por un usuario final, o si es un permiso de todo el inquilino que debe ser aceptado por un administrador de la compañía. Los valores posibles son el *usuario* o *Administrador*. |
|userConsentDescription|String| Texto de Ayuda de permiso que aparece en la experiencia de consentimiento de usuario final. |
|userConsentDisplayName|String| Nombre para mostrar para el permiso que aparece en la experiencia de consentimiento de usuario final. |
|valor|String| El valor de la notificación de ámbito que se debe esperar la aplicación de recursos en el token de acceso de OAuth 2.0. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.permissionScope"
}-->

```json
{
  "adminConsentDescription": "String",
  "adminConsentDisplayName": "String",
  "id": "Guid",
  "isEnabled": true,
  "origin": "String",
  "type": "String",
  "userConsentDescription": "String",
  "userConsentDisplayName": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "permissionScope resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->