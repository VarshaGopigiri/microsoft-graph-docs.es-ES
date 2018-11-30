---
title: tipo de recurso de la función de aplicación
description: Representa una función de aplicación que pueden solicitarse por una aplicación de cliente al llamar a otra aplicación o que se puede usar para asignar una aplicación a usuarios o grupos en una función de la aplicación especificada. La propiedad **appRoles** de la entidad servicePrincipal y de la entidad de la aplicación es una colección de **función de aplicación**.
ms.openlocfilehash: f87ef6f40fbeb18ec4b3a2373fb2a19e14da84a4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084591"
---
# <a name="approle-resource-type"></a>tipo de recurso de la función de aplicación

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una función de aplicación que pueden solicitarse por una aplicación de cliente al llamar a otra aplicación o que se puede usar para asignar una aplicación a usuarios o grupos en una función de la aplicación especificada. La propiedad **appRoles** de la entidad [servicePrincipal](serviceprincipal.md) y de la entidad de la [aplicación](application.md) es una colección de **función de aplicación**.

> Importante: Esta funcionalidad está deshabilitada en la versión actual.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.approle"
}-->

```json
{
  "allowedMemberTypes": ["string"],
  "description": "string",
  "displayName": "string",
  "id": "guid",
  "isEnabled": true,
  "origin": "string",
  "value": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowedMemberTypes|Colección String|Especifica si esta definición de rol de aplicación se puede asignar a usuarios y grupos por valor a "User", o a otras aplicaciones (que tienen acceso a esta aplicación en escenarios de servicio de demonio) estableciendo a "Aplicación", o a ambos.|
|descripción|String|Texto de ayuda que aparece en la asignación de la aplicación de administración de permisos y experiencias de consentimiento.|
|displayName|String|Nombre para mostrar para el permiso que aparece en las experiencias de asignación de consentimiento y aplicación de administración.|
|id|Guid|Identificador único de la función dentro de la colección **appRoles** .|
|isEnabled|Boolean|Al crear o actualizar una definición de rol, esto se debe establecer en **true** (que es el valor predeterminado). Para eliminar un rol, esto en primer lugar se debe establecer en **false**.  En ese momento, en una llamada posterior, se puede quitar este rol.|
|valor|String|Especifica el valor de la notificación de roles que se debe esperar la aplicación en los tokens de autenticación y acceso.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "appRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->