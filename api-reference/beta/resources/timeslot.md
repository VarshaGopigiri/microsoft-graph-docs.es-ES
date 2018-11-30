---
title: Tipo de recurso timeSlot
description: Un periodo de tiempo.
ms.openlocfilehash: c1df6ea458bf6742dc20149e62d9760a8a6510e2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089807"
---
# <a name="timeslot-resource-type"></a><span data-ttu-id="6fb8b-103">Tipo de recurso timeSlot</span><span class="sxs-lookup"><span data-stu-id="6fb8b-103">timeSlot resource type</span></span>

> <span data-ttu-id="6fb8b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6fb8b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6fb8b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6fb8b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6fb8b-106">Un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6fb8b-106">A time period.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6fb8b-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6fb8b-107">JSON representation</span></span>

<span data-ttu-id="6fb8b-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6fb8b-108">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeSlot"
}-->

```json
{
  "end": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "start": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```
## <a name="properties"></a><span data-ttu-id="6fb8b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6fb8b-109">Properties</span></span>
| <span data-ttu-id="6fb8b-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6fb8b-110">Property</span></span>     | <span data-ttu-id="6fb8b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fb8b-111">Type</span></span>   |<span data-ttu-id="6fb8b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fb8b-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6fb8b-113">finalización</span><span class="sxs-lookup"><span data-stu-id="6fb8b-113">end</span></span>|[<span data-ttu-id="6fb8b-114">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="6fb8b-114">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="6fb8b-115">Comienza un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6fb8b-115">The time a period begins.</span></span>|
|<span data-ttu-id="6fb8b-116">inicio</span><span class="sxs-lookup"><span data-stu-id="6fb8b-116">start</span></span>|[<span data-ttu-id="6fb8b-117">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="6fb8b-117">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="6fb8b-118">Finaliza un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6fb8b-118">The time the period ends.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeSlot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->