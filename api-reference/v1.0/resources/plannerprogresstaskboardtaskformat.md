---
title: Tipo de recurso plannerProgressTaskBoardTaskFormat
description: El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada task tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 5b6989751a5ad32a40530d568ae1e0e04f25f6d4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938474"
---
# <a name="plannerprogresstaskboardtaskformat-resource-type"></a><span data-ttu-id="32d78-104">Tipo de recurso plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="32d78-104">plannerProgressTaskBoardTaskFormat resource type</span></span>

<span data-ttu-id="32d78-p102">El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada [task](plannertask.md) tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="32d78-p102">The **plannerProgressTaskBoardTaskFormat** resource represents the information used to render a task correctly in the Progress view of the Task Board (a view organized by the state of the PercentComplete field on the task object, with columns for Not Started, In Progress and Complete). Each [task](plannertask.md) will have one **plannerProgressTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="32d78-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="32d78-107">Methods</span></span>

| <span data-ttu-id="32d78-108">Método</span><span class="sxs-lookup"><span data-stu-id="32d78-108">Method</span></span>           | <span data-ttu-id="32d78-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32d78-109">Return Type</span></span>    |<span data-ttu-id="32d78-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="32d78-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="32d78-111">Obtener plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="32d78-111">Get plannerProgressTaskBoardTaskFormat</span></span>](../api/plannerprogresstaskboardtaskformat-get.md) | [<span data-ttu-id="32d78-112">plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="32d78-112">plannerProgressTaskBoardTaskFormat</span></span>](plannerprogresstaskboardtaskformat.md) |<span data-ttu-id="32d78-113">Leer las propiedades y las relaciones del objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="32d78-113">Read properties and relationships of **plannerProgressTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="32d78-114">Update</span><span class="sxs-lookup"><span data-stu-id="32d78-114">Update</span></span>](../api/plannerprogresstaskboardtaskformat-update.md) | [<span data-ttu-id="32d78-115">plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="32d78-115">plannerProgressTaskBoardTaskFormat</span></span>](plannerprogresstaskboardtaskformat.md)    |<span data-ttu-id="32d78-116">Actualizar el objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="32d78-116">Update **plannerProgressTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="32d78-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32d78-117">Properties</span></span>
| <span data-ttu-id="32d78-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32d78-118">Property</span></span>     | <span data-ttu-id="32d78-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="32d78-119">Type</span></span>   |<span data-ttu-id="32d78-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="32d78-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="32d78-121">id</span><span class="sxs-lookup"><span data-stu-id="32d78-121">id</span></span>|<span data-ttu-id="32d78-122">String</span><span class="sxs-lookup"><span data-stu-id="32d78-122">String</span></span>| <span data-ttu-id="32d78-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32d78-123">Read-only.</span></span> <span data-ttu-id="32d78-124">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="32d78-124">ID of the resource.</span></span> <span data-ttu-id="32d78-125">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="32d78-125">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="32d78-126">[Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="32d78-126">[Format validation](planner-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="32d78-127">orderHint</span><span class="sxs-lookup"><span data-stu-id="32d78-127">orderHint</span></span>|<span data-ttu-id="32d78-128">String</span><span class="sxs-lookup"><span data-stu-id="32d78-128">String</span></span>|<span data-ttu-id="32d78-p104">Valor de sugerencia usado para ordenar la tarea en la vista Progreso del panel de tareas. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="32d78-p104">Hint value used to order the task on the Progress view of the Task Board. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="32d78-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="32d78-131">Relationships</span></span>
<span data-ttu-id="32d78-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="32d78-132">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="32d78-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="32d78-133">JSON representation</span></span>
<span data-ttu-id="32d78-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="32d78-134">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
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
