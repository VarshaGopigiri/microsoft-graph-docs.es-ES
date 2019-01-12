---
title: tipo de recurso plannerPlanContext
description: El recurso **plannerPlanContext** representa la relación de una plannerPlan para una experiencia de usuario fuera del organizador. Planes en el organizador pueden se exponen en otras experiencias, como Microsoft Teams, realizar un seguimiento de trabajo en el contexto de esa experiencia.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: e118e32ea74332f0d8d0f958f7c55cd9980acb8f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962894"
---
# <a name="plannerplancontext-resource-type"></a><span data-ttu-id="7ce12-104">tipo de recurso plannerPlanContext</span><span class="sxs-lookup"><span data-stu-id="7ce12-104">plannerPlanContext resource type</span></span>

> <span data-ttu-id="7ce12-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7ce12-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7ce12-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7ce12-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7ce12-107">El recurso **plannerPlanContext** representa la relación de una [plannerPlan](plannerplan.md) para una experiencia de usuario fuera del organizador.</span><span class="sxs-lookup"><span data-stu-id="7ce12-107">The **plannerPlanContext** resource represents the relationship of a [plannerPlan](plannerplan.md) to a user experience outside of Planner.</span></span> <span data-ttu-id="7ce12-108">Planes en el organizador pueden se exponen en otras experiencias, como Microsoft Teams, realizar un seguimiento de trabajo en el contexto de esa experiencia.</span><span class="sxs-lookup"><span data-stu-id="7ce12-108">Plans in Planner can be surfaced in other experiences, such as Microsoft Teams, to track work in the context of that experience.</span></span>
<span data-ttu-id="7ce12-109">La experiencia de que la entrada de **plannerPlanContext** reresents se puede identificar en función de la propiedad **ownerAppId** :</span><span class="sxs-lookup"><span data-stu-id="7ce12-109">The experience the **plannerPlanContext** entry reresents can be identified based on the **ownerAppId** property:</span></span>
 - <span data-ttu-id="7ce12-110">5e3ce6c0-2b1f-4285-8d4b-75ee78787346: la entrada de contexto pertenece a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7ce12-110">5e3ce6c0-2b1f-4285-8d4b-75ee78787346 : The context entry belongs to Microsoft Teams.</span></span>
 - <span data-ttu-id="7ce12-111">00000003-0000-0ff1-CE00-000000000000: la entrada de contexto pertenece a SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7ce12-111">00000003-0000-0ff1-ce00-000000000000 : The context entry belongs to SharePoint.</span></span>

## <a name="properties"></a><span data-ttu-id="7ce12-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ce12-112">Properties</span></span>
| <span data-ttu-id="7ce12-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ce12-113">Property</span></span>     | <span data-ttu-id="7ce12-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ce12-114">Type</span></span>   |<span data-ttu-id="7ce12-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ce12-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7ce12-116">associationType</span><span class="sxs-lookup"><span data-stu-id="7ce12-116">associationType</span></span>|<span data-ttu-id="7ce12-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ce12-117">String</span></span>|<span data-ttu-id="7ce12-118">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="7ce12-118">Nullable.</span></span> <span data-ttu-id="7ce12-119">Un tipo definido por la aplicación de la asociación entre el [plannerPlan](plannerplan.md) y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ce12-119">An app-defined type of association between the [plannerPlan](plannerplan.md) and the app.</span></span> <span data-ttu-id="7ce12-120">La aplicación puede utilizar esta información para realizar un seguimiento de los distintos tipos de relaciones en el mismo [plannerPlan](plannerplan.md).</span><span class="sxs-lookup"><span data-stu-id="7ce12-120">The app can use this information to track different kinds of relationships to the same [plannerPlan](plannerplan.md).</span></span>|
|<span data-ttu-id="7ce12-121">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7ce12-121">createdDateTime</span></span>|<span data-ttu-id="7ce12-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7ce12-122">DateTimeOffset</span></span>|<span data-ttu-id="7ce12-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7ce12-123">Read-only.</span></span> <span data-ttu-id="7ce12-124">La fecha y la hora cuando se creó el **plannerPlanContext** .</span><span class="sxs-lookup"><span data-stu-id="7ce12-124">The date and time when the **plannerPlanContext** was created.</span></span> <span data-ttu-id="7ce12-125">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="7ce12-125">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="7ce12-126">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="7ce12-126">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="7ce12-127">displayNameSegments</span><span class="sxs-lookup"><span data-stu-id="7ce12-127">displayNameSegments</span></span>|<span data-ttu-id="7ce12-128">Colección String</span><span class="sxs-lookup"><span data-stu-id="7ce12-128">String collection</span></span>|<span data-ttu-id="7ce12-129">Los segmentos del nombre de la experiencia del externo.</span><span class="sxs-lookup"><span data-stu-id="7ce12-129">The segments of the name of the external experience.</span></span> <span data-ttu-id="7ce12-130">Segmentos representan una estructura jerárquica que permite que otras aplicaciones mostrar la relación.</span><span class="sxs-lookup"><span data-stu-id="7ce12-130">Segments represent a hierarchical structure that allows other apps to display the relationship.</span></span>|
|<span data-ttu-id="7ce12-131">ownerAppId</span><span class="sxs-lookup"><span data-stu-id="7ce12-131">ownerAppId</span></span>|<span data-ttu-id="7ce12-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ce12-132">String</span></span>|<span data-ttu-id="7ce12-133">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7ce12-133">Read-only.</span></span> <span data-ttu-id="7ce12-134">Identificador de la aplicación que creó el **plannerPlanContext**.</span><span class="sxs-lookup"><span data-stu-id="7ce12-134">ID of the app that created the **plannerPlanContext**.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7ce12-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7ce12-135">JSON representation</span></span>

<span data-ttu-id="7ce12-136">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7ce12-136">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanContext"
}-->

```json
{
  "associationType": "Board",
  "createdDateTime": "2015-10-14T00:57:28.4698344Z",
  "displayNameSegments": [
    "Finance Team",
    "Budget Plans"
  ],
  "ownerAppId": "5e3ce6c0-2b1f-4285-8d4b-75ee78787346"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanContext resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
