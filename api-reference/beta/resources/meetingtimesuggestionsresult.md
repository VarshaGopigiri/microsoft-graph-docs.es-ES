---
title: Tipo de recurso meetingTimeSuggestionsResult
description: Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.
ms.openlocfilehash: 2c6cb28ea0ec899e693300b321c652fb814582f1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089778"
---
# <a name="meetingtimesuggestionsresult-resource-type"></a>Tipo de recurso meetingTimeSuggestionsResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.

Las siguientes son las posibles razones por las que [findMeetingTimes](../api/user-findmeetingtimes.md) no devuelve ninguna sugerencia de reunión.

|**valor emptySuggestionsReason**|**Razones**|
|:-----|:-----|
| attendeesUnavailable | Se conoce la disponibilidad de todos los asistentes, pero no hay suficientes asistentes para alcanzar el umbral de [confianza de la reunión](../api/user-findmeetingtimes.md#the-confidence-of-a-meeting-suggestion) en ningún horario, que de forma predeterminada es del 50%.|
| attendeesUnavailableOrUnknown | Algunos (o todos) los asistentes tienen una disponibilidad desconocida, lo que provoca que la confianza en la reunión caiga por debajo del umbral establecido, que de forma predeterminada es del 50%. La disponibilidad de los asistentes puede ser desconocida si estos se encuentran fuera de la organización, o si hay un error al obtener la información de disponibilidad.|
| locationsUnavailable | La propiedad **isRequired** del parámetro [locationConstraint](locationconstraint.md) se especifica como obligatoria, aún no hay ninguna ubicación disponible para las franjas de tiempo calculadas. |
| organizerUnavailable | El parámetro **isOrganizerOptional** es falso y el organizador aún no está disponible durante el tiempo solicitado. |
| desconocido | No se conoce el motivo por el que no se devuelven sugerencias de reunión.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingTimeSuggestionsResult"
}-->

```json
{
  "emptySuggestionsReason": "String",
  "meetingTimeSuggestions": [{"@odata.type": "microsoft.graph.meetingTimeSuggestion"}]
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|emptySuggestionsReason|String|Un motivo por el que no se devuelven sugerencias de reunión. Los valores posibles son: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable` o `unknown`. Esta propiedad es una cadena vacía si la propiedad **meetingTimeSuggestions** incluye alguna sugerencia de reunión.|
|meetingTimeSuggestions|[meetingTimeSuggestion](meetingtimesuggestion.md) collection|Matriz de sugerencias de reunión.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestionsResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->