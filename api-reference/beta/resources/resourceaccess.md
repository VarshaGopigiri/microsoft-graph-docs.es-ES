---
title: tipo de recurso resourceAccess
description: Especifica un ámbito de permiso OAuth 2.0 o una función de aplicación que requiere una aplicación. La propiedad **resourceAccess** del tipo requiredResourceAccess es una colección de **ResourceAccess**.
localization_priority: Normal
ms.openlocfilehash: f5389915897c3aab8b8277a45b54042bc861b290
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862338"
---
# <a name="resourceaccess-resource-type"></a>tipo de recurso resourceAccess

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica un ámbito de permiso OAuth 2.0 o una función de aplicación que requiere una aplicación. La propiedad **resourceAccess** del tipo [requiredResourceAccess](requiredresourceaccess.md) es una colección de **ResourceAccess**.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.resourceAccess"
}-->

```json
{
  "id": "guid",
  "type": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Guid|El identificador único para una de las instancias de [oAuth2Permission](oauth2permission.md) o [función de aplicación](approle.md) que expone la aplicación de recursos.|
|type|Cadena|Especifica si la propiedad **id** hace referencia a un [oAuth2Permission](oauth2permission.md) o una [función de aplicación](approle.md). Los valores posibles son "ámbito" o "role".|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resourceAccess resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
