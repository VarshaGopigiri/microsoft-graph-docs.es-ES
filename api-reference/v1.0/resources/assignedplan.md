---
title: Tipo de recurso assignedPlan
description: La propiedad **assignedPlans** de la entidad user y la entidad organization es una colección de **provisionedPlan**.
ms.openlocfilehash: 306c485b31189e7693075735ceda0812d3259251
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029594"
---
# <a name="assignedplan-resource-type"></a><span data-ttu-id="291a9-103">Tipo de recurso assignedPlan</span><span class="sxs-lookup"><span data-stu-id="291a9-103">assignedPlan resource type</span></span>

<span data-ttu-id="291a9-104">La propiedad **assignedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.</span><span class="sxs-lookup"><span data-stu-id="291a9-104">The **assignedPlans** property of both the [user](user.md) entity and the [organization](organization.md) entity is a collection of **assignedPlan**.</span></span>


## <a name="properties"></a><span data-ttu-id="291a9-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="291a9-105">Properties</span></span>
| <span data-ttu-id="291a9-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="291a9-106">Property</span></span>     | <span data-ttu-id="291a9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="291a9-107">Type</span></span>   |<span data-ttu-id="291a9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="291a9-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="291a9-109">assignedDateTime</span><span class="sxs-lookup"><span data-stu-id="291a9-109">assignedDateTime</span></span>|<span data-ttu-id="291a9-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="291a9-110">DateTimeOffset</span></span>|<span data-ttu-id="291a9-p101">Fecha y hora en que se asignó el plan; por ejemplo: 2013-01-02T19:32:30Z. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="291a9-p101">The date and time at which the plan was assigned; for example: 2013-01-02T19:32:30Z. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="291a9-114">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="291a9-114">capabilityStatus</span></span>|<span data-ttu-id="291a9-115">String</span><span class="sxs-lookup"><span data-stu-id="291a9-115">String</span></span>|<span data-ttu-id="291a9-116">Por ejemplo, "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="291a9-116">For example, “Enabled”.</span></span>|
|<span data-ttu-id="291a9-117">service</span><span class="sxs-lookup"><span data-stu-id="291a9-117">service</span></span>|<span data-ttu-id="291a9-118">String</span><span class="sxs-lookup"><span data-stu-id="291a9-118">String</span></span>|<span data-ttu-id="291a9-119">Nombre del servicio; por ejemplo, "Exchange".</span><span class="sxs-lookup"><span data-stu-id="291a9-119">The name of the service; for example, “Exchange”.</span></span>|
|<span data-ttu-id="291a9-120">servicePlanId</span><span class="sxs-lookup"><span data-stu-id="291a9-120">servicePlanId</span></span>|<span data-ttu-id="291a9-121">Guid</span><span class="sxs-lookup"><span data-stu-id="291a9-121">Guid</span></span>|<span data-ttu-id="291a9-122">GUID que identifica el plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="291a9-122">A GUID that identifies the service plan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="291a9-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="291a9-123">JSON representation</span></span>

<span data-ttu-id="291a9-124">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="291a9-124">Here is a JSON representation of the resource</span></span>

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
