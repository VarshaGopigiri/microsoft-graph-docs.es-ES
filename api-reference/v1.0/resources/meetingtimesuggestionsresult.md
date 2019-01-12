---
title: Tipo de recurso meetingTimeSuggestionsResult
description: Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.
localization_priority: Normal
author: VinodRavichandran
ms.prod: microsoft-teams
ms.openlocfilehash: ed3af37ba48a48f3bc864dc8d9ad67e729999398
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914188"
---
# <a name="meetingtimesuggestionsresult-resource-type"></a><span data-ttu-id="095c0-103">Tipo de recurso meetingTimeSuggestionsResult</span><span class="sxs-lookup"><span data-stu-id="095c0-103">meetingTimeSuggestionsResult resource type</span></span>

<span data-ttu-id="095c0-104">Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.</span><span class="sxs-lookup"><span data-stu-id="095c0-104">A collection of meeting suggestions if there is any, or the reason if there isn't.</span></span>

<span data-ttu-id="095c0-105">Las siguientes son las posibles razones por las que [findMeetingTimes](../api/user-findmeetingtimes.md) no devuelve ninguna sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="095c0-105">The following are the possible reasons that [findMeetingTimes](../api/user-findmeetingtimes.md) does not return any meeting suggestions.</span></span>

|<span data-ttu-id="095c0-106">**valor emptySuggestionsReason**</span><span class="sxs-lookup"><span data-stu-id="095c0-106">**emptySuggestionsReason value**</span></span>|<span data-ttu-id="095c0-107">**Razones**</span><span class="sxs-lookup"><span data-stu-id="095c0-107">**Reasons**</span></span>|
|:-----|:-----|
| <span data-ttu-id="095c0-108">attendeesUnavailable</span><span class="sxs-lookup"><span data-stu-id="095c0-108">attendeesUnavailable</span></span> | <span data-ttu-id="095c0-109">Se conoce la disponibilidad de todos los asistentes, pero no hay suficientes asistentes para alcanzar el umbral de [confianza de la reunión](../api/user-findmeetingtimes.md#the-confidence-of-a-meeting-suggestion) en ningún horario, que de forma predeterminada es del 50%.</span><span class="sxs-lookup"><span data-stu-id="095c0-109">All of the attendees' availability is known, but not enough attendees are available to reach the [meeting confidence](../api/user-findmeetingtimes.md#the-confidence-of-a-meeting-suggestion) threshold, which is 50% by default, for any time period.</span></span>|
| <span data-ttu-id="095c0-110">attendeesUnavailableOrUnknown</span><span class="sxs-lookup"><span data-stu-id="095c0-110">attendeesUnavailableOrUnknown</span></span> | <span data-ttu-id="095c0-p101">Algunos (o todos) los asistentes tienen una disponibilidad desconocida, lo que provoca que la confianza en la reunión caiga por debajo del umbral establecido, que de forma predeterminada es del 50%. La disponibilidad de los asistentes puede ser desconocida si estos se encuentran fuera de la organización, o si hay un error al obtener la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="095c0-p101">Some or all of the attendees have unknown availability, causing the meeting confidence to fall below the set threshold, which is 50% by default. Attendee availability can become unknown if the attendee is outside of the organization, or there is an error obtaining free/busy information.</span></span>|
| <span data-ttu-id="095c0-113">locationsUnavailable</span><span class="sxs-lookup"><span data-stu-id="095c0-113">locationsUnavailable</span></span> | <span data-ttu-id="095c0-114">La propiedad **isRequired** del parámetro [locationConstraint](locationconstraint.md) se especifica como obligatoria, aún no hay ninguna ubicación disponible para las franjas de tiempo calculadas.</span><span class="sxs-lookup"><span data-stu-id="095c0-114">The **isRequired** property of the [locationConstraint](locationconstraint.md) parameter is specified as mandatory, and yet there are no locations available at the calculated time slots.</span></span> |
| <span data-ttu-id="095c0-115">organizerUnavailable</span><span class="sxs-lookup"><span data-stu-id="095c0-115">organizerUnavailable</span></span> | <span data-ttu-id="095c0-116">El parámetro **isOrganizerOptional** es falso y el organizador aún no está disponible durante el tiempo solicitado.</span><span class="sxs-lookup"><span data-stu-id="095c0-116">The **isOrganizerOptional** parameter is false and yet the organizer is not available during the requested time window.</span></span> |
| <span data-ttu-id="095c0-117">desconocido</span><span class="sxs-lookup"><span data-stu-id="095c0-117">unknown</span></span> | <span data-ttu-id="095c0-118">No se conoce el motivo por el que no se devuelven sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="095c0-118">The reason for not returning any meeting suggestions is not known.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="095c0-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="095c0-119">JSON representation</span></span>

<span data-ttu-id="095c0-120">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="095c0-120">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="095c0-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="095c0-121">Properties</span></span>
| <span data-ttu-id="095c0-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="095c0-122">Property</span></span>     | <span data-ttu-id="095c0-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="095c0-123">Type</span></span>   |<span data-ttu-id="095c0-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="095c0-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="095c0-125">emptySuggestionsReason</span><span class="sxs-lookup"><span data-stu-id="095c0-125">emptySuggestionsReason</span></span>|<span data-ttu-id="095c0-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="095c0-126">String</span></span>|<span data-ttu-id="095c0-127">Una razón para no devolver cualquier sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="095c0-127">A reason for not returning any meeting suggestions.</span></span> <span data-ttu-id="095c0-128">Los valores posibles son: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable`, o `unknown`.</span><span class="sxs-lookup"><span data-stu-id="095c0-128">The possible values are: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable`, or `unknown`.</span></span> <span data-ttu-id="095c0-129">Esta propiedad es una cadena vacía si la propiedad **meetingTimeSuggestions** incluye cualquier sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="095c0-129">This property is an empty string if the **meetingTimeSuggestions** property does include any meeting suggestions.</span></span>|
|<span data-ttu-id="095c0-130">meetingTimeSuggestions</span><span class="sxs-lookup"><span data-stu-id="095c0-130">meetingTimeSuggestions</span></span>|<span data-ttu-id="095c0-131">[meetingTimeSuggestion](meetingtimesuggestion.md) collection</span><span class="sxs-lookup"><span data-stu-id="095c0-131">[meetingTimeSuggestion](meetingtimesuggestion.md) collection</span></span>|<span data-ttu-id="095c0-132">Matriz de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="095c0-132">An array of meeting suggestions.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestionsResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
