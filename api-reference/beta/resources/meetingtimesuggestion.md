---
title: Tipo de recurso meetingTimeSuggestion
description: 'Una sugerencia de reunión que incluye información como el tiempo de la reunión, la probabilidad de asistencia, individual '
localization_priority: Normal
author: VinodRavichandran
ms.prod: microsoft-teams
ms.openlocfilehash: 6c7adf6d3b31ebdd5a068f71572b80141736a0bf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956118"
---
# <a name="meetingtimesuggestion-resource-type"></a>Tipo de recurso meetingTimeSuggestion

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
  "confidence": 1024.0,
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
|organizerAvailability|Cadena| Disponibilidad del organizador de la reunión para esta sugerencia de reunión. Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.|
|suggestionReason|Cadena|Razón para proponer hora de la reunión.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
