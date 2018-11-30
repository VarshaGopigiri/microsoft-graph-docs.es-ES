---
title: Tipo de recurso meetingTimeSuggestion
description: 'Una sugerencia de reunión que incluye información como el tiempo de la reunión, la probabilidad de asistencia, individual '
ms.openlocfilehash: 345d09015be5e489c88cb89fe6a4175ebbab2874
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032280"
---
# <a name="meetingtimesuggestion-resource-type"></a>Tipo de recurso meetingTimeSuggestion

Una sugerencia de reunión que incluye información como la hora de la reunión, posibilidad de asistencia, disponibilidad personal y ubicaciones de reuniones disponibles.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingTimeSuggestion"
}-->

```json
{
  "attendeeAvailability": [{"@odata.type": "microsoft.graph.attendeeAvailability"}],
  "confidence": 100.0,
  "locations": [{"@odata.type": "microsoft.graph.location"}],
  "meetingTimeSlot": {"@odata.type": "microsoft.graph.timeSlot"},
  "organizerAvailability": "String",
  "suggestionReason": "String"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attendeeAvailability|[attendeeAvailability](attendeeavailability.md) collection|Una matriz que muestra el estado de disponibilidad de cada asistente para esta sugerencia de reunión.|
|confidence|Doble|Un porcentaje que representa la probabilidad de que asistan todos los convocados.|
|locations|Colección [location](location.md)|Una matriz que especifica el nombre y la ubicación geográfica de cada ubicación de reunión para esta sugerencia de reunión.|
|meetingTimeSlot|[timeSlot](timeslot.md)|Un período de tiempo sugerido para la reunión.|
|organizerAvailability|freeBusyStatus| Disponibilidad del organizador de la reunión para esta sugerencia de reunión. Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.|
|suggestionReason|String|Razón para proponer hora de la reunión.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->