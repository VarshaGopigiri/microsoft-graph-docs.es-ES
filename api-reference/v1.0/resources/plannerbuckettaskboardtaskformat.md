# <a name="plannerbuckettaskboardtaskformat-resource-type"></a><span data-ttu-id="05230-101">Tipo de recurso plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="05230-101">plannerBucketTaskBoardTaskFormat resource type</span></span>

<span data-ttu-id="05230-p101">El recurso **plannerBucketTaskBoardTaskFormat** representa la información usada para procesar una tarea correctamente en la vista Depósitos del panel de tareas (una vista organizada por tareas dentro de los depósitos a los que están asignadas). Cada [task](plannertask.md) tendrá un objeto **plannerBucketTaskBoardTaskFormat** asociado.</span><span class="sxs-lookup"><span data-stu-id="05230-p101">The **plannerBucketTaskBoardTaskFormat** resource represents the information used to render a task correctly in the Buckets view of the Task Board (a view organized by tasks within the buckets they are assigned to). Each [task](plannertask.md) will have one **plannerBucketTaskBoardTaskFormat** object associated with it.</span></span>


## <a name="methods"></a><span data-ttu-id="05230-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="05230-104">Methods</span></span>

| <span data-ttu-id="05230-105">Método</span><span class="sxs-lookup"><span data-stu-id="05230-105">Method</span></span>           | <span data-ttu-id="05230-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05230-106">Return Type</span></span>    |<span data-ttu-id="05230-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="05230-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="05230-108">Obtener plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="05230-108">Get plannerBucketTaskBoardTaskFormat</span></span>](../api/plannerbuckettaskboardtaskformat_get.md) | [<span data-ttu-id="05230-109">plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="05230-109">plannerBucketTaskBoardTaskFormat</span></span>](plannerbuckettaskboardtaskformat.md) |<span data-ttu-id="05230-110">Leer las propiedades y las relaciones del objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="05230-110">Read properties and relationships of **plannerBucketTaskBoardTaskFormat** object.</span></span>|
|[<span data-ttu-id="05230-111">Update</span><span class="sxs-lookup"><span data-stu-id="05230-111">Update</span></span>](../api/plannerbuckettaskboardtaskformat_update.md) | [<span data-ttu-id="05230-112">plannerBucketTaskBoardTaskFormat</span><span class="sxs-lookup"><span data-stu-id="05230-112">plannerBucketTaskBoardTaskFormat</span></span>](plannerbuckettaskboardtaskformat.md)  |<span data-ttu-id="05230-113">Actualizar el objeto **plannerBucketTaskBoardTaskFormat**.</span><span class="sxs-lookup"><span data-stu-id="05230-113">Update **plannerBucketTaskBoardTaskFormat** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="05230-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="05230-114">Properties</span></span>
| <span data-ttu-id="05230-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05230-115">Property</span></span>     | <span data-ttu-id="05230-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="05230-116">Type</span></span>   |<span data-ttu-id="05230-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="05230-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="05230-118">id</span><span class="sxs-lookup"><span data-stu-id="05230-118">id</span></span>|<span data-ttu-id="05230-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="05230-119">String</span></span>| <span data-ttu-id="05230-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="05230-120">Read-only.</span></span> <span data-ttu-id="05230-121">El identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="05230-121">The ID of the resource.</span></span> <span data-ttu-id="05230-122">Tiene 28 caracteres y distingue mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="05230-122">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="05230-123">[La validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="05230-123">[Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="05230-124">orderHint</span><span class="sxs-lookup"><span data-stu-id="05230-124">orderHint</span></span>|<span data-ttu-id="05230-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="05230-125">String</span></span>|<span data-ttu-id="05230-p103">Sugerencia usada para ordenar tareas en la vista Depósito del panel de tareas. El formato se define tal como se describe [aquí](planner_order_hint_format.md).</span><span class="sxs-lookup"><span data-stu-id="05230-p103">Hint used to order tasks in the Bucket view of the Task Board. The format is defined as outlined [here](planner_order_hint_format.md).</span></span>|

## <a name="relationships"></a><span data-ttu-id="05230-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="05230-128">Relationships</span></span>
<span data-ttu-id="05230-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="05230-129">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="05230-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="05230-130">JSON representation</span></span>
<span data-ttu-id="05230-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="05230-131">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerBucketTaskBoardTaskFormat"
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
  "description": "plannerBucketTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->