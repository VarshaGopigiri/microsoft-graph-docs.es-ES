---
title: Tipo de recurso meetingTimeSuggestion
description: 'Una sugerencia de reunión que incluye información como el tiempo de la reunión, la probabilidad de asistencia, individual '
localization_priority: Normal
author: VinodRavichandran
ms.prod: microsoft-teams
ms.openlocfilehash: 8472526709e563900ac5193b0065111f3ed620fe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978812"
---
# <a name="meetingtimesuggestion-resource-type"></a><span data-ttu-id="f1d6f-103">Tipo de recurso meetingTimeSuggestion</span><span class="sxs-lookup"><span data-stu-id="f1d6f-103">meetingTimeSuggestion resource type</span></span>

<span data-ttu-id="f1d6f-104">Una sugerencia de reunión que incluye información como la hora de la reunión, posibilidad de asistencia, disponibilidad personal y ubicaciones de reuniones disponibles.</span><span class="sxs-lookup"><span data-stu-id="f1d6f-104">A meeting suggestion that includes information like meeting time, attendance likelihood, individual availability, and available meeting locations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f1d6f-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f1d6f-105">JSON representation</span></span>

<span data-ttu-id="f1d6f-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f1d6f-106">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="f1d6f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1d6f-107">Properties</span></span>
| <span data-ttu-id="f1d6f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f1d6f-108">Property</span></span>     | <span data-ttu-id="f1d6f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1d6f-109">Type</span></span>   |<span data-ttu-id="f1d6f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1d6f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f1d6f-111">attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="f1d6f-111">attendeeAvailability</span></span>|<span data-ttu-id="f1d6f-112">[attendeeAvailability](attendeeavailability.md) collection</span><span class="sxs-lookup"><span data-stu-id="f1d6f-112">[attendeeAvailability](attendeeavailability.md) collection</span></span>|<span data-ttu-id="f1d6f-113">Una matriz que muestra el estado de disponibilidad de cada asistente para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="f1d6f-113">An array that shows the availability status of each attendee for this meeting suggestion.</span></span>|
|<span data-ttu-id="f1d6f-114">confidence</span><span class="sxs-lookup"><span data-stu-id="f1d6f-114">confidence</span></span>|<span data-ttu-id="f1d6f-115">Doble</span><span class="sxs-lookup"><span data-stu-id="f1d6f-115">Double</span></span>|<span data-ttu-id="f1d6f-116">Un porcentaje que representa la probabilidad de que asistan todos los convocados.</span><span class="sxs-lookup"><span data-stu-id="f1d6f-116">A percentage that represents the likelhood of all the attendees attending.</span></span>|
|<span data-ttu-id="f1d6f-117">locations</span><span class="sxs-lookup"><span data-stu-id="f1d6f-117">locations</span></span>|<span data-ttu-id="f1d6f-118">Colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="f1d6f-118">[location](location.md) collection</span></span>|<span data-ttu-id="f1d6f-119">Una matriz que especifica el nombre y la ubicación geográfica de cada ubicación de reunión para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="f1d6f-119">An array that specifies the name and geographic location of each meeting location for this meeting suggestion.</span></span>|
|<span data-ttu-id="f1d6f-120">meetingTimeSlot</span><span class="sxs-lookup"><span data-stu-id="f1d6f-120">meetingTimeSlot</span></span>|[<span data-ttu-id="f1d6f-121">timeSlot</span><span class="sxs-lookup"><span data-stu-id="f1d6f-121">timeSlot</span></span>](timeslot.md)|<span data-ttu-id="f1d6f-122">Un período de tiempo sugerido para la reunión.</span><span class="sxs-lookup"><span data-stu-id="f1d6f-122">A time period suggested for the meeting.</span></span>|
|<span data-ttu-id="f1d6f-123">organizerAvailability</span><span class="sxs-lookup"><span data-stu-id="f1d6f-123">organizerAvailability</span></span>|<span data-ttu-id="f1d6f-124">freeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="f1d6f-124">freeBusyStatus</span></span>| <span data-ttu-id="f1d6f-125">Disponibilidad del organizador de la reunión para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="f1d6f-125">Availability of the meeting organizer for this meeting suggestion.</span></span> <span data-ttu-id="f1d6f-126">Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="f1d6f-126">The possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|
|<span data-ttu-id="f1d6f-127">suggestionReason</span><span class="sxs-lookup"><span data-stu-id="f1d6f-127">suggestionReason</span></span>|<span data-ttu-id="f1d6f-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="f1d6f-128">String</span></span>|<span data-ttu-id="f1d6f-129">Razón para proponer hora de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f1d6f-129">Reason for suggesting the meeting time.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
