---
title: Tipo de recurso assignedPlan
description: La propiedad **assignedPlans** de la entidad user y la entidad organization es una colección de **provisionedPlan**.
localization_priority: Normal
ms.openlocfilehash: 82a5ecc5ebb161a213553e2063488c01990a36a0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888824"
---
# <a name="assignedplan-resource-type"></a><span data-ttu-id="5ae8c-103">Tipo de recurso assignedPlan</span><span class="sxs-lookup"><span data-stu-id="5ae8c-103">assignedPlan resource type</span></span>

> <span data-ttu-id="5ae8c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5ae8c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5ae8c-106">La propiedad **assignedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-106">The **assignedPlans** property of both the [user](user.md) entity and the [organization](organization.md) entity is a collection of **assignedPlan**.</span></span>


## <a name="properties"></a><span data-ttu-id="5ae8c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5ae8c-107">Properties</span></span>
| <span data-ttu-id="5ae8c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ae8c-108">Property</span></span>     | <span data-ttu-id="5ae8c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ae8c-109">Type</span></span>   |<span data-ttu-id="5ae8c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ae8c-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5ae8c-111">assignedDateTime</span><span class="sxs-lookup"><span data-stu-id="5ae8c-111">assignedDateTime</span></span>|<span data-ttu-id="5ae8c-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ae8c-112">DateTimeOffset</span></span>|<span data-ttu-id="5ae8c-p102">Fecha y hora en que se asignó el plan; por ejemplo: 2013-01-02T19:32:30Z. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="5ae8c-p102">The date and time at which the plan was assigned; for example: 2013-01-02T19:32:30Z. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="5ae8c-116">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="5ae8c-116">capabilityStatus</span></span>|<span data-ttu-id="5ae8c-117">String</span><span class="sxs-lookup"><span data-stu-id="5ae8c-117">String</span></span>|<span data-ttu-id="5ae8c-118">Por ejemplo, "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="5ae8c-118">For example, “Enabled”.</span></span>|
|<span data-ttu-id="5ae8c-119">service</span><span class="sxs-lookup"><span data-stu-id="5ae8c-119">service</span></span>|<span data-ttu-id="5ae8c-120">String</span><span class="sxs-lookup"><span data-stu-id="5ae8c-120">String</span></span>|<span data-ttu-id="5ae8c-121">Nombre del servicio; por ejemplo, "Exchange".</span><span class="sxs-lookup"><span data-stu-id="5ae8c-121">The name of the service; for example, “Exchange”.</span></span>|
|<span data-ttu-id="5ae8c-122">servicePlanId</span><span class="sxs-lookup"><span data-stu-id="5ae8c-122">servicePlanId</span></span>|<span data-ttu-id="5ae8c-123">Guid</span><span class="sxs-lookup"><span data-stu-id="5ae8c-123">Guid</span></span>|<span data-ttu-id="5ae8c-124">GUID que identifica el plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="5ae8c-124">A GUID that identifies the service plan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5ae8c-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5ae8c-125">JSON representation</span></span>

<span data-ttu-id="5ae8c-126">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5ae8c-126">Here is a JSON representation of the resource</span></span>

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
