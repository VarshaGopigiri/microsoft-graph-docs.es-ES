---
title: Tipo de recurso scoredEmailAddress
description: Representa una dirección de correo electrónico con puntuación.
localization_priority: Normal
ms.openlocfilehash: 740173e7d5f93dc875c08508bf73100727fdf415
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819477"
---
# <a name="scoredemailaddress-resource-type"></a>Tipo de recurso scoredEmailAddress

Representa una dirección de correo electrónico con puntuación.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|address|string|La dirección de correo electrónico.|
|relevanceScore|double|La puntuación de relevancia de la dirección de correo electrónico. Una puntuación de relevancia se usa como criterio de ordenación con respecto a los demás resultados devueltos. Un valor de puntuación de relevancia más alto corresponde a un resultado más relevante. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scoredEmailAddress"
}-->

```json
{
  "address": "string",
  "relevanceScore": 1024.0
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scoredEmailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
