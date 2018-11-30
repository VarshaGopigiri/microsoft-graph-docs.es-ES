---
title: tipo de recurso plannerRecentPlanReference
description: 'El recurso **plannerRecentPlanReference** escriba representa una referencia a un plannerPlan que recientemente se ha visto por un usuario. '
ms.openlocfilehash: ac774ffbf7ebdfe45211cf50c2ce065921de30f1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083866"
---
# <a name="plannerrecentplanreference-resource-type"></a><span data-ttu-id="0a653-103">tipo de recurso plannerRecentPlanReference</span><span class="sxs-lookup"><span data-stu-id="0a653-103">plannerRecentPlanReference resource type</span></span>

> <span data-ttu-id="0a653-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0a653-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0a653-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0a653-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0a653-106">El recurso **plannerRecentPlanReference** escriba representa una referencia a un [plannerPlan](plannerplan.md) que recientemente se ha visto por un usuario.</span><span class="sxs-lookup"><span data-stu-id="0a653-106">The **plannerRecentPlanReference** resource type repesents a reference to a [plannerPlan](plannerplan.md) that has recently been viewed by a user.</span></span> <span data-ttu-id="0a653-107">El **plannerRecentPlanReferences** para un usuario se mantienen explícitamente por aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0a653-107">The **plannerRecentPlanReferences** for a user are explicitly maintained by apps.</span></span> <span data-ttu-id="0a653-108">Cualquier aplicación que implementa la característica de planes recientes debe registrar cuando el usuario vio por última vez un plan y actualización **plannerRecentPlanReference** entradas en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="0a653-108">Any app that implements the recent plans feature should record when the user last viewed a plan, and update **plannerRecentPlanReference** entries accordingly.</span></span>
<span data-ttu-id="0a653-109">Aplicaciones deben tener en cuenta que las entradas de **plannerRecentPlanReference** pueden hacer referencia a **plannerPlans** que se eliminan, que ya no se puede obtener acceso el usuario, o que se han actualizado con un título diferente.</span><span class="sxs-lookup"><span data-stu-id="0a653-109">Apps should note that **plannerRecentPlanReference** entries can reference **plannerPlans** that are deleted, that the user can no longer access, or that have been updated with a different title.</span></span>
<span data-ttu-id="0a653-110">Se recomienda que aplicaciones notificar a los usuarios cuando hay discrepancias y mantener actualizadas las entradas.</span><span class="sxs-lookup"><span data-stu-id="0a653-110">We recommend that apps notify users when there are discrepancies and keep the entries up to date.</span></span>

## <a name="properties"></a><span data-ttu-id="0a653-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a653-111">Properties</span></span>
| <span data-ttu-id="0a653-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0a653-112">Property</span></span>     | <span data-ttu-id="0a653-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a653-113">Type</span></span>   |<span data-ttu-id="0a653-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a653-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0a653-115">lastAccessedDateTime</span><span class="sxs-lookup"><span data-stu-id="0a653-115">lastAccessedDateTime</span></span>|<span data-ttu-id="0a653-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a653-116">DateTimeOffset</span></span>|<span data-ttu-id="0a653-117">La fecha y la hora que el plan fue la última vez por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0a653-117">The date and time the plan was last viewed by the user.</span></span> <span data-ttu-id="0a653-118">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="0a653-118">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="0a653-119">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="0a653-119">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="0a653-120">planTitle</span><span class="sxs-lookup"><span data-stu-id="0a653-120">planTitle</span></span>|<span data-ttu-id="0a653-121">String</span><span class="sxs-lookup"><span data-stu-id="0a653-121">String</span></span>|<span data-ttu-id="0a653-122">El título del plan en el momento de ve el usuario lo.</span><span class="sxs-lookup"><span data-stu-id="0a653-122">The title of the plan at the time the user viewed it.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0a653-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0a653-123">JSON representation</span></span>

<span data-ttu-id="0a653-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0a653-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerRecentPlanReference"
}-->

```json
{
  "lastAccessedDateTime": "String (timestamp)",
  "planTitle": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerRecentPlanReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
