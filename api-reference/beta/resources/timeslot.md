---
title: Tipo de recurso timeSlot
description: Un periodo de tiempo.
localization_priority: Normal
ms.openlocfilehash: 1f383a7feafbb3816ef838d8f0667eebdd42443f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877934"
---
# <a name="timeslot-resource-type"></a><span data-ttu-id="fe2ea-103">Tipo de recurso timeSlot</span><span class="sxs-lookup"><span data-stu-id="fe2ea-103">timeSlot resource type</span></span>

> <span data-ttu-id="fe2ea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fe2ea-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fe2ea-106">Un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-106">A time period.</span></span>

## <a name="json-representation"></a><span data-ttu-id="fe2ea-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fe2ea-107">JSON representation</span></span>

<span data-ttu-id="fe2ea-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fe2ea-108">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="fe2ea-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe2ea-109">Properties</span></span>
| <span data-ttu-id="fe2ea-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fe2ea-110">Property</span></span>     | <span data-ttu-id="fe2ea-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe2ea-111">Type</span></span>   |<span data-ttu-id="fe2ea-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe2ea-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fe2ea-113">finalización</span><span class="sxs-lookup"><span data-stu-id="fe2ea-113">end</span></span>|[<span data-ttu-id="fe2ea-114">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="fe2ea-114">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="fe2ea-115">Comienza un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-115">The time a period begins.</span></span>|
|<span data-ttu-id="fe2ea-116">inicio</span><span class="sxs-lookup"><span data-stu-id="fe2ea-116">start</span></span>|[<span data-ttu-id="fe2ea-117">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="fe2ea-117">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="fe2ea-118">Finaliza un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-118">The time the period ends.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeSlot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
