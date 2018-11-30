---
title: Tipo de recurso timeSlot
description: Un periodo de tiempo.
ms.openlocfilehash: 43ce20e006f2a6946877a4ffd2bf730d45d6d1c3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030608"
---
# <a name="timeslot-resource-type"></a><span data-ttu-id="f4edc-103">Tipo de recurso timeSlot</span><span class="sxs-lookup"><span data-stu-id="f4edc-103">timeSlot resource type</span></span>

<span data-ttu-id="f4edc-104">Un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f4edc-104">A time period.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f4edc-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f4edc-105">JSON representation</span></span>

<span data-ttu-id="f4edc-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f4edc-106">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="f4edc-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4edc-107">Properties</span></span>
| <span data-ttu-id="f4edc-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4edc-108">Property</span></span>     | <span data-ttu-id="f4edc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4edc-109">Type</span></span>   |<span data-ttu-id="f4edc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4edc-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f4edc-111">finalización</span><span class="sxs-lookup"><span data-stu-id="f4edc-111">end</span></span>|[<span data-ttu-id="f4edc-112">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="f4edc-112">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="f4edc-113">Comienza un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f4edc-113">The time a period begins.</span></span>|
|<span data-ttu-id="f4edc-114">inicio</span><span class="sxs-lookup"><span data-stu-id="f4edc-114">start</span></span>|[<span data-ttu-id="f4edc-115">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="f4edc-115">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="f4edc-116">Finaliza un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f4edc-116">The time the period ends.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeSlot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->