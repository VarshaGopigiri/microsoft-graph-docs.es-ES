---
title: tipo de recurso preAuthorizedApplication
description: Representa una aplicación y los permisos solicitados para consentimiento implícito. Requiere un administrador que se ha proporcionado el consentimiento a la aplicación. preAuthorizedApplications no requieren el usuario da su consentimiento a los permisos solicitados. Los permisos enumerados en preAuthorizedApplications no requieren el consentimiento de usuario. Sin embargo, los permisos solicitados adicionales no aparece en preAuthorizedApplications requieren el consentimiento de usuario.
localization_priority: Normal
ms.openlocfilehash: fa26b8046b81db70300b8ff40abcbd2b84f3f0c8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832798"
---
# <a name="preauthorizedapplication-resource-type"></a>tipo de recurso preAuthorizedApplication

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una aplicación y los permisos solicitados para consentimiento implícito. Requiere un administrador que se ha proporcionado el consentimiento a la aplicación. preAuthorizedApplications no requieren el usuario da su consentimiento a los permisos solicitados. Los permisos enumerados en preAuthorizedApplications no requieren el consentimiento de usuario. Sin embargo, los permisos solicitados adicionales no aparece en preAuthorizedApplications requieren el consentimiento de usuario.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:---------------|:--------|:----------|
|appId|cadena| El identificador único para la aplicación. |
|permissionIds|Colección String| Se requiere el identificador único para el [publishedPermissionScope](permissionscope.md) o la [función de aplicación](approle.md) de la aplicación. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.preAuthorizedApplication"
}-->

```json
{
  "appId": "String",
  "permissionIds": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "preAuthorizedApplication resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
