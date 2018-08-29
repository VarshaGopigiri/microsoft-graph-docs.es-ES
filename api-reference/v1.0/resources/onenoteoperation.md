# <a name="onenoteoperation-resource-type"></a><span data-ttu-id="fe51c-101">Tipo de recurso onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="fe51c-101">onenoteOperation resource type</span></span>

<span data-ttu-id="fe51c-102">Estado de ciertas operaciones de OneNote de larga duración.</span><span class="sxs-lookup"><span data-stu-id="fe51c-102">The status of certain long-running OneNote operations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="fe51c-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fe51c-103">JSON representation</span></span>

<span data-ttu-id="fe51c-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fe51c-104">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.operation",
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
## <a name="properties"></a><span data-ttu-id="fe51c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe51c-105">Properties</span></span>
| <span data-ttu-id="fe51c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fe51c-106">Property</span></span>     | <span data-ttu-id="fe51c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe51c-107">Type</span></span>   |<span data-ttu-id="fe51c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe51c-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fe51c-109">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="fe51c-109">createdDateTime</span></span>| <span data-ttu-id="fe51c-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fe51c-110">DateTimeOffset</span></span> |<span data-ttu-id="fe51c-111">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="fe51c-111">The start time of the operation.</span></span>|
|<span data-ttu-id="fe51c-112">error</span><span class="sxs-lookup"><span data-stu-id="fe51c-112">error</span></span>|[<span data-ttu-id="fe51c-113">onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="fe51c-113">onenoteOperationError</span></span>](onenoteoperationerror.md)|<span data-ttu-id="fe51c-114">Error devuelto por la operación.</span><span class="sxs-lookup"><span data-stu-id="fe51c-114">The error returned by the operation.</span></span>|
|<span data-ttu-id="fe51c-115">id</span><span class="sxs-lookup"><span data-stu-id="fe51c-115">id</span></span>|<span data-ttu-id="fe51c-116">string</span><span class="sxs-lookup"><span data-stu-id="fe51c-116">string</span></span>|<span data-ttu-id="fe51c-117">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fe51c-117">The operation id. Read-only.</span></span>|
|<span data-ttu-id="fe51c-118">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="fe51c-118">lastActionDateTime</span></span>| <span data-ttu-id="fe51c-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fe51c-119">DateTimeOffset</span></span> |<span data-ttu-id="fe51c-120">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="fe51c-120">The time of the last action of the operation.</span></span>|
|<span data-ttu-id="fe51c-121">resourceId</span><span class="sxs-lookup"><span data-stu-id="fe51c-121">resourceId</span></span>|<span data-ttu-id="fe51c-122">string</span><span class="sxs-lookup"><span data-stu-id="fe51c-122">string</span></span>|<span data-ttu-id="fe51c-123">Identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="fe51c-123">The resource id.</span></span>|
|<span data-ttu-id="fe51c-124">resourceLocation</span><span class="sxs-lookup"><span data-stu-id="fe51c-124">resourceLocation</span></span>|<span data-ttu-id="fe51c-125">string</span><span class="sxs-lookup"><span data-stu-id="fe51c-125">string</span></span>|<span data-ttu-id="fe51c-p101">URI de recurso del objeto. Por ejemplo, el URI de recurso de una página o sección copiada.</span><span class="sxs-lookup"><span data-stu-id="fe51c-p101">The resource URI for the object. For example, the resource URI for a copied page or section.</span></span> |
|<span data-ttu-id="fe51c-128">status</span><span class="sxs-lookup"><span data-stu-id="fe51c-128">status</span></span>|<span data-ttu-id="fe51c-129">cadena</span><span class="sxs-lookup"><span data-stu-id="fe51c-129">string</span></span>|<span data-ttu-id="fe51c-130">Estado actual de la operación: `notstarted`, `running`, `completed` o `failed`</span><span class="sxs-lookup"><span data-stu-id="fe51c-130">The current status of the operation: `notstarted`, `running`, `completed`, `failed`</span></span> |
|<span data-ttu-id="fe51c-131">percentComplete</span><span class="sxs-lookup"><span data-stu-id="fe51c-131">percentComplete</span></span>|<span data-ttu-id="fe51c-132">cadena</span><span class="sxs-lookup"><span data-stu-id="fe51c-132">string</span></span>|<span data-ttu-id="fe51c-133">El porcentaje de operación completada si la operación todavía tiene el estado `running`</span><span class="sxs-lookup"><span data-stu-id="fe51c-133">The operation percent complete if the operation is still in `running` status</span></span>

## <a name="relationships"></a><span data-ttu-id="fe51c-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fe51c-134">Relationships</span></span>
<span data-ttu-id="fe51c-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fe51c-135">None</span></span>


## <a name="methods"></a><span data-ttu-id="fe51c-136">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe51c-136">Methods</span></span>

| <span data-ttu-id="fe51c-137">Método</span><span class="sxs-lookup"><span data-stu-id="fe51c-137">Method</span></span>           | <span data-ttu-id="fe51c-138">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe51c-138">Return Type</span></span>    |<span data-ttu-id="fe51c-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe51c-139">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="fe51c-140">Obtener operation</span><span class="sxs-lookup"><span data-stu-id="fe51c-140">Get operation</span></span>](../api/onenoteoperation_get.md) | [<span data-ttu-id="fe51c-141">onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="fe51c-141">onenoteOperation</span></span>](onenoteoperation.md) |<span data-ttu-id="fe51c-142">Obtener el estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="fe51c-142">Get the status of the operation.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
