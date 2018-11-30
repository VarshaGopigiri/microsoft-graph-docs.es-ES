---
title: Tipo de recurso meetingTimeSuggestion
description: 'Una sugerencia de reunión que incluye información como el tiempo de la reunión, la probabilidad de asistencia, individual '
ms.openlocfilehash: 04b7996292decab5330cb17b8aada82d58cf759f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090725"
---
# <a name="meetingtimesuggestion-resource-type"></a><span data-ttu-id="9bffe-103">Tipo de recurso meetingTimeSuggestion</span><span class="sxs-lookup"><span data-stu-id="9bffe-103">meetingTimeSuggestion resource type</span></span>

> <span data-ttu-id="9bffe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9bffe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9bffe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9bffe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9bffe-106">Una sugerencia de reunión que incluye información como la hora de la reunión, posibilidad de asistencia, disponibilidad personal y ubicaciones de reuniones disponibles.</span><span class="sxs-lookup"><span data-stu-id="9bffe-106">A meeting suggestion that includes information like meeting time, attendance likelihood, individual availability, and available meeting locations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9bffe-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9bffe-107">JSON representation</span></span>

<span data-ttu-id="9bffe-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9bffe-108">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="9bffe-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9bffe-109">Properties</span></span>
| <span data-ttu-id="9bffe-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9bffe-110">Property</span></span>     | <span data-ttu-id="9bffe-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bffe-111">Type</span></span>   |<span data-ttu-id="9bffe-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bffe-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9bffe-113">attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="9bffe-113">attendeeAvailability</span></span>|<span data-ttu-id="9bffe-114">[attendeeAvailability](attendeeavailability.md) collection</span><span class="sxs-lookup"><span data-stu-id="9bffe-114">[attendeeAvailability](attendeeavailability.md) collection</span></span>|<span data-ttu-id="9bffe-115">Una matriz que muestra el estado de disponibilidad de cada asistente para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="9bffe-115">An array that shows the availability status of each attendee for this meeting suggestion.</span></span>|
|<span data-ttu-id="9bffe-116">confidence</span><span class="sxs-lookup"><span data-stu-id="9bffe-116">confidence</span></span>|<span data-ttu-id="9bffe-117">Doble</span><span class="sxs-lookup"><span data-stu-id="9bffe-117">Double</span></span>|<span data-ttu-id="9bffe-118">Un porcentaje que representa la probabilidad de que asistan todos los convocados.</span><span class="sxs-lookup"><span data-stu-id="9bffe-118">A percentage that represents the likelhood of all the attendees attending.</span></span>|
|<span data-ttu-id="9bffe-119">locations</span><span class="sxs-lookup"><span data-stu-id="9bffe-119">locations</span></span>|<span data-ttu-id="9bffe-120">Colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="9bffe-120">[location](location.md) collection</span></span>|<span data-ttu-id="9bffe-121">Una matriz que especifica el nombre y la ubicación geográfica de cada ubicación de reunión para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="9bffe-121">An array that specifies the name and geographic location of each meeting location for this meeting suggestion.</span></span>|
|<span data-ttu-id="9bffe-122">meetingTimeSlot</span><span class="sxs-lookup"><span data-stu-id="9bffe-122">meetingTimeSlot</span></span>|[<span data-ttu-id="9bffe-123">timeSlot</span><span class="sxs-lookup"><span data-stu-id="9bffe-123">timeSlot</span></span>](timeslot.md)|<span data-ttu-id="9bffe-124">Un período de tiempo sugerido para la reunión.</span><span class="sxs-lookup"><span data-stu-id="9bffe-124">A time period suggested for the meeting.</span></span>|
|<span data-ttu-id="9bffe-125">organizerAvailability</span><span class="sxs-lookup"><span data-stu-id="9bffe-125">organizerAvailability</span></span>|<span data-ttu-id="9bffe-126">String</span><span class="sxs-lookup"><span data-stu-id="9bffe-126">String</span></span>| <span data-ttu-id="9bffe-p102">Disponibilidad del organizador de la reunión para esta sugerencia de reunión. Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="9bffe-p102">Availability of the meeting organizer for this meeting suggestion. Possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|
|<span data-ttu-id="9bffe-129">suggestionReason</span><span class="sxs-lookup"><span data-stu-id="9bffe-129">suggestionReason</span></span>|<span data-ttu-id="9bffe-130">String</span><span class="sxs-lookup"><span data-stu-id="9bffe-130">String</span></span>|<span data-ttu-id="9bffe-131">Razón para proponer hora de la reunión.</span><span class="sxs-lookup"><span data-stu-id="9bffe-131">Reason for suggesting the meeting time.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->