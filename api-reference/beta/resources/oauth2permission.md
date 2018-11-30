---
title: tipo de recurso oAuth2Permission
description: Representa una OAuth 2.0 habían delegada ámbito de permisos. La versión 2.0 de OAuth especificado ámbitos de permisos delegado pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** en el objeto application) cuando se llama a una aplicación de recursos. La propiedad **appRoles** de la entidad servicePrincipal y de la entidad de la aplicación es una colección de **oAuth2Permission**.
ms.openlocfilehash: 4a790c935dd84fb7bd4e1422ca59914d9a319ae9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088635"
---
# <a name="oauth2permission-resource-type"></a>tipo de recurso oAuth2Permission

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una OAuth 2.0 habían delegada ámbito de permisos. La versión 2.0 de OAuth especificado ámbitos de permisos delegado pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** en el objeto [application](application.md) ) cuando se llama a una aplicación de recursos. La propiedad **appRoles** de la entidad [servicePrincipal](serviceprincipal.md) y de la entidad de la [aplicación](application.md) es una colección de **oAuth2Permission**.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.oAuth2Permission"
}-->

```json
{
  "adminConsentDescription": "string",
  "adminConsentDisplayName": "string",
  "id": "guid",
  "isEnabled": true,
  "origin": "string",
  "type": "string",
  "userConsentDescription": "string",
  "userConsentDisplayName": "string",
  "value": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|adminConsentDescription|String|Texto de Ayuda de permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración.|
|adminConsentDisplayName|String|Nombre para mostrar para el permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración.|
|id|Guid|Identificador de permiso de ámbito único dentro de la colección oauth2Permissions.|
|isEnabled|Boolean|Al crear o actualizar un permiso, se debe establecer esta propiedad en **true** (que es el valor predeterminado). Para eliminar un permiso, primero se debe establecer esta propiedad en **false**.  En ese momento, en una llamada posterior, se puede quitar el permiso.|
|type|String|Especifica si se puede aceptado este permiso ámbito por un usuario final, o si es un permiso de todo el inquilino que debe ser aceptado por un administrador de la compañía.  Los valores posibles son "Usuario" o "Administrador".|
|userConsentDescription|String|Texto de Ayuda de permiso que aparece en la experiencia de consentimiento de usuario final.|
|userConsentDisplayName|String|Nombre para mostrar para el permiso que aparece en la experiencia de consentimiento de usuario final.|
|valor|String|El valor de la notificación de ámbito que se debe esperar la aplicación de recursos en el token de acceso de OAuth 2.0.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "oAuth2Permission resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
