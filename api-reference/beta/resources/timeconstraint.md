---
title: Tipo de recurso timeConstraint
description: Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.
ms.openlocfilehash: 092133d34e12fe5c06bfd8a76e8a33afb33892f3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084368"
---
# <a name="timeconstraint-resource-type"></a><span data-ttu-id="4656d-103">Tipo de recurso timeConstraint</span><span class="sxs-lookup"><span data-stu-id="4656d-103">timeConstraint resource type</span></span>

> <span data-ttu-id="4656d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4656d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4656d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4656d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4656d-106">Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.</span><span class="sxs-lookup"><span data-stu-id="4656d-106">Restricts meeting time suggestions to certain hours and days of the week according to the specified nature of activity and open time slots.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4656d-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4656d-107">JSON representation</span></span>

<span data-ttu-id="4656d-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4656d-108">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeconstraint"
}-->

```json
{
  "activityDomain": "String",
  "timeslots": [{"@odata.type": "microsoft.graph.timeSlot"}]
}

```
## <a name="properties"></a><span data-ttu-id="4656d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4656d-109">Properties</span></span>
| <span data-ttu-id="4656d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4656d-110">Property</span></span>     | <span data-ttu-id="4656d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="4656d-111">Type</span></span>   |<span data-ttu-id="4656d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4656d-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4656d-113">activityDomain</span><span class="sxs-lookup"><span data-stu-id="4656d-113">activityDomain</span></span>|<span data-ttu-id="4656d-114">String</span><span class="sxs-lookup"><span data-stu-id="4656d-114">String</span></span>|<span data-ttu-id="4656d-p102">La naturaleza de la actividad, opcional. Los valores posibles son: `work`, `personal`, `unrestricted` o `unknown`.</span><span class="sxs-lookup"><span data-stu-id="4656d-p102">The nature of the activity, optional. Possible values are: `work`, `personal`, `unrestricted`, or `unknown`.</span></span>|
|<span data-ttu-id="4656d-117">ranuras de intervalo de tiempo</span><span class="sxs-lookup"><span data-stu-id="4656d-117">timeslots</span></span>|<span data-ttu-id="4656d-118">Colección[timeSlot](timeslot.md)</span><span class="sxs-lookup"><span data-stu-id="4656d-118">[timeSlot](timeslot.md) collection</span></span>|<span data-ttu-id="4656d-119">Matriz de periodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4656d-119">An array of time periods.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->