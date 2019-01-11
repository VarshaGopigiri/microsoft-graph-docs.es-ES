---
title: Tipo de recurso plannerProgressTaskBoardTaskFormat
description: El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada task tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.
localization_priority: Normal
ms.openlocfilehash: 2f3395e0b63d038b8c280e54a76afcc2ca864789
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845587"
---
# <a name="plannerprogresstaskboardtaskformat-resource-type"></a><span data-ttu-id="1dc9b-104">Tipo de recurso plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="1dc9b-104">plannerProgressTaskBoardTaskFormat resource type</span></span>

> <span data-ttu-id="1dc9b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1dc9b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1dc9b-p103">El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada [task](plannertask.md) tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-p103">The **plannerProgressTaskBoardTaskFormat** resource represents the information used to render a task correctly in the Progress view of the Task Board (a view organized by the state of the PercentComplete field on the task object, with columns for Not Started, In Progress and Complete). Each [task](plannertask.md) will have one **plannerProgressTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="1dc9b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1dc9b-109">Methods</span></span>

| <span data-ttu-id="1dc9b-110">Método</span><span class="sxs-lookup"><span data-stu-id="1dc9b-110">Method</span></span>           | <span data-ttu-id="1dc9b-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dc9b-111">Return Type</span></span>    |<span data-ttu-id="1dc9b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dc9b-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="1dc9b-113">Obtener plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="1dc9b-113">Get plannerProgressTaskBoardTaskFormat</span></span>](../api/plannerprogresstaskboardtaskformat-get.md) | [<span data-ttu-id="1dc9b-114">plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="1dc9b-114">plannerProgressTaskBoardTaskFormat</span></span>](plannerprogresstaskboardtaskformat.md) |<span data-ttu-id="1dc9b-115">Leer las propiedades y las relaciones del objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-115">Read properties and relationships of **plannerProgressTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="1dc9b-116">Update</span><span class="sxs-lookup"><span data-stu-id="1dc9b-116">Update</span></span>](../api/plannerprogresstaskboardtaskformat-update.md) | [<span data-ttu-id="1dc9b-117">plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="1dc9b-117">plannerProgressTaskBoardTaskFormat</span></span>](plannerprogresstaskboardtaskformat.md)    |<span data-ttu-id="1dc9b-118">Actualizar el objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-118">Update **plannerProgressTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="1dc9b-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1dc9b-119">Properties</span></span>
| <span data-ttu-id="1dc9b-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1dc9b-120">Property</span></span>     | <span data-ttu-id="1dc9b-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="1dc9b-121">Type</span></span>   |<span data-ttu-id="1dc9b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dc9b-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1dc9b-123">id</span><span class="sxs-lookup"><span data-stu-id="1dc9b-123">id</span></span>|<span data-ttu-id="1dc9b-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="1dc9b-124">String</span></span>| <span data-ttu-id="1dc9b-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-125">Read-only.</span></span> <span data-ttu-id="1dc9b-126">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-126">ID of the resource.</span></span> <span data-ttu-id="1dc9b-127">Es 28 caracteres de largo y entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-127">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="1dc9b-128">[Validación de formato](tasks-identifiers-disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-128">[Format validation](tasks-identifiers-disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="1dc9b-129">orderHint</span><span class="sxs-lookup"><span data-stu-id="1dc9b-129">orderHint</span></span>|<span data-ttu-id="1dc9b-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="1dc9b-130">String</span></span>|<span data-ttu-id="1dc9b-p105">Valor de sugerencia usado para ordenar la tarea en la vista Progreso del panel de tareas. El formato se define tal como se describe [aquí](planner-order-hint-format.md).</span><span class="sxs-lookup"><span data-stu-id="1dc9b-p105">Hint value used to order the task on the Progress view of the Task Board. The format is defined as outlined [here](planner-order-hint-format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="1dc9b-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1dc9b-133">Relationships</span></span>
<span data-ttu-id="1dc9b-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1dc9b-134">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="1dc9b-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1dc9b-135">JSON representation</span></span>
<span data-ttu-id="1dc9b-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-136">Here is a JSON representation of the resource.</span></span>

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
