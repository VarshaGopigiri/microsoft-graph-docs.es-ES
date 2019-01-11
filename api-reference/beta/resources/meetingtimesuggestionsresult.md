---
title: Tipo de recurso meetingTimeSuggestionsResult
description: Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.
localization_priority: Normal
ms.openlocfilehash: aff5abd69297cd466027c1a614b2609697c00ce6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806842"
---
# <a name="meetingtimesuggestionsresult-resource-type"></a><span data-ttu-id="24af6-103">Tipo de recurso meetingTimeSuggestionsResult</span><span class="sxs-lookup"><span data-stu-id="24af6-103">meetingTimeSuggestionsResult resource type</span></span>

> <span data-ttu-id="24af6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="24af6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="24af6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="24af6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="24af6-106">Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.</span><span class="sxs-lookup"><span data-stu-id="24af6-106">A collection of meeting suggestions if there is any, or the reason if there isn't.</span></span>

<span data-ttu-id="24af6-107">Las siguientes son las posibles razones por las que [findMeetingTimes](../api/user-findmeetingtimes.md) no devuelve ninguna sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="24af6-107">The following are the possible reasons that [findMeetingTimes](../api/user-findmeetingtimes.md) does not return any meeting suggestions.</span></span>

|<span data-ttu-id="24af6-108">**valor emptySuggestionsReason**</span><span class="sxs-lookup"><span data-stu-id="24af6-108">**emptySuggestionsReason value**</span></span>|<span data-ttu-id="24af6-109">**Razones**</span><span class="sxs-lookup"><span data-stu-id="24af6-109">**Reasons**</span></span>|
|:-----|:-----|
| <span data-ttu-id="24af6-110">attendeesUnavailable</span><span class="sxs-lookup"><span data-stu-id="24af6-110">attendeesUnavailable</span></span> | <span data-ttu-id="24af6-111">Se conoce la disponibilidad de todos los asistentes, pero no hay suficientes asistentes para alcanzar el umbral de [confianza de la reunión](../api/user-findmeetingtimes.md#the-confidence-of-a-meeting-suggestion) en ningún horario, que de forma predeterminada es del 50%.</span><span class="sxs-lookup"><span data-stu-id="24af6-111">All of the attendees' availability is known, but not enough attendees are available to reach the [meeting confidence](../api/user-findmeetingtimes.md#the-confidence-of-a-meeting-suggestion) threshold, which is 50% by default, for any time period.</span></span>|
| <span data-ttu-id="24af6-112">attendeesUnavailableOrUnknown</span><span class="sxs-lookup"><span data-stu-id="24af6-112">attendeesUnavailableOrUnknown</span></span> | <span data-ttu-id="24af6-p102">Algunos (o todos) los asistentes tienen una disponibilidad desconocida, lo que provoca que la confianza en la reunión caiga por debajo del umbral establecido, que de forma predeterminada es del 50%. La disponibilidad de los asistentes puede ser desconocida si estos se encuentran fuera de la organización, o si hay un error al obtener la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="24af6-p102">Some or all of the attendees have unknown availability, causing the meeting confidence to fall below the set threshold, which is 50% by default. Attendee availability can become unknown if the attendee is outside of the organization, or there is an error obtaining free/busy information.</span></span>|
| <span data-ttu-id="24af6-115">locationsUnavailable</span><span class="sxs-lookup"><span data-stu-id="24af6-115">locationsUnavailable</span></span> | <span data-ttu-id="24af6-116">La propiedad **isRequired** del parámetro [locationConstraint](locationconstraint.md) se especifica como obligatoria, aún no hay ninguna ubicación disponible para las franjas de tiempo calculadas.</span><span class="sxs-lookup"><span data-stu-id="24af6-116">The **isRequired** property of the [locationConstraint](locationconstraint.md) parameter is specified as mandatory, and yet there are no locations available at the calculated time slots.</span></span> |
| <span data-ttu-id="24af6-117">organizerUnavailable</span><span class="sxs-lookup"><span data-stu-id="24af6-117">organizerUnavailable</span></span> | <span data-ttu-id="24af6-118">El parámetro **isOrganizerOptional** es falso y el organizador aún no está disponible durante el tiempo solicitado.</span><span class="sxs-lookup"><span data-stu-id="24af6-118">The **isOrganizerOptional** parameter is false and yet the organizer is not available during the requested time window.</span></span> |
| <span data-ttu-id="24af6-119">desconocido</span><span class="sxs-lookup"><span data-stu-id="24af6-119">unknown</span></span> | <span data-ttu-id="24af6-120">No se conoce el motivo por el que no se devuelven sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="24af6-120">The reason for not returning any meeting suggestions is not known.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="24af6-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="24af6-121">JSON representation</span></span>

<span data-ttu-id="24af6-122">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="24af6-122">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="24af6-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24af6-123">Properties</span></span>
| <span data-ttu-id="24af6-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="24af6-124">Property</span></span>     | <span data-ttu-id="24af6-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="24af6-125">Type</span></span>   |<span data-ttu-id="24af6-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="24af6-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="24af6-127">emptySuggestionsReason</span><span class="sxs-lookup"><span data-stu-id="24af6-127">emptySuggestionsReason</span></span>|<span data-ttu-id="24af6-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="24af6-128">String</span></span>|<span data-ttu-id="24af6-p103">Un motivo por el que no se devuelven sugerencias de reunión. Los valores posibles son: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable` o `unknown`. Esta propiedad es una cadena vacía si la propiedad **meetingTimeSuggestions** incluye alguna sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="24af6-p103">A reason for not returning any meeting suggestions. Possible values are: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable`, or `unknown`. This property is an empty string if the **meetingTimeSuggestions** property does include any meeting suggestions.</span></span>|
|<span data-ttu-id="24af6-132">meetingTimeSuggestions</span><span class="sxs-lookup"><span data-stu-id="24af6-132">meetingTimeSuggestions</span></span>|<span data-ttu-id="24af6-133">[meetingTimeSuggestion](meetingtimesuggestion.md) collection</span><span class="sxs-lookup"><span data-stu-id="24af6-133">[meetingTimeSuggestion](meetingtimesuggestion.md) collection</span></span>|<span data-ttu-id="24af6-134">Matriz de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="24af6-134">An array of meeting suggestions.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestionsResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
