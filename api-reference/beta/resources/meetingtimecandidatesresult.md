---
title: tipo de recurso meetingTimeCandidatesResult
description: Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.
ms.openlocfilehash: 38ca5b6be15d3cd268403f7f95645a8aaf31cf9d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083863"
---
# <a name="meetingtimecandidatesresult-resource-type"></a><span data-ttu-id="14024-103">tipo de recurso meetingTimeCandidatesResult</span><span class="sxs-lookup"><span data-stu-id="14024-103">meetingTimeCandidatesResult resource type</span></span>

> <span data-ttu-id="14024-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="14024-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="14024-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="14024-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="14024-106">Una colección de sugerencias para la reunión, en caso de haberla, o el motivo de su cancelación, en caso de que se produzca.</span><span class="sxs-lookup"><span data-stu-id="14024-106">A collection of meeting suggestions if there is any, or the reason if there isn't.</span></span>

<span data-ttu-id="14024-107">Las siguientes son las posibles razones por las que [findMeetingTimes](../api/user-findmeetingtimes.md) no devuelve ninguna sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="14024-107">The following are the possible reasons that [findMeetingTimes](../api/user-findmeetingtimes.md) does not return any meeting suggestions.</span></span>

|<span data-ttu-id="14024-108">**valor de emptySuggestionsHint**</span><span class="sxs-lookup"><span data-stu-id="14024-108">**emptySuggestionsHint value**</span></span>|<span data-ttu-id="14024-109">**Razones**</span><span class="sxs-lookup"><span data-stu-id="14024-109">**Reasons**</span></span>|
|:-----|:-----|
| <span data-ttu-id="14024-110">attendeesUnavailable</span><span class="sxs-lookup"><span data-stu-id="14024-110">attendeesUnavailable</span></span> | <span data-ttu-id="14024-111">Se conoce la disponibilidad de todos los asistentes, pero no hay suficientes asistentes para alcanzar el umbral de confianza de la reunión en ningún horario, que de forma predeterminada es del 50%.</span><span class="sxs-lookup"><span data-stu-id="14024-111">All of the attendees' availability is known, but not enough attendees are available to reach the meeting confidence threshold, which is 50% by default, for any time period.</span></span> <span data-ttu-id="14024-112">Este umbral se basa en estado libre/ocupado los asistentes aprovechan su para una reunión sugerida período de tiempo, con el estado libre de un asistente correspondiente al 100% de posibilidades de asistencia, estado desconocido 50% y estado ocupado 0%.</span><span class="sxs-lookup"><span data-stu-id="14024-112">This threshold is based on the attendees' free/busy status for a suggested meeting time period, with an attendee's free status corresponding to 100% chance of attendance, unknown status 50%, and busy status 0%.</span></span>|
| <span data-ttu-id="14024-113">attendeesUnavailableOrUnknown</span><span class="sxs-lookup"><span data-stu-id="14024-113">attendeesUnavailableOrUnknown</span></span> | <span data-ttu-id="14024-p103">Algunos (o todos) los asistentes tienen una disponibilidad desconocida, lo que provoca que la confianza en la reunión caiga por debajo del umbral establecido, que de forma predeterminada es del 50%. La disponibilidad de los asistentes puede ser desconocida si estos se encuentran fuera de la organización, o si hay un error al obtener la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="14024-p103">Some or all of the attendees have unknown availability, causing the meeting confidence to fall below the set threshold, which is 50% by default. Attendee availability can become unknown if the attendee is outside of the organization, or there is an error obtaining free/busy information.</span></span>|
| <span data-ttu-id="14024-116">locationsUnavailable</span><span class="sxs-lookup"><span data-stu-id="14024-116">locationsUnavailable</span></span> | <span data-ttu-id="14024-117">La propiedad **isRequired** del parámetro [locationConstraint](locationconstraint.md) se especifica como obligatoria, aún no hay ninguna ubicación disponible para las franjas de tiempo calculadas.</span><span class="sxs-lookup"><span data-stu-id="14024-117">The **isRequired** property of the [locationConstraint](locationconstraint.md) parameter is specified as mandatory, and yet there are no locations available at the calculated time slots.</span></span> |
| <span data-ttu-id="14024-118">organizerUnavailable</span><span class="sxs-lookup"><span data-stu-id="14024-118">organizerUnavailable</span></span> | <span data-ttu-id="14024-119">El parámetro **isOrganizerOptional** es falso y el organizador aún no está disponible durante el tiempo solicitado.</span><span class="sxs-lookup"><span data-stu-id="14024-119">The **isOrganizerOptional** parameter is false and yet the organizer is not available during the requested time window.</span></span> |
| <span data-ttu-id="14024-120">desconocido</span><span class="sxs-lookup"><span data-stu-id="14024-120">unknown</span></span> | <span data-ttu-id="14024-121">No se conoce el motivo por el que no se devuelven sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="14024-121">The reason for not returning any meeting suggestions is not known.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="14024-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="14024-122">JSON representation</span></span>

<span data-ttu-id="14024-123">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="14024-123">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="14024-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14024-124">Properties</span></span>
| <span data-ttu-id="14024-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="14024-125">Property</span></span>     | <span data-ttu-id="14024-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="14024-126">Type</span></span>   |<span data-ttu-id="14024-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="14024-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="14024-128">emptySuggestionsHint</span><span class="sxs-lookup"><span data-stu-id="14024-128">emptySuggestionsHint</span></span>|<span data-ttu-id="14024-129">String</span><span class="sxs-lookup"><span data-stu-id="14024-129">String</span></span>|<span data-ttu-id="14024-p104">Un motivo por el que no se devuelven sugerencias de reunión. Los valores posibles son: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable` o `unknown`.</span><span class="sxs-lookup"><span data-stu-id="14024-p104">A reason for not returning any meeting suggestions. Possible values are: `attendeesUnavailable`, `attendeesUnavailableOrUnknown`, `locationsUnavailable`, `organizerUnavailable`, or `unknown`.</span></span>|
|<span data-ttu-id="14024-132">meetingTimeSlots</span><span class="sxs-lookup"><span data-stu-id="14024-132">meetingTimeSlots</span></span>|<span data-ttu-id="14024-133">colección de [meetingTimeCandidate](meetingtimecandidate.md)</span><span class="sxs-lookup"><span data-stu-id="14024-133">[meetingTimeCandidate](meetingtimecandidate.md) collection</span></span>|<span data-ttu-id="14024-134">Matriz de sugerencias de reunión.</span><span class="sxs-lookup"><span data-stu-id="14024-134">An array of meeting suggestions.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeCandidatesResult resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->