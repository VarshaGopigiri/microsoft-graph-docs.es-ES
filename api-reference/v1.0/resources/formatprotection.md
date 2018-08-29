# <a name="formatprotection-resource-type"></a><span data-ttu-id="7169a-101">Tipo de recurso FormatProtection</span><span class="sxs-lookup"><span data-stu-id="7169a-101">FormatProtection resource type</span></span>

<span data-ttu-id="7169a-102">Representa la protección de formato de un objeto range.</span><span class="sxs-lookup"><span data-stu-id="7169a-102">Represents the format protection of a range object.</span></span>


## <a name="methods"></a><span data-ttu-id="7169a-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="7169a-103">Methods</span></span>

| <span data-ttu-id="7169a-104">Método</span><span class="sxs-lookup"><span data-stu-id="7169a-104">Method</span></span>           | <span data-ttu-id="7169a-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7169a-105">Return Type</span></span>    |<span data-ttu-id="7169a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7169a-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="7169a-107">Obtener FormatProtection</span><span class="sxs-lookup"><span data-stu-id="7169a-107">Get FormatProtection</span></span>](../api/formatprotection_get.md) | [<span data-ttu-id="7169a-108">FormatProtection</span><span class="sxs-lookup"><span data-stu-id="7169a-108">FormatProtection</span></span>](formatprotection.md) |<span data-ttu-id="7169a-109">Lee las propiedades y relaciones del objeto formatProtection.</span><span class="sxs-lookup"><span data-stu-id="7169a-109">Read properties and relationships of formatProtection object.</span></span>|
|[<span data-ttu-id="7169a-110">Actualizar</span><span class="sxs-lookup"><span data-stu-id="7169a-110">Update</span></span>](../api/formatprotection_update.md) | [<span data-ttu-id="7169a-111">FormatProtection</span><span class="sxs-lookup"><span data-stu-id="7169a-111">FormatProtection</span></span>](formatprotection.md)  |<span data-ttu-id="7169a-112">Actualiza el objeto FormatProtection.</span><span class="sxs-lookup"><span data-stu-id="7169a-112">Update FormatProtection object.</span></span> |

## <a name="properties"></a><span data-ttu-id="7169a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7169a-113">Properties</span></span>
| <span data-ttu-id="7169a-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7169a-114">Property</span></span>     | <span data-ttu-id="7169a-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="7169a-115">Type</span></span>   |<span data-ttu-id="7169a-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7169a-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7169a-117">formulaHidden</span><span class="sxs-lookup"><span data-stu-id="7169a-117">formulaHidden</span></span>|<span data-ttu-id="7169a-118">booleano</span><span class="sxs-lookup"><span data-stu-id="7169a-118">boolean</span></span>|<span data-ttu-id="7169a-p101">Indica si Excel oculta la fórmula de las celdas del rango. Un valor null indica que el rango no tiene una configuración de fórmula oculta uniforme.</span><span class="sxs-lookup"><span data-stu-id="7169a-p101">Indicates if Excel hides the formula for the cells in the range. A null value indicates that the entire range doesn't have uniform formula hidden setting.</span></span>|
|<span data-ttu-id="7169a-121">locked</span><span class="sxs-lookup"><span data-stu-id="7169a-121">locked</span></span>|<span data-ttu-id="7169a-122">booleano</span><span class="sxs-lookup"><span data-stu-id="7169a-122">boolean</span></span>|<span data-ttu-id="7169a-p102">Indica si Excel bloquea las celdas del objeto. Un valor nulo indica que todo el rango no tiene una configuración de bloqueo uniforme.</span><span class="sxs-lookup"><span data-stu-id="7169a-p102">Indicates if Excel locks the cells in the object. A null value indicates that the entire range doesn't have uniform lock setting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7169a-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7169a-125">Relationships</span></span>
<span data-ttu-id="7169a-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7169a-126">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="7169a-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7169a-127">JSON representation</span></span>

<span data-ttu-id="7169a-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7169a-128">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFormatProtection"
}-->

```json
{
  "formulaHidden": true,
  "locked": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "FormatProtection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->