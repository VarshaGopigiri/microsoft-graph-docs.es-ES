# <a name="plannertaskdetails-resource-type"></a><span data-ttu-id="25b6e-101">Tipo de recurso plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="25b6e-101">plannerTaskDetails resource type</span></span>

<span data-ttu-id="25b6e-p101">El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto [task](plannertask.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="25b6e-p101">The **plannerTaskDetails** resource represents the additional information about a task. Each [task](plannertask.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="25b6e-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="25b6e-104">Methods</span></span>

| <span data-ttu-id="25b6e-105">Método</span><span class="sxs-lookup"><span data-stu-id="25b6e-105">Method</span></span>           | <span data-ttu-id="25b6e-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25b6e-106">Return Type</span></span>    |<span data-ttu-id="25b6e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="25b6e-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="25b6e-108">Obtener plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="25b6e-108">Get plannerTaskDetails</span></span>](../api/plannertaskdetails_get.md) | [<span data-ttu-id="25b6e-109">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="25b6e-109">plannerTaskDetails</span></span>](plannertaskdetails.md) |<span data-ttu-id="25b6e-110">Leer las propiedades y las relaciones del objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="25b6e-110">Read properties and relationships of **plannerTaskDetails** object.</span></span>|
|[<span data-ttu-id="25b6e-111">Update</span><span class="sxs-lookup"><span data-stu-id="25b6e-111">Update</span></span>](../api/plannertaskdetails_update.md) | [<span data-ttu-id="25b6e-112">plannerTaskDetails</span><span class="sxs-lookup"><span data-stu-id="25b6e-112">plannerTaskDetails</span></span>](plannertaskdetails.md)    |<span data-ttu-id="25b6e-113">Actualizar el objeto **plannerTaskDetails**.</span><span class="sxs-lookup"><span data-stu-id="25b6e-113">Update **plannerTaskDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="25b6e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25b6e-114">Properties</span></span>
| <span data-ttu-id="25b6e-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25b6e-115">Property</span></span>     | <span data-ttu-id="25b6e-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="25b6e-116">Type</span></span>   |<span data-ttu-id="25b6e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="25b6e-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="25b6e-118">checklist</span><span class="sxs-lookup"><span data-stu-id="25b6e-118">checklist</span></span>|[<span data-ttu-id="25b6e-119">plannerChecklistItems</span><span class="sxs-lookup"><span data-stu-id="25b6e-119">plannerChecklistItems</span></span>](plannerchecklistitems.md)|<span data-ttu-id="25b6e-120">Colección de elementos de la lista de comprobación de la tarea.</span><span class="sxs-lookup"><span data-stu-id="25b6e-120">The collection of checklist items on the task.</span></span>|
|<span data-ttu-id="25b6e-121">description</span><span class="sxs-lookup"><span data-stu-id="25b6e-121">description</span></span>|<span data-ttu-id="25b6e-122">String</span><span class="sxs-lookup"><span data-stu-id="25b6e-122">String</span></span>|<span data-ttu-id="25b6e-123">Descripción de la tarea</span><span class="sxs-lookup"><span data-stu-id="25b6e-123">Description of the task</span></span>|
|<span data-ttu-id="25b6e-124">id</span><span class="sxs-lookup"><span data-stu-id="25b6e-124">id</span></span>|<span data-ttu-id="25b6e-125">String</span><span class="sxs-lookup"><span data-stu-id="25b6e-125">String</span></span>| <span data-ttu-id="25b6e-p102">Solo lectura. Id. de los detalles de la tarea. Tiene 28 caracteres y distingue entre mayúsculas y minúsculas. La [validación del formato](planner_identifiers_disclaimer.md) se efectúa en el servicio.</span><span class="sxs-lookup"><span data-stu-id="25b6e-p102">Read-only. ID of the task details. It is 28 characters long and case sensitive. [Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="25b6e-130">previewType</span><span class="sxs-lookup"><span data-stu-id="25b6e-130">previewType</span></span>|<span data-ttu-id="25b6e-131">string</span><span class="sxs-lookup"><span data-stu-id="25b6e-131">string</span></span>|<span data-ttu-id="25b6e-p103">Establece el tipo de vista previa que aparece en la tarea. Los valores posibles son `automatic`, `noPreview`, `checklist`, `description` y `reference`. Si se establece en `automatic`, la aplicación que visualiza la tarea elige la vista previa mostrada.</span><span class="sxs-lookup"><span data-stu-id="25b6e-p103">This sets the type of preview that shows up on the task. Possible values are: `automatic`, `noPreview`, `checklist`, `description`, `reference`. When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|
|<span data-ttu-id="25b6e-135">references</span><span class="sxs-lookup"><span data-stu-id="25b6e-135">references</span></span>|[<span data-ttu-id="25b6e-136">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="25b6e-136">plannerExternalReferences</span></span>](plannerexternalreferences.md)|<span data-ttu-id="25b6e-137">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="25b6e-137">The collection of references on the task.</span></span>|

## <a name="relationships"></a><span data-ttu-id="25b6e-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="25b6e-138">Relationships</span></span>
<span data-ttu-id="25b6e-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="25b6e-139">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="25b6e-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25b6e-140">JSON representation</span></span>
<span data-ttu-id="25b6e-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="25b6e-141">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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