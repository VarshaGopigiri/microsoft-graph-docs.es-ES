# <a name="onenoteoperation-resource-type"></a><span data-ttu-id="4eadd-101">Tipo de recurso onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="4eadd-101">onenoteOperation resource type</span></span>

<span data-ttu-id="4eadd-102">Estado de ciertas operaciones de OneNote de larga duración.</span><span class="sxs-lookup"><span data-stu-id="4eadd-102">The status of certain long-running OneNote operations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4eadd-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4eadd-103">JSON representation</span></span>

<span data-ttu-id="4eadd-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4eadd-104">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteOperation"
}-->

```json
{
  "createdDateTime": "String (timestamp)",
  "error": {"@odata.type": "microsoft.graph.onenoteOperationError"},
  "id": "string (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "resourceId": "string",
  "resourceLocation": "string",
  "status": "string",
  "percentComplete": "string"
}

```
## <a name="properties"></a><span data-ttu-id="4eadd-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4eadd-105">Properties</span></span>
| <span data-ttu-id="4eadd-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4eadd-106">Property</span></span>     | <span data-ttu-id="4eadd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4eadd-107">Type</span></span>   |<span data-ttu-id="4eadd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4eadd-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4eadd-109">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4eadd-109">createdDateTime</span></span>| <span data-ttu-id="4eadd-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4eadd-110">DateTimeOffset</span></span> |<span data-ttu-id="4eadd-111">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="4eadd-111">The start time of the operation.</span></span>|
|<span data-ttu-id="4eadd-112">error</span><span class="sxs-lookup"><span data-stu-id="4eadd-112">error</span></span>|[<span data-ttu-id="4eadd-113">onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="4eadd-113">onenoteOperationError</span></span>](onenoteoperationerror.md)|<span data-ttu-id="4eadd-114">Error devuelto por la operación.</span><span class="sxs-lookup"><span data-stu-id="4eadd-114">The error returned by the operation.</span></span>|
|<span data-ttu-id="4eadd-115">id</span><span class="sxs-lookup"><span data-stu-id="4eadd-115">id</span></span>|<span data-ttu-id="4eadd-116">string</span><span class="sxs-lookup"><span data-stu-id="4eadd-116">string</span></span>|<span data-ttu-id="4eadd-117">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4eadd-117">The operation id. Read-only.</span></span>|
|<span data-ttu-id="4eadd-118">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="4eadd-118">lastActionDateTime</span></span>| <span data-ttu-id="4eadd-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4eadd-119">DateTimeOffset</span></span> |<span data-ttu-id="4eadd-120">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="4eadd-120">The time of the last action of the operation.</span></span>|
|<span data-ttu-id="4eadd-121">resourceId</span><span class="sxs-lookup"><span data-stu-id="4eadd-121">resourceId</span></span>|<span data-ttu-id="4eadd-122">cadena</span><span class="sxs-lookup"><span data-stu-id="4eadd-122">string</span></span>|<span data-ttu-id="4eadd-123">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="4eadd-123">The resource id.</span></span>|
|<span data-ttu-id="4eadd-124">resourceLocation</span><span class="sxs-lookup"><span data-stu-id="4eadd-124">resourceLocation</span></span>|<span data-ttu-id="4eadd-125">string</span><span class="sxs-lookup"><span data-stu-id="4eadd-125">string</span></span>|<span data-ttu-id="4eadd-p101">URI de recurso del objeto. Por ejemplo, el URI de recurso de una página o sección copiada.</span><span class="sxs-lookup"><span data-stu-id="4eadd-p101">The resource URI for the object. For example, the resource URI for a copied page or section.</span></span> |
|<span data-ttu-id="4eadd-128">status</span><span class="sxs-lookup"><span data-stu-id="4eadd-128">status</span></span>|<span data-ttu-id="4eadd-129">cadena</span><span class="sxs-lookup"><span data-stu-id="4eadd-129">string</span></span>|<span data-ttu-id="4eadd-130">Estado actual de la operación: `notstarted`, `running`, `completed` o `failed`</span><span class="sxs-lookup"><span data-stu-id="4eadd-130">The current status of the operation: `notstarted`, `running`, `completed`, `failed`</span></span> |
|<span data-ttu-id="4eadd-131">percentComplete</span><span class="sxs-lookup"><span data-stu-id="4eadd-131">percentComplete</span></span>|<span data-ttu-id="4eadd-132">cadena</span><span class="sxs-lookup"><span data-stu-id="4eadd-132">string</span></span>|<span data-ttu-id="4eadd-133">El porcentaje de operación completada si la operación todavía tiene el estado `running`</span><span class="sxs-lookup"><span data-stu-id="4eadd-133">The operation percent complete if the operation is still in `running` status</span></span>

## <a name="relationships"></a><span data-ttu-id="4eadd-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4eadd-134">Relationships</span></span>
<span data-ttu-id="4eadd-135">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4eadd-135">None</span></span>


## <a name="methods"></a><span data-ttu-id="4eadd-136">Métodos</span><span class="sxs-lookup"><span data-stu-id="4eadd-136">Methods</span></span>

| <span data-ttu-id="4eadd-137">Método</span><span class="sxs-lookup"><span data-stu-id="4eadd-137">Method</span></span>           | <span data-ttu-id="4eadd-138">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4eadd-138">Return Type</span></span>    |<span data-ttu-id="4eadd-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="4eadd-139">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="4eadd-140">Obtener operation</span><span class="sxs-lookup"><span data-stu-id="4eadd-140">Get operation</span></span>](../api/onenoteoperation_get.md) | [<span data-ttu-id="4eadd-141">onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="4eadd-141">onenoteOperation</span></span>](onenoteoperation.md) |<span data-ttu-id="4eadd-142">Obtener el estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="4eadd-142">Get the status of the operation.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
