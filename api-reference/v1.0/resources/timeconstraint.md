---
title: Tipo de recurso timeConstraint
description: Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.
ms.openlocfilehash: 82ab18eb09201236f3227c7dd0660519092a3133
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029329"
---
# <a name="timeconstraint-resource-type"></a><span data-ttu-id="ffe80-103">Tipo de recurso timeConstraint</span><span class="sxs-lookup"><span data-stu-id="ffe80-103">timeConstraint resource type</span></span>

<span data-ttu-id="ffe80-104">Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.</span><span class="sxs-lookup"><span data-stu-id="ffe80-104">Restricts meeting time suggestions to certain hours and days of the week according to the specified nature of activity and open time slots.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ffe80-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ffe80-105">JSON representation</span></span>

<span data-ttu-id="ffe80-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ffe80-106">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="ffe80-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffe80-107">Properties</span></span>
| <span data-ttu-id="ffe80-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ffe80-108">Property</span></span>     | <span data-ttu-id="ffe80-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffe80-109">Type</span></span>   |<span data-ttu-id="ffe80-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffe80-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ffe80-111">activityDomain</span><span class="sxs-lookup"><span data-stu-id="ffe80-111">activityDomain</span></span>|<span data-ttu-id="ffe80-112">activityDomain</span><span class="sxs-lookup"><span data-stu-id="ffe80-112">activityDomain</span></span>|<span data-ttu-id="ffe80-113">La naturaleza de la actividad, de forma opcional.</span><span class="sxs-lookup"><span data-stu-id="ffe80-113">The nature of the activity, optional.</span></span> <span data-ttu-id="ffe80-114">Los valores posibles son: `work`, `personal`, `unrestricted`, o `unknown`.</span><span class="sxs-lookup"><span data-stu-id="ffe80-114">The possible values are: `work`, `personal`, `unrestricted`, or `unknown`.</span></span>|
|<span data-ttu-id="ffe80-115">ranuras de intervalo de tiempo</span><span class="sxs-lookup"><span data-stu-id="ffe80-115">timeslots</span></span>|<span data-ttu-id="ffe80-116">Colección[timeSlot](timeslot.md)</span><span class="sxs-lookup"><span data-stu-id="ffe80-116">[timeSlot](timeslot.md) collection</span></span>|<span data-ttu-id="ffe80-117">Matriz de periodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="ffe80-117">An array of time periods.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
