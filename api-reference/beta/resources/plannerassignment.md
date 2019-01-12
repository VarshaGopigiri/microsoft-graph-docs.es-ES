---
title: Tipo de recurso plannerAssignment
description: El recurso **plannerAssignment** representa la asignación de una tarea a un usuario. Este tipo se usa en el plannerAssignments de tipo abierto.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 5eaeb00abf7446db1085a7c0d0916b0a7b5b2434
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963965"
---
# <a name="plannerassignment-resource-type"></a><span data-ttu-id="7c9df-104">Tipo de recurso plannerAssignment</span><span class="sxs-lookup"><span data-stu-id="7c9df-104">plannerAssignment resource type</span></span>

> <span data-ttu-id="7c9df-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c9df-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c9df-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c9df-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c9df-p103">El recurso **plannerAssignment** representa la asignación de una tarea a un usuario. Este tipo se usa en el tipo abierto [plannerAssignments](plannerassignments.md).</span><span class="sxs-lookup"><span data-stu-id="7c9df-p103">The **plannerAssignment** resource represents the assignment of a task to a user. This type is used in the open type [plannerAssignments](plannerassignments.md).</span></span>


## <a name="properties"></a><span data-ttu-id="7c9df-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c9df-109">Properties</span></span>
| <span data-ttu-id="7c9df-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c9df-110">Property</span></span>     | <span data-ttu-id="7c9df-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c9df-111">Type</span></span>   |<span data-ttu-id="7c9df-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c9df-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7c9df-113">assignedBy</span><span class="sxs-lookup"><span data-stu-id="7c9df-113">assignedBy</span></span>|[<span data-ttu-id="7c9df-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="7c9df-114">identitySet</span></span>](identityset.md)|<span data-ttu-id="7c9df-115">La identidad del usuario que realiza la asignación de la tarea (el asignante).</span><span class="sxs-lookup"><span data-stu-id="7c9df-115">The identity of the user that performed the assignment of the task, i.e. the assignor.</span></span>|
|<span data-ttu-id="7c9df-116">assignedDateTime</span><span class="sxs-lookup"><span data-stu-id="7c9df-116">assignedDateTime</span></span>|<span data-ttu-id="7c9df-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7c9df-117">DateTimeOffset</span></span>|<span data-ttu-id="7c9df-p104">La hora a la que se asignó la tarea. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="7c9df-p104">The time at which the task was assigned. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="7c9df-121">orderHint</span><span class="sxs-lookup"><span data-stu-id="7c9df-121">orderHint</span></span>|<span data-ttu-id="7c9df-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="7c9df-122">String</span></span>|<span data-ttu-id="7c9df-p105">La sugerencia usada para ordenar las personas a las que se ha asignado una tarea. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="7c9df-p105">Hint used to order assignees in a task. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7c9df-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7c9df-125">JSON representation</span></span>
<span data-ttu-id="7c9df-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7c9df-126">Here is a JSON representation of the resource.</span></span>

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
