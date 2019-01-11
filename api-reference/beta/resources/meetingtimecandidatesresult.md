---
title: tipo de recurso meetingTimeCandidatesResult
description: Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.
localization_priority: Normal
ms.openlocfilehash: 5b261295de43dcb0bfb94f85c833559430365002
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810657"
---
# <a name="meetingtimecandidatesresult-resource-type"></a>tipo de recurso meetingTimeCandidatesResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.

Las siguientes son las posibles razones por las que [findMeetingTimes](../api/user-findmeetingtimes.md) no devuelve ninguna sugerencia de reunión.

|**valor de emptySuggestionsHint**|**Razones**|
|:-----|:-----|
| attendeesUnavailable | Se conoce la disponibilidad de todos los asistentes, pero no hay suficientes asistentes para alcanzar el umbral de confianza de la reunión en ningún horario, que de forma predeterminada es del 50%. Este umbral se basa en estado libre/ocupado los asistentes aprovechan su para una reunión sugerida período de tiempo, con el estado libre de un asistente correspondiente al 100% de posibilidades de asistencia, estado desconocido 50% y estado ocupado 0%.|
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
  "@odata.type": "microsoft.graph.meetingTimeCandidatesResult"
}-->

```json
{
  "emptySuggestionsHint": "String",
  "meetingTimeSlots": [{"@odata.type": "microsoft.graph.meetingTimeCandidate"}]
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|emptySuggestionsHint|Cadena|Un motivo por el que no se devuelven sugerencias de reunión. Los valores posibles son: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable` o `unknown`.|
|meetingTimeSlots|colección de [meetingTimeCandidate](meetingtimecandidate.md)|Matriz de sugerencias de reunión.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeCandidatesResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
