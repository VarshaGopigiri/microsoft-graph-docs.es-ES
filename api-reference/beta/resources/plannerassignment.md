---
title: Tipo de recurso plannerAssignment
description: El recurso **plannerAssignment** representa la asignación de una tarea a un usuario. Este tipo se usa en el plannerAssignments de tipo abierto.
ms.openlocfilehash: 1efe7c3f2d3229bcce1d2c35e375cc636dadc51f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089250"
---
# <a name="plannerassignment-resource-type"></a><span data-ttu-id="4c09a-104">Tipo de recurso plannerAssignment</span><span class="sxs-lookup"><span data-stu-id="4c09a-104">plannerAssignment resource type</span></span>

> <span data-ttu-id="4c09a-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4c09a-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4c09a-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4c09a-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4c09a-p103">El recurso **plannerAssignment** representa la asignación de una tarea a un usuario. Este tipo se usa en el tipo abierto [plannerAssignments](plannerassignments.md).</span><span class="sxs-lookup"><span data-stu-id="4c09a-p103">The **plannerAssignment** resource represents the assignment of a task to a user. This type is used in the open type [plannerAssignments](plannerassignments.md).</span></span>


## <a name="properties"></a><span data-ttu-id="4c09a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c09a-109">Properties</span></span>
| <span data-ttu-id="4c09a-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c09a-110">Property</span></span>     | <span data-ttu-id="4c09a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c09a-111">Type</span></span>   |<span data-ttu-id="4c09a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c09a-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4c09a-113">assignedBy</span><span class="sxs-lookup"><span data-stu-id="4c09a-113">assignedBy</span></span>|[<span data-ttu-id="4c09a-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="4c09a-114">identitySet</span></span>](identityset.md)|<span data-ttu-id="4c09a-115">La identidad del usuario que realiza la asignación de la tarea (el asignante).</span><span class="sxs-lookup"><span data-stu-id="4c09a-115">The identity of the user that performed the assignment of the task, i.e. the assignor.</span></span>|
|<span data-ttu-id="4c09a-116">assignedDateTime</span><span class="sxs-lookup"><span data-stu-id="4c09a-116">assignedDateTime</span></span>|<span data-ttu-id="4c09a-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4c09a-117">DateTimeOffset</span></span>|<span data-ttu-id="4c09a-p104">La hora a la que se asignó la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="4c09a-p104">The time at which the task was assigned. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="4c09a-121">orderHint</span><span class="sxs-lookup"><span data-stu-id="4c09a-121">orderHint</span></span>|<span data-ttu-id="4c09a-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="4c09a-122">String</span></span>|<span data-ttu-id="4c09a-p105">La sugerencia usada para ordenar las personas a las que se ha asignado una tarea. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="4c09a-p105">Hint used to order assignees in a task. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4c09a-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4c09a-125">JSON representation</span></span>
<span data-ttu-id="4c09a-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4c09a-126">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAssignment"
}-->

```json
{
  "assignedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "assignedDateTime": "String (timestamp)",
  "orderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->