# <a name="plannertaskdetails-resource-type"></a><span data-ttu-id="201f3-101">Tipo de recurso plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="201f3-101">plannerTaskDetails resource type</span></span>

<span data-ttu-id="201f3-p101">El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto [task](plannertask.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="201f3-p101">The **plannerTaskDetails** resource represents the additional information about a task. Each [task](plannertask.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="201f3-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="201f3-104">Methods</span></span>

| <span data-ttu-id="201f3-105">Método</span><span class="sxs-lookup"><span data-stu-id="201f3-105">Method</span></span>           | <span data-ttu-id="201f3-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="201f3-106">Return Type</span></span>    |<span data-ttu-id="201f3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="201f3-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="201f3-108">Obtener plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="201f3-108">Get plannerTaskDetails</span></span>](../api/plannertaskdetails_get.md) | [<span data-ttu-id="201f3-109">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="201f3-109">plannerTaskDetails</span></span>](plannertaskdetails.md) |<span data-ttu-id="201f3-110">Leer las propiedades y las relaciones del objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="201f3-110">Read properties and relationships of **plannerTaskDetails** object.</span></span>|
|[<span data-ttu-id="201f3-111">Update</span><span class="sxs-lookup"><span data-stu-id="201f3-111">Update</span></span>](../api/plannertaskdetails_update.md) | [<span data-ttu-id="201f3-112">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="201f3-112">plannerTaskDetails</span></span>](plannertaskdetails.md)    |<span data-ttu-id="201f3-113">Actualizar el objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="201f3-113">Update **plannerTaskDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="201f3-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="201f3-114">Properties</span></span>
| <span data-ttu-id="201f3-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="201f3-115">Property</span></span>     | <span data-ttu-id="201f3-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="201f3-116">Type</span></span>   |<span data-ttu-id="201f3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="201f3-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="201f3-118">checklist</span><span class="sxs-lookup"><span data-stu-id="201f3-118">checklist</span></span>|[<span data-ttu-id="201f3-119">plannerChecklistItems</span><span class="sxs-lookup"><span data-stu-id="201f3-119">plannerChecklistItems</span></span>](plannerchecklistitems.md)|<span data-ttu-id="201f3-120">Colección de elementos de la lista de comprobación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="201f3-120">The collection of checklist items on the task.</span></span>|
|<span data-ttu-id="201f3-121">description</span><span class="sxs-lookup"><span data-stu-id="201f3-121">description</span></span>|<span data-ttu-id="201f3-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="201f3-122">String</span></span>|<span data-ttu-id="201f3-123">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="201f3-123">Description of the task</span></span>|
|<span data-ttu-id="201f3-124">id</span><span class="sxs-lookup"><span data-stu-id="201f3-124">id</span></span>|<span data-ttu-id="201f3-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="201f3-125">String</span></span>| <span data-ttu-id="201f3-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="201f3-126">Read-only.</span></span> <span data-ttu-id="201f3-127">Identificador de los detalles de la tarea.</span><span class="sxs-lookup"><span data-stu-id="201f3-127">ID of the task details.</span></span> <span data-ttu-id="201f3-128">Tiene 28 caracteres y distingue mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="201f3-128">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="201f3-129">La [validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="201f3-129">[Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="201f3-130">previewType</span><span class="sxs-lookup"><span data-stu-id="201f3-130">previewType</span></span>|<span data-ttu-id="201f3-131">cadena</span><span class="sxs-lookup"><span data-stu-id="201f3-131">string</span></span>|<span data-ttu-id="201f3-132">Esto establece el tipo de vista previa que se muestra en la tarea.</span><span class="sxs-lookup"><span data-stu-id="201f3-132">This sets the type of preview that shows up on the task. Possible values are: , , , , .</span></span> <span data-ttu-id="201f3-133">Los valores posibles son: `automatic`, `noPreview`, `checklist`, `description` y `reference`.</span><span class="sxs-lookup"><span data-stu-id="201f3-133">The possible values are `automatic`, `noPreview`, `checklist`, `description`, `reference`, , , , , , , or .</span></span> <span data-ttu-id="201f3-134">Cuando se establece en `automatic` la vista previa que se muestra es elegida por la aplicación de visualización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="201f3-134">This sets the type of preview that shows up on the task. Possible values are: , , , , . When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|
|<span data-ttu-id="201f3-135">references</span><span class="sxs-lookup"><span data-stu-id="201f3-135">references</span></span>|[<span data-ttu-id="201f3-136">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="201f3-136">plannerExternalReferences</span></span>](plannerexternalreferences.md)|<span data-ttu-id="201f3-137">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="201f3-137">The collection of references on the task.</span></span>|

## <a name="relationships"></a><span data-ttu-id="201f3-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="201f3-138">Relationships</span></span>
<span data-ttu-id="201f3-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="201f3-139">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="201f3-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="201f3-140">JSON representation</span></span>
<span data-ttu-id="201f3-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="201f3-141">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerTaskDetails"
}-->

```json
{
  "checklist": {"@odata.type": "microsoft.graph.plannerChecklistItems"},
  "description": "String",
  "id": "String (identifier)",
  "previewType": "string",
  "references": {"@odata.type": "microsoft.graph.plannerExternalReferences"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerTaskDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
