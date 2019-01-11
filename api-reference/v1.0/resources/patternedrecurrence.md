---
title: Tipo de recurso patternedRecurrence
description: Patrón e intervalo de periodicidad.
localization_priority: Normal
ms.openlocfilehash: 8a9581150e3b7790f32268eb34f35b22abcb3642
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840799"
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
