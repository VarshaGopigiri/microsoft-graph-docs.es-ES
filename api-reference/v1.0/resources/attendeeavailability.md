---
title: Tipo de recurso attendeeAvailability
description: El tipo y la disponibilidad de un asistente.
localization_priority: Normal
ms.openlocfilehash: a6dee994fc5eb3786fc1a432adcb9333bdb56ec8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834751"
---
# <a name="attendeeavailability-resource-type"></a><span data-ttu-id="67f30-103">Tipo de recurso attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="67f30-103">attendeeAvailability resource type</span></span>

<span data-ttu-id="67f30-104">El tipo y la disponibilidad de un asistente.</span><span class="sxs-lookup"><span data-stu-id="67f30-104">The type and availability of an attendee.</span></span>

## <a name="json-representation"></a><span data-ttu-id="67f30-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="67f30-105">JSON representation</span></span>

<span data-ttu-id="67f30-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="67f30-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendeeAvailability"
}-->

```json
{
  "attendee": {"@odata.type": "microsoft.graph.attendeeBase"},
  "availability": "String"
}

```
## <a name="properties"></a><span data-ttu-id="67f30-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67f30-107">Properties</span></span>
| <span data-ttu-id="67f30-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67f30-108">Property</span></span>     | <span data-ttu-id="67f30-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="67f30-109">Type</span></span>   |<span data-ttu-id="67f30-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="67f30-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="67f30-111">asistente</span><span class="sxs-lookup"><span data-stu-id="67f30-111">attendee</span></span>|[<span data-ttu-id="67f30-112">AttendeeBase</span><span class="sxs-lookup"><span data-stu-id="67f30-112">AttendeeBase</span></span>](attendeebase.md)|<span data-ttu-id="67f30-113">El tipo de asistente, ya sea una persona o un recurso, y en caso de ser una persona, si es obligatorio u opcional.</span><span class="sxs-lookup"><span data-stu-id="67f30-113">The type of attendee - whether it's a person or a resource, and whether required or optional if it's a person.</span></span>|
|<span data-ttu-id="67f30-114">disponibilidad</span><span class="sxs-lookup"><span data-stu-id="67f30-114">availability</span></span>|<span data-ttu-id="67f30-115">freeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="67f30-115">freeBusyStatus</span></span>| <span data-ttu-id="67f30-116">El estado de disponibilidad del asistente.</span><span class="sxs-lookup"><span data-stu-id="67f30-116">The availability status of the attendee.</span></span> <span data-ttu-id="67f30-117">Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="67f30-117">The possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeAvailability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
