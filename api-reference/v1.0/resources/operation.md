# <a name="operation-resource-type"></a><span data-ttu-id="321c5-101">Tipo de recurso de operaciones</span><span class="sxs-lookup"><span data-stu-id="321c5-101">operation resource type</span></span>

<span data-ttu-id="321c5-102">El estado de una operación de larga ejecución.</span><span class="sxs-lookup"><span data-stu-id="321c5-102">The status of a long-running operation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="321c5-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="321c5-103">JSON representation</span></span>

<span data-ttu-id="321c5-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="321c5-104">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.operation"
}-->

```json
{
  "createdDateTime": "String (timestamp)",
  "lastActionDateTime": "String (timestamp)",
  "status": "notStarted | running | completed | failed"
}

```
## <a name="properties"></a><span data-ttu-id="321c5-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="321c5-105">Properties</span></span>
| <span data-ttu-id="321c5-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="321c5-106">Property</span></span>     | <span data-ttu-id="321c5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="321c5-107">Type</span></span>   |<span data-ttu-id="321c5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="321c5-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="321c5-109">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="321c5-109">createdDateTime</span></span>| <span data-ttu-id="321c5-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="321c5-110">DateTimeOffset</span></span> |<span data-ttu-id="321c5-111">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="321c5-111">The start time of the operation.</span></span>|
|<span data-ttu-id="321c5-112">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="321c5-112">lastActionDateTime</span></span>| <span data-ttu-id="321c5-113">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="321c5-113">DateTimeOffset</span></span> |<span data-ttu-id="321c5-114">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="321c5-114">The time of the last action of the operation.</span></span>|
|<span data-ttu-id="321c5-115">estado</span><span class="sxs-lookup"><span data-stu-id="321c5-115">status</span></span>|<span data-ttu-id="321c5-116">operationStatus</span><span class="sxs-lookup"><span data-stu-id="321c5-116">operationStatus</span></span>|<span data-ttu-id="321c5-117">Estado actual de la operación: `notStarted`, `running`, `completed` o `failed`</span><span class="sxs-lookup"><span data-stu-id="321c5-117">The current status of the operation: `notStarted`, `running`, `completed`, `failed`</span></span> |

<!-- uuid: 13fa92b1-3b41-498b-aab1-f943464a124f
2018-03-30 10:29:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "operation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
