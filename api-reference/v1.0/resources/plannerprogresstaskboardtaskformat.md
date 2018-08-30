# <a name="plannerprogresstaskboardtaskformat-resource-type"></a><span data-ttu-id="e50bc-101">Tipo de recurso plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="e50bc-101">plannerProgressTaskBoardTaskFormat resource type</span></span>

<span data-ttu-id="e50bc-p101">El recurso **plannerProgressTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Progreso del panel de tareas (una vista organizada por el estado del campo PorcentajeCompletado en el objeto de la tarea, con columnas para No iniciado, En curso y Completado). Cada [task](plannertask.md) tendrá un objeto **plannerProgressTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="e50bc-p101">The **plannerProgressTaskBoardTaskFormat** resource represents the information used to render a task correctly in the Progress view of the Task Board (a view organized by the state of the PercentComplete field on the task object, with columns for Not Started, In Progress and Complete). Each [task](plannertask.md) will have one **plannerProgressTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="e50bc-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="e50bc-104">Methods</span></span>

| <span data-ttu-id="e50bc-105">Método</span><span class="sxs-lookup"><span data-stu-id="e50bc-105">Method</span></span>           | <span data-ttu-id="e50bc-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e50bc-106">Return Type</span></span>    |<span data-ttu-id="e50bc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e50bc-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e50bc-108">Obtener plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="e50bc-108">Get plannerProgressTaskBoardTaskFormat</span></span>](../api/plannerprogresstaskboardtaskformat_get.md) | [<span data-ttu-id="e50bc-109">plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="e50bc-109">plannerProgressTaskBoardTaskFormat</span></span>](plannerprogresstaskboardtaskformat.md) |<span data-ttu-id="e50bc-110">Leer las propiedades y las relaciones del objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="e50bc-110">Read properties and relationships of **plannerProgressTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="e50bc-111">Update</span><span class="sxs-lookup"><span data-stu-id="e50bc-111">Update</span></span>](../api/plannerprogresstaskboardtaskformat_update.md) | [<span data-ttu-id="e50bc-112">plannerProgressTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="e50bc-112">plannerProgressTaskBoardTaskFormat</span></span>](plannerprogresstaskboardtaskformat.md)    |<span data-ttu-id="e50bc-113">Actualizar el objeto **plannerProgressTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="e50bc-113">Update **plannerProgressTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="e50bc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e50bc-114">Properties</span></span>
| <span data-ttu-id="e50bc-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e50bc-115">Property</span></span>     | <span data-ttu-id="e50bc-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="e50bc-116">Type</span></span>   |<span data-ttu-id="e50bc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e50bc-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e50bc-118">id</span><span class="sxs-lookup"><span data-stu-id="e50bc-118">id</span></span>|<span data-ttu-id="e50bc-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="e50bc-119">String</span></span>| <span data-ttu-id="e50bc-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e50bc-120">Read-only.</span></span> <span data-ttu-id="e50bc-121">El identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="e50bc-121">The ID of the resource.</span></span> <span data-ttu-id="e50bc-122">Tiene 28 caracteres y distingue mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e50bc-122">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="e50bc-123">[La validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="e50bc-123">[Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="e50bc-124">orderHint</span><span class="sxs-lookup"><span data-stu-id="e50bc-124">orderHint</span></span>|<span data-ttu-id="e50bc-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="e50bc-125">String</span></span>|<span data-ttu-id="e50bc-p103">Valor de sugerencia usado para ordenar la tarea en la vista Progreso del panel de tareas. El formato se define tal como se describe [aquí](planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="e50bc-p103">Hint value used to order the task on the Progress view of the Task Board. The format is defined as outlined [here](planner_order_hint_format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="e50bc-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e50bc-128">Relationships</span></span>
<span data-ttu-id="e50bc-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e50bc-129">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e50bc-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e50bc-130">JSON representation</span></span>
<span data-ttu-id="e50bc-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e50bc-131">Here is a JSON representation of the resource.</span></span>

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