---
title: Tipo de recurso plannerProgressTaskBoardTaskFormat
description: El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada task tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.
ms.openlocfilehash: 8ff6f536920bafb8734f63ef9fe9b72f8c2b1acb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085328"
---
# <a name="plannerprogresstaskboardtaskformat-resource-type"></a><span data-ttu-id="d9b3d-104">Tipo de recurso plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="d9b3d-104">plannerProgressTaskBoardTaskFormat resource type</span></span>

> <span data-ttu-id="d9b3d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9b3d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d9b3d-p103">El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada [task](plannertask.md) tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-p103">The **plannerProgressTaskBoardTaskFormat** resource represents the information used to render a task correctly in the Progress view of the Task Board (a view organized by the state of the PercentComplete field on the task object, with columns for Not Started, In Progress and Complete). Each [task](plannertask.md) will have one **plannerProgressTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="d9b3d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9b3d-109">Methods</span></span>

| <span data-ttu-id="d9b3d-110">Método</span><span class="sxs-lookup"><span data-stu-id="d9b3d-110">Method</span></span>           | <span data-ttu-id="d9b3d-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9b3d-111">Return Type</span></span>    |<span data-ttu-id="d9b3d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9b3d-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d9b3d-113">Obtener plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="d9b3d-113">Get plannerProgressTaskBoardTaskFormat</span></span>](../api/plannerprogresstaskboardtaskformat-get.md) | [<span data-ttu-id="d9b3d-114">plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="d9b3d-114">plannerProgressTaskBoardTaskFormat</span></span>](plannerprogresstaskboardtaskformat.md) |<span data-ttu-id="d9b3d-115">Leer las propiedades y las relaciones del objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-115">Read properties and relationships of **plannerProgressTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="d9b3d-116">Update</span><span class="sxs-lookup"><span data-stu-id="d9b3d-116">Update</span></span>](../api/plannerprogresstaskboardtaskformat-update.md) | [<span data-ttu-id="d9b3d-117">plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="d9b3d-117">plannerProgressTaskBoardTaskFormat</span></span>](plannerprogresstaskboardtaskformat.md)    |<span data-ttu-id="d9b3d-118">Actualizar el objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-118">Update **plannerProgressTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="d9b3d-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9b3d-119">Properties</span></span>
| <span data-ttu-id="d9b3d-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9b3d-120">Property</span></span>     | <span data-ttu-id="d9b3d-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9b3d-121">Type</span></span>   |<span data-ttu-id="d9b3d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9b3d-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9b3d-123">id</span><span class="sxs-lookup"><span data-stu-id="d9b3d-123">id</span></span>|<span data-ttu-id="d9b3d-124">String</span><span class="sxs-lookup"><span data-stu-id="d9b3d-124">String</span></span>| <span data-ttu-id="d9b3d-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-125">Read-only.</span></span> <span data-ttu-id="d9b3d-126">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-126">ID of the resource.</span></span> <span data-ttu-id="d9b3d-127">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-127">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="d9b3d-128">[Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-128">[Format validation](tasks-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="d9b3d-129">orderHint</span><span class="sxs-lookup"><span data-stu-id="d9b3d-129">orderHint</span></span>|<span data-ttu-id="d9b3d-130">String</span><span class="sxs-lookup"><span data-stu-id="d9b3d-130">String</span></span>|<span data-ttu-id="d9b3d-p105">Valor de sugerencia usado para ordenar la tarea en la vista Progreso del panel de tareas. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="d9b3d-p105">Hint value used to order the task on the Progress view of the Task Board. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="d9b3d-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d9b3d-133">Relationships</span></span>
<span data-ttu-id="d9b3d-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d9b3d-134">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="d9b3d-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9b3d-135">JSON representation</span></span>
<span data-ttu-id="d9b3d-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-136">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerProgressTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerProgressTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->