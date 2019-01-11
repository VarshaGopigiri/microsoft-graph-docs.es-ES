---
title: Tipo de recurso timeSlot
description: Un periodo de tiempo.
localization_priority: Normal
ms.openlocfilehash: e01b8d0f34a21eb18bc92e8bcc4e1b8365541d5c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860567"
---
# <a name="timeslot-resource-type"></a><span data-ttu-id="e5abd-103">Tipo de recurso timeSlot</span><span class="sxs-lookup"><span data-stu-id="e5abd-103">timeSlot resource type</span></span>

<span data-ttu-id="e5abd-104">Un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e5abd-104">A time period.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e5abd-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e5abd-105">JSON representation</span></span>

<span data-ttu-id="e5abd-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e5abd-106">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="e5abd-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5abd-107">Properties</span></span>
| <span data-ttu-id="e5abd-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5abd-108">Property</span></span>     | <span data-ttu-id="e5abd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5abd-109">Type</span></span>   |<span data-ttu-id="e5abd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5abd-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e5abd-111">finalización</span><span class="sxs-lookup"><span data-stu-id="e5abd-111">end</span></span>|[<span data-ttu-id="e5abd-112">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="e5abd-112">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="e5abd-113">Comienza un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e5abd-113">The time a period begins.</span></span>|
|<span data-ttu-id="e5abd-114">inicio</span><span class="sxs-lookup"><span data-stu-id="e5abd-114">start</span></span>|[<span data-ttu-id="e5abd-115">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="e5abd-115">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="e5abd-116">Finaliza un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e5abd-116">The time the period ends.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeSlot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
