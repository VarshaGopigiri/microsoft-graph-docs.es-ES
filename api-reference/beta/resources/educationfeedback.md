---
title: tipo de recurso educationFeedback
description: Comentarios de un profesor para un estudiante. Esta propiedad representa la parte de texto de los comentarios junto con la que.
ms.openlocfilehash: 4d9a08744ac818b4aadfac965a53655d498923ab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083143"
---
# <a name="educationfeedback-resource-type"></a>tipo de recurso educationFeedback

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Comentarios de un profesor para un estudiante. Esta propiedad representa la parte de texto de los comentarios junto con la que.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|feedbackBy|[identitySet](identityset.md)|Usuario que creó los comentarios.|
|feedbackDateTime|DateTimeOffset|Momento en el tiempo cuando se asignó los comentarios. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|text|[itemBody](itembody.md)|Comentarios.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationFeedback"
}-->

```json
{
  "feedbackBy": {"@odata.type": "microsoft.graph.identitySet"},
  "feedbackDateTime": "String (timestamp)",
  "text": {"@odata.type": "microsoft.graph.itemBody"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationFeedback resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->