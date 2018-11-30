---
title: Tipo de recurso attendeeAvailability
description: El tipo y la disponibilidad de un asistente.
ms.openlocfilehash: ddea2be21f2dd9290637536e2a428e25fc03fcca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083470"
---
# <a name="attendeeavailability-resource-type"></a><span data-ttu-id="60dc6-103">Tipo de recurso attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="60dc6-103">attendeeAvailability resource type</span></span>

> <span data-ttu-id="60dc6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="60dc6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="60dc6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="60dc6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="60dc6-106">El tipo y la disponibilidad de un asistente.</span><span class="sxs-lookup"><span data-stu-id="60dc6-106">The type and availability of an attendee.</span></span>

## <a name="json-representation"></a><span data-ttu-id="60dc6-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="60dc6-107">JSON representation</span></span>

<span data-ttu-id="60dc6-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="60dc6-108">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="60dc6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60dc6-109">Properties</span></span>
| <span data-ttu-id="60dc6-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60dc6-110">Property</span></span>     | <span data-ttu-id="60dc6-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="60dc6-111">Type</span></span>   |<span data-ttu-id="60dc6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="60dc6-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="60dc6-113">asistente</span><span class="sxs-lookup"><span data-stu-id="60dc6-113">attendee</span></span>|[<span data-ttu-id="60dc6-114">AttendeeBase</span><span class="sxs-lookup"><span data-stu-id="60dc6-114">AttendeeBase</span></span>](attendeebase.md)|<span data-ttu-id="60dc6-115">El tipo de asistente, ya sea una persona o un recurso, y en caso de ser una persona, si es obligatorio u opcional.</span><span class="sxs-lookup"><span data-stu-id="60dc6-115">The type of attendee - whether it's a person or a resource, and whether required or optional if it's a person.</span></span>|
|<span data-ttu-id="60dc6-116">disponibilidad</span><span class="sxs-lookup"><span data-stu-id="60dc6-116">availability</span></span>|<span data-ttu-id="60dc6-117">String</span><span class="sxs-lookup"><span data-stu-id="60dc6-117">String</span></span>| <span data-ttu-id="60dc6-p102">El estado de disponibilidad del asistente. Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="60dc6-p102">The availability status of the attendee. Possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeAvailability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->