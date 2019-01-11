---
title: tipo de recurso requiredResourceAccess
description: Especifica el conjunto de OAuth 2.0 ámbitos de permisos y roles de la aplicación en el recurso especificado que una aplicación necesita tener acceso a. Los ámbitos de permisos especificados OAuth 2.0 pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** ) cuando una llamada a una aplicación de recursos. La propiedad **requiredResourceAccess** de la entidad de la aplicación es una colección de **ReqiredResourceAccess**.
localization_priority: Normal
ms.openlocfilehash: 473126365a7f0b3ba3ab0371322ff90bd36318e3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856171"
---
# <a name="requiredresourceaccess-resource-type"></a>tipo de recurso requiredResourceAccess

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica el conjunto de OAuth 2.0 ámbitos de permisos y roles de la aplicación en el recurso especificado que una aplicación necesita tener acceso a. Los ámbitos de permisos especificados OAuth 2.0 pueden solicitarse por las aplicaciones de cliente (a través de la colección **requiredResourceAccess** ) cuando una llamada a una aplicación de recursos. La propiedad **requiredResourceAccess** de la entidad de la [aplicación](application.md) es una colección de **ReqiredResourceAccess**.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.requiredResourceAccess"
}-->

```json
{
  "resourceAccess": [{"@odata.type": "microsoft.graph.resourceAccess"}],
  "resourceAppId": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|resourceAccess|Colección de [ResourceAccess](resourceaccess.md)|La lista de ámbitos de OAuth2.0 de permisos y roles de la aplicación que requiere la aplicación desde el recurso especificado.|
|resourceAppId|Cadena|El identificador único para el recurso que la aplicación necesita tener acceso a.  Debe ser igual que el **appId** declaradas en la aplicación de destino de recursos.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "requiredResourceAccess resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
