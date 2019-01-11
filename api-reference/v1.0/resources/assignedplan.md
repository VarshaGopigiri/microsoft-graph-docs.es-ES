---
title: Tipo de recurso assignedPlan
description: La propiedad **assignedPlans** de la entidad user y la entidad organization es una colección de **provisionedPlan**.
localization_priority: Normal
ms.openlocfilehash: d1f3df6a88ab688206d26db6fc0afe1e1d4a4f60
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853000"
---
# <a name="assignedplan-resource-type"></a><span data-ttu-id="1e83a-103">Tipo de recurso assignedPlan</span><span class="sxs-lookup"><span data-stu-id="1e83a-103">assignedPlan resource type</span></span>

<span data-ttu-id="1e83a-104">La propiedad **assignedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.</span><span class="sxs-lookup"><span data-stu-id="1e83a-104">The **assignedPlans** property of both the [user](user.md) entity and the [organization](organization.md) entity is a collection of **assignedPlan**.</span></span>


## <a name="properties"></a><span data-ttu-id="1e83a-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e83a-105">Properties</span></span>
| <span data-ttu-id="1e83a-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e83a-106">Property</span></span>     | <span data-ttu-id="1e83a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e83a-107">Type</span></span>   |<span data-ttu-id="1e83a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e83a-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1e83a-109">assignedDateTime</span><span class="sxs-lookup"><span data-stu-id="1e83a-109">assignedDateTime</span></span>|<span data-ttu-id="1e83a-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1e83a-110">DateTimeOffset</span></span>|<span data-ttu-id="1e83a-p101">Fecha y hora en que se asignó el plan; por ejemplo: 2013-01-02T19:32:30Z. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="1e83a-p101">The date and time at which the plan was assigned; for example: 2013-01-02T19:32:30Z. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="1e83a-114">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="1e83a-114">capabilityStatus</span></span>|<span data-ttu-id="1e83a-115">String</span><span class="sxs-lookup"><span data-stu-id="1e83a-115">String</span></span>|<span data-ttu-id="1e83a-116">Por ejemplo, "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="1e83a-116">For example, “Enabled”.</span></span>|
|<span data-ttu-id="1e83a-117">service</span><span class="sxs-lookup"><span data-stu-id="1e83a-117">service</span></span>|<span data-ttu-id="1e83a-118">String</span><span class="sxs-lookup"><span data-stu-id="1e83a-118">String</span></span>|<span data-ttu-id="1e83a-119">Nombre del servicio; por ejemplo, "Exchange".</span><span class="sxs-lookup"><span data-stu-id="1e83a-119">The name of the service; for example, “Exchange”.</span></span>|
|<span data-ttu-id="1e83a-120">servicePlanId</span><span class="sxs-lookup"><span data-stu-id="1e83a-120">servicePlanId</span></span>|<span data-ttu-id="1e83a-121">Guid</span><span class="sxs-lookup"><span data-stu-id="1e83a-121">Guid</span></span>|<span data-ttu-id="1e83a-122">GUID que identifica el plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="1e83a-122">A GUID that identifies the service plan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1e83a-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1e83a-123">JSON representation</span></span>

<span data-ttu-id="1e83a-124">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1e83a-124">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.assignedPlan"
}-->

```json
{
  "assignedDateTime": "String (timestamp)",
  "capabilityStatus": "string",
  "service": "string",
  "servicePlanId": "guid"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "assignedPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
