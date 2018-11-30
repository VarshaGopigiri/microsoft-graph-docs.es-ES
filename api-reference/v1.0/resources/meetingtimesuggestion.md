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
# <a name="meetingtimesuggestion-resource-type"></a><span data-ttu-id="0b097-103">Tipo de recurso meetingTimeSuggestion</span><span class="sxs-lookup"><span data-stu-id="0b097-103">meetingTimeSuggestion resource type</span></span>

<span data-ttu-id="0b097-104">Una sugerencia de reunión que incluye información como la hora de la reunión, posibilidad de asistencia, disponibilidad personal y ubicaciones de reuniones disponibles.</span><span class="sxs-lookup"><span data-stu-id="0b097-104">A meeting suggestion that includes information like meeting time, attendance likelihood, individual availability, and available meeting locations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0b097-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0b097-105">JSON representation</span></span>

<span data-ttu-id="0b097-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0b097-106">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="0b097-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b097-107">Properties</span></span>
| <span data-ttu-id="0b097-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b097-108">Property</span></span>     | <span data-ttu-id="0b097-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b097-109">Type</span></span>   |<span data-ttu-id="0b097-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b097-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0b097-111">attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="0b097-111">attendeeAvailability</span></span>|<span data-ttu-id="0b097-112">[attendeeAvailability](attendeeavailability.md) collection</span><span class="sxs-lookup"><span data-stu-id="0b097-112">[attendeeAvailability](attendeeavailability.md) collection</span></span>|<span data-ttu-id="0b097-113">Una matriz que muestra el estado de disponibilidad de cada asistente para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="0b097-113">An array that shows the availability status of each attendee for this meeting suggestion.</span></span>|
|<span data-ttu-id="0b097-114">confidence</span><span class="sxs-lookup"><span data-stu-id="0b097-114">confidence</span></span>|<span data-ttu-id="0b097-115">Doble</span><span class="sxs-lookup"><span data-stu-id="0b097-115">Double</span></span>|<span data-ttu-id="0b097-116">Un porcentaje que representa la probabilidad de que asistan todos los convocados.</span><span class="sxs-lookup"><span data-stu-id="0b097-116">A percentage that represents the likelhood of all the attendees attending.</span></span>|
|<span data-ttu-id="0b097-117">locations</span><span class="sxs-lookup"><span data-stu-id="0b097-117">locations</span></span>|<span data-ttu-id="0b097-118">Colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="0b097-118">[location](location.md) collection</span></span>|<span data-ttu-id="0b097-119">Una matriz que especifica el nombre y la ubicación geográfica de cada ubicación de reunión para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="0b097-119">An array that specifies the name and geographic location of each meeting location for this meeting suggestion.</span></span>|
|<span data-ttu-id="0b097-120">meetingTimeSlot</span><span class="sxs-lookup"><span data-stu-id="0b097-120">meetingTimeSlot</span></span>|[<span data-ttu-id="0b097-121">timeSlot</span><span class="sxs-lookup"><span data-stu-id="0b097-121">timeSlot</span></span>](timeslot.md)|<span data-ttu-id="0b097-122">Un período de tiempo sugerido para la reunión.</span><span class="sxs-lookup"><span data-stu-id="0b097-122">A time period suggested for the meeting.</span></span>|
|<span data-ttu-id="0b097-123">organizerAvailability</span><span class="sxs-lookup"><span data-stu-id="0b097-123">organizerAvailability</span></span>|<span data-ttu-id="0b097-124">freeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="0b097-124">freeBusyStatus</span></span>| <span data-ttu-id="0b097-125">Disponibilidad del organizador de la reunión para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="0b097-125">Availability of the meeting organizer for this meeting suggestion.</span></span> <span data-ttu-id="0b097-126">Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="0b097-126">The possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|
|<span data-ttu-id="0b097-127">suggestionReason</span><span class="sxs-lookup"><span data-stu-id="0b097-127">suggestionReason</span></span>|<span data-ttu-id="0b097-128">String</span><span class="sxs-lookup"><span data-stu-id="0b097-128">String</span></span>|<span data-ttu-id="0b097-129">Razón para proponer hora de la reunión.</span><span class="sxs-lookup"><span data-stu-id="0b097-129">Reason for suggesting the meeting time.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->