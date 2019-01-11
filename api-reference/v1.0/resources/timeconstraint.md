---
title: Tipo de recurso timeConstraint
description: Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.
localization_priority: Normal
ms.openlocfilehash: b6e239abbd0d9f7b4f83df4a60625a2f88131476
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815095"
---
# <a name="timeconstraint-resource-type"></a><span data-ttu-id="e752b-103">Tipo de recurso timeConstraint</span><span class="sxs-lookup"><span data-stu-id="e752b-103">timeConstraint resource type</span></span>

<span data-ttu-id="e752b-104">Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.</span><span class="sxs-lookup"><span data-stu-id="e752b-104">Restricts meeting time suggestions to certain hours and days of the week according to the specified nature of activity and open time slots.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e752b-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e752b-105">JSON representation</span></span>

<span data-ttu-id="e752b-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e752b-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeConstraint"
}-->

```json
{
  "activityDomain": "String",
  "timeslots": [{"@odata.type": "microsoft.graph.timeSlot"}]
}

```
## <a name="properties"></a><span data-ttu-id="e752b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e752b-107">Properties</span></span>
| <span data-ttu-id="e752b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e752b-108">Property</span></span>     | <span data-ttu-id="e752b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e752b-109">Type</span></span>   |<span data-ttu-id="e752b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e752b-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e752b-111">activityDomain</span><span class="sxs-lookup"><span data-stu-id="e752b-111">activityDomain</span></span>|<span data-ttu-id="e752b-112">activityDomain</span><span class="sxs-lookup"><span data-stu-id="e752b-112">activityDomain</span></span>|<span data-ttu-id="e752b-113">La naturaleza de la actividad, de forma opcional.</span><span class="sxs-lookup"><span data-stu-id="e752b-113">The nature of the activity, optional.</span></span> <span data-ttu-id="e752b-114">Los valores posibles son: `work`, `personal`, `unrestricted`, o `unknown`.</span><span class="sxs-lookup"><span data-stu-id="e752b-114">The possible values are: `work`, `personal`, `unrestricted`, or `unknown`.</span></span>|
|<span data-ttu-id="e752b-115">ranuras de intervalo de tiempo</span><span class="sxs-lookup"><span data-stu-id="e752b-115">timeslots</span></span>|<span data-ttu-id="e752b-116">Colección[timeSlot](timeslot.md)</span><span class="sxs-lookup"><span data-stu-id="e752b-116">[timeSlot](timeslot.md) collection</span></span>|<span data-ttu-id="e752b-117">Matriz de periodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e752b-117">An array of time periods.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
