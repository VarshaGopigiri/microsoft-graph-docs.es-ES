# <a name="plannerplandetails-resource-type"></a><span data-ttu-id="5f18c-101">Tipo de recurso plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="5f18c-101">plannerPlanDetails resource type</span></span>


<span data-ttu-id="5f18c-p101">El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto [plan](plannerplan.md) tiene un objeto details.</span><span class="sxs-lookup"><span data-stu-id="5f18c-p101">The **plannerPlanDetails** resource represents the additional information about a plan. Each [plan](plannerplan.md) object has a details object.</span></span>


## <a name="methods"></a><span data-ttu-id="5f18c-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f18c-104">Methods</span></span>

| <span data-ttu-id="5f18c-105">Método</span><span class="sxs-lookup"><span data-stu-id="5f18c-105">Method</span></span>           | <span data-ttu-id="5f18c-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f18c-106">Return Type</span></span>    |<span data-ttu-id="5f18c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f18c-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5f18c-108">Obtener plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="5f18c-108">Get plannerPlanDetails</span></span>](../api/plannerplandetails_get.md) | [<span data-ttu-id="5f18c-109">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="5f18c-109">plannerPlanDetails</span></span>](plannerplandetails.md) |<span data-ttu-id="5f18c-110">Leer las propiedades y las relaciones del objeto **plannerPlanDetails**.</span><span class="sxs-lookup"><span data-stu-id="5f18c-110">Read properties and relationships of **plannerPlanDetails** object.</span></span>|
|[<span data-ttu-id="5f18c-111">Update</span><span class="sxs-lookup"><span data-stu-id="5f18c-111">Update</span></span>](../api/plannerplandetails_update.md) | [<span data-ttu-id="5f18c-112">plannerPlanDetails</span><span class="sxs-lookup"><span data-stu-id="5f18c-112">plannerPlanDetails</span></span>](plannerplandetails.md)    |<span data-ttu-id="5f18c-113">Actualizar el objeto **plannerPlanDetails**.</span><span class="sxs-lookup"><span data-stu-id="5f18c-113">Update **plannerPlanDetails** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="5f18c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f18c-114">Properties</span></span>
| <span data-ttu-id="5f18c-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f18c-115">Property</span></span>     | <span data-ttu-id="5f18c-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f18c-116">Type</span></span>   |<span data-ttu-id="5f18c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f18c-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5f18c-118">categoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="5f18c-118">categoryDescriptions</span></span>|[<span data-ttu-id="5f18c-119">plannerCategoryDescriptions</span><span class="sxs-lookup"><span data-stu-id="5f18c-119">plannerCategoryDescriptions</span></span>](plannercategorydescriptions.md)|<span data-ttu-id="5f18c-120">Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan</span><span class="sxs-lookup"><span data-stu-id="5f18c-120">An object that specifies the descriptions of the six categories that can be associated with tasks in the plan</span></span>|
|<span data-ttu-id="5f18c-121">id</span><span class="sxs-lookup"><span data-stu-id="5f18c-121">id</span></span>|<span data-ttu-id="5f18c-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="5f18c-122">String</span></span>| <span data-ttu-id="5f18c-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f18c-123">Read-only.</span></span> <span data-ttu-id="5f18c-124">Identificador de los detalles del plan.</span><span class="sxs-lookup"><span data-stu-id="5f18c-124">ID of the plan details.</span></span> <span data-ttu-id="5f18c-125">Tiene 28 caracteres y distingue mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5f18c-125">It is 28 characters long and case-sensitive.</span></span> <span data-ttu-id="5f18c-126">[La validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.</span><span class="sxs-lookup"><span data-stu-id="5f18c-126">[Format validation](planner_identifiers_disclaimer.md) is done on the service.</span></span>|
|<span data-ttu-id="5f18c-127">sharedWith</span><span class="sxs-lookup"><span data-stu-id="5f18c-127">sharedWith</span></span>|[<span data-ttu-id="5f18c-128">plannerUserIds</span><span class="sxs-lookup"><span data-stu-id="5f18c-128">plannerUserIds</span></span>](planneruserids.md)|<span data-ttu-id="5f18c-p103">Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="5f18c-p103">Set of user ids that this plan is shared with. If you are leveraging Office 365 Groups, use the Groups API to manage group membership to share the [group's](group.md) plan. You can also add existing members of the group to this collection though it is not required for them to access the plan owned by the group.</span></span> |

## <a name="relationships"></a><span data-ttu-id="5f18c-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5f18c-132">Relationships</span></span>
<span data-ttu-id="5f18c-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5f18c-133">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="5f18c-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5f18c-134">JSON representation</span></span>
<span data-ttu-id="5f18c-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5f18c-135">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerPlanDetails"
}-->

```json
{
  "categoryDescriptions": {"@odata.type": "microsoft.graph.plannerCategoryDescriptions"},
  "id": "String (identifier)",
  "sharedWith": {"@odata.type": "microsoft.graph.plannerUserIds"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->