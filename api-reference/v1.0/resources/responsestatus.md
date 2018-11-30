---
title: Tipo de recurso responseStatus
description: Estado de la respuesta de una convocatoria de reunión.
ms.openlocfilehash: 95f525bae387520888f006d6496a56dab9148145
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029503"
---
# <a name="responsestatus-resource-type"></a>Tipo de recurso responseStatus

Estado de la respuesta de una convocatoria de reunión.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo           | Descripción |
|:---------|:---------------|:------------|
| response | responseType   | Tipo de la respuesta. Los valores posibles son: `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined`, `NotResponded`.
| time     | DateTimeOffset | Fecha y hora en que se devolvió la respuesta. Usa el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.responseStatus"
}-->

```json
{
  "response": "String",
  "time": "String (timestamp)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "responseStatus resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
