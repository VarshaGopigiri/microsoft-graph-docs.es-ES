# <a name="plannerassignedtotaskboardtaskformat-resource-type"></a><span data-ttu-id="0d335-101">Tipo de recurso plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="0d335-101">plannerAssignedToTaskBoardTaskFormat resource type</span></span>

<span data-ttu-id="0d335-p101">El recurso **plannerAssignedToTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista AsignadoA del panel de tareas (una vista organizada por usuarios a los que se asignan las tareas). Cada [task](plannertask.md) tendrá un objeto **plannerAssignedToTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="0d335-p101">The **plannerAssignedToTaskBoardTaskFormat** resource represents the information used to render a task correctly in the AssignedTo view of the Task Board (a view organized by users to whom tasks are assigned to). Each [task](plannertask.md) will have one **plannerAssignedToTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="0d335-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d335-104">Methods</span></span>

| <span data-ttu-id="0d335-105">Método</span><span class="sxs-lookup"><span data-stu-id="0d335-105">Method</span></span>           | <span data-ttu-id="0d335-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d335-106">Return Type</span></span>    |<span data-ttu-id="0d335-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d335-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0d335-108">Obtener plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="0d335-108">Get plannerAssignedToTaskBoardTaskFormat</span></span>](../api/plannerassignedtotaskboardtaskformat_get.md) | [<span data-ttu-id="0d335-109">plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="0d335-109">plannerAssignedToTaskBoardTaskFormat</span></span>](plannerassignedtotaskboardtaskformat.md) |<span data-ttu-id="0d335-110">Leer las propiedades y las relaciones del objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="0d335-110">Read properties and relationships of **plannerAssignedToTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="0d335-111">Update</span><span class="sxs-lookup"><span data-stu-id="0d335-111">Update</span></span>](../api/plannerassignedtotaskboardtaskformat_update.md) | [<span data-ttu-id="0d335-112">plannerAssignedToTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="0d335-112">plannerAssignedToTaskBoardTaskFormat</span></span>](plannerassignedtotaskboardtaskformat.md)  |<span data-ttu-id="0d335-113">Actualizar el objeto **plannerAssignedToTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="0d335-113">Update **plannerAssignedToTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="0d335-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d335-114">Properties</span></span>
| <span data-ttu-id="0d335-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0d335-115">Property</span></span>     | <span data-ttu-id="0d335-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d335-116">Type</span></span>   |<span data-ttu-id="0d335-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d335-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0d335-118">id</span><span class="sxs-lookup"><span data-stu-id="0d335-118">id</span></span>|<span data-ttu-id="0d335-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="0d335-119">String</span></span>| <span data-ttu-id="0d335-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0d335-120">Read-only.</span></span> <span data-ttu-id="0d335-121">El identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="0d335-121">The ID of the resource.</span></span> <span data-ttu-id="0d335-122">Tiene 28 caracteres y distingue mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0d335-122">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="0d335-123">La [validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="0d335-123">[Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="0d335-124">orderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="0d335-124">orderHintsByAssignee</span></span>|[<span data-ttu-id="0d335-125">plannerOrderHintsByAssignee</span><span class="sxs-lookup"><span data-stu-id="0d335-125">plannerOrderHintsByAssignee</span></span>](plannerorderhintsbyassignee.md)|<span data-ttu-id="0d335-p103">Diccionario de sugerencias usadas para ordenar las tareas en la vista AsignadoA del panel de tareas. La clave de cada entrada es uno de los usuarios a los que se ha asignado la tarea, mientras que el valor es la sugerencia de orden. El formato de cada valor se define tal como se describe [aquí](planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="0d335-p103">Dictionary of hints used to order tasks on the AssignedTo view of the Task Board. The key of each entry is one of the users the task is assigned to and the value is the order hint. The format of each value is defined as outlined [here](planner_order_hint_format.md).</span></span>|
|<span data-ttu-id="0d335-129">unassignedOrderHint</span><span class="sxs-lookup"><span data-stu-id="0d335-129">unassignedOrderHint</span></span>|<span data-ttu-id="0d335-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="0d335-130">String</span></span>|<span data-ttu-id="0d335-p104">Valor de sugerencia usado para ordenar la tarea en la vista AsignadoA del panel de tareas si la tarea no está asignada a nadie, o si el diccionario orderHintsByAssignee no proporciona ninguna sugerencia de orden para el usuario al que se ha asignado la tarea. El formato se define tal como se describe [aquí](planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="0d335-p104">Hint value used to order the task on the AssignedTo view of the Task Board when the task is not assigned to anyone, or if the orderHintsByAssignee dictionary does not provide an order hint for the user the task is assigned to. The format is defined as outlined [here](planner_order_hint_format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="0d335-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0d335-133">Relationships</span></span>
<span data-ttu-id="0d335-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0d335-134">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="0d335-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0d335-135">JSON representation</span></span>
<span data-ttu-id="0d335-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0d335-136">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerAssignedToTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHintsByAssignee": {"@odata.type": "microsoft.graph.plannerOrderHintsByAssignee"},
  "unassignedOrderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignedToTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->