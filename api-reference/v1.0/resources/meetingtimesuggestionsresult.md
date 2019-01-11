---
title: Tipo de recurso meetingTimeSuggestionsResult
description: Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.
localization_priority: Normal
ms.openlocfilehash: 85a0c3ade54204cb78957e81325869197f403c5d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823698"
---
# <a name="meetingtimesuggestionsresult-resource-type"></a><span data-ttu-id="74694-103">Tipo de recurso meetingTimeSuggestionsResult</span><span class="sxs-lookup"><span data-stu-id="74694-103">meetingTimeSuggestionsResult resource type</span></span>

<span data-ttu-id="74694-104">Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.</span><span class="sxs-lookup"><span data-stu-id="74694-104">A collection of meeting suggestions if there is any, or the reason if there isn't.</span></span>

<span data-ttu-id="74694-105">Las siguientes son las posibles razones por las que [findMeetingTimes](../api/user-findmeetingtimes.md) no devuelve ninguna sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="74694-105">The following are the possible reasons that [findMeetingTimes](../api/user-findmeetingtimes.md) does not return any meeting suggestions.</span></span>

|<span data-ttu-id="74694-106">**valor emptySuggestionsReason**</span><span class="sxs-lookup"><span data-stu-id="74694-106">**emptySuggestionsReason value**</span></span>|<span data-ttu-id="74694-107">**Razones**</span><span class="sxs-lookup"><span data-stu-id="74694-107">**Reasons**</span></span>|
|:-----|:-----|
| <span data-ttu-id="74694-108">attendeesUnavailable</span><span class="sxs-lookup"><span data-stu-id="74694-108">attendeesUnavailable</span></span> | <span data-ttu-id="74694-109">Se conoce la disponibilidad de todos los asistentes, pero no hay suficientes asistentes para alcanzar el umbral de [confianza de la reunión](../api/user-findmeetingtimes.md#the-confidence-of-a-meeting-suggestion) en ningún horario, que de forma predeterminada es del 50%.</span><span class="sxs-lookup"><span data-stu-id="74694-109">All of the attendees' availability is known, but not enough attendees are available to reach the [meeting confidence](../api/user-findmeetingtimes.md#the-confidence-of-a-meeting-suggestion) threshold, which is 50% by default, for any time period.</span></span>|
| <span data-ttu-id="74694-110">attendeesUnavailableOrUnknown</span><span class="sxs-lookup"><span data-stu-id="74694-110">attendeesUnavailableOrUnknown</span></span> | <span data-ttu-id="74694-p101">Algunos (o todos) los asistentes tienen una disponibilidad desconocida, lo que provoca que la confianza en la reunión caiga por debajo del umbral establecido, que de forma predeterminada es del 50%. La disponibilidad de los asistentes puede ser desconocida si estos se encuentran fuera de la organización, o si hay un error al obtener la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="74694-p101">Some or all of the attendees have unknown availability, causing the meeting confidence to fall below the set threshold, which is 50% by default. Attendee availability can become unknown if the attendee is outside of the organization, or there is an error obtaining free/busy information.</span></span>|
| <span data-ttu-id="74694-113">locationsUnavailable</span><span class="sxs-lookup"><span data-stu-id="74694-113">locationsUnavailable</span></span> | <span data-ttu-id="74694-114">La propiedad **isRequired** del parámetro [locationConstraint](locationconstraint.md) se especifica como obligatoria, aún no hay ninguna ubicación disponible para las franjas de tiempo calculadas.</span><span class="sxs-lookup"><span data-stu-id="74694-114">The **isRequired** property of the [locationConstraint](locationconstraint.md) parameter is specified as mandatory, and yet there are no locations available at the calculated time slots.</span></span> |
| <span data-ttu-id="74694-115">organizerUnavailable</span><span class="sxs-lookup"><span data-stu-id="74694-115">organizerUnavailable</span></span> | <span data-ttu-id="74694-116">El parámetro **isOrganizerOptional** es falso y el organizador aún no está disponible durante el tiempo solicitado.</span><span class="sxs-lookup"><span data-stu-id="74694-116">The **isOrganizerOptional** parameter is false and yet the organizer is not available during the requested time window.</span></span> |
| <span data-ttu-id="74694-117">desconocido</span><span class="sxs-lookup"><span data-stu-id="74694-117">unknown</span></span> | <span data-ttu-id="74694-118">No se conoce el motivo por el que no se devuelven sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="74694-118">The reason for not returning any meeting suggestions is not known.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="74694-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="74694-119">JSON representation</span></span>

<span data-ttu-id="74694-120">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="74694-120">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="74694-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="74694-121">Properties</span></span>
| <span data-ttu-id="74694-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="74694-122">Property</span></span>     | <span data-ttu-id="74694-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="74694-123">Type</span></span>   |<span data-ttu-id="74694-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="74694-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="74694-125">emptySuggestionsReason</span><span class="sxs-lookup"><span data-stu-id="74694-125">emptySuggestionsReason</span></span>|<span data-ttu-id="74694-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="74694-126">String</span></span>|<span data-ttu-id="74694-127">Una razón para no devolver cualquier sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="74694-127">A reason for not returning any meeting suggestions.</span></span> <span data-ttu-id="74694-128">Los valores posibles son: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable`, o `unknown`.</span><span class="sxs-lookup"><span data-stu-id="74694-128">The possible values are: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable`, or `unknown`.</span></span> <span data-ttu-id="74694-129">Esta propiedad es una cadena vacía si la propiedad **meetingTimeSuggestions** incluye cualquier sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="74694-129">This property is an empty string if the **meetingTimeSuggestions** property does include any meeting suggestions.</span></span>|
|<span data-ttu-id="74694-130">meetingTimeSuggestions</span><span class="sxs-lookup"><span data-stu-id="74694-130">meetingTimeSuggestions</span></span>|<span data-ttu-id="74694-131">[meetingTimeSuggestion](meetingtimesuggestion.md) collection</span><span class="sxs-lookup"><span data-stu-id="74694-131">[meetingTimeSuggestion](meetingtimesuggestion.md) collection</span></span>|<span data-ttu-id="74694-132">Matriz de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="74694-132">An array of meeting suggestions.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestionsResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
