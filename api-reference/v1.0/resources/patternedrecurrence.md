---
title: Tipo de recurso patternedRecurrence
description: Patrón e intervalo de periodicidad.
ms.openlocfilehash: 10a90db032cd7461e28bc096fd6213df44f3ea45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029602"
---
# <a name="patternedrecurrence-resource-type"></a>Tipo de recurso patternedRecurrence

Patrón e intervalo de periodicidad.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|pattern|[RecurrencePattern](recurrencepattern.md)|Frecuencia de un evento.|
|range|[RecurrenceRange](recurrencerange.md)|Duración de un evento.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.patternedRecurrence"
}-->

```json
{
  "pattern": {"@odata.type": "microsoft.graph.recurrencePattern"},
  "range": {"@odata.type": "microsoft.graph.recurrenceRange"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "patternedRecurrence resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
