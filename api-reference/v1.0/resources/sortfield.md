# <a name="sortfield-resource-type"></a><span data-ttu-id="06df7-101">Tipo de recurso SortField</span><span class="sxs-lookup"><span data-stu-id="06df7-101">SortField resource type</span></span>

<span data-ttu-id="06df7-102">Representa una condición en una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="06df7-102">Represents a condition in a sorting operation.</span></span>

## <a name="properties"></a><span data-ttu-id="06df7-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06df7-103">Properties</span></span>
| <span data-ttu-id="06df7-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06df7-104">Property</span></span>     | <span data-ttu-id="06df7-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="06df7-105">Type</span></span>   |<span data-ttu-id="06df7-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="06df7-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="06df7-107">ascending</span><span class="sxs-lookup"><span data-stu-id="06df7-107">ascending</span></span>|<span data-ttu-id="06df7-108">booleano</span><span class="sxs-lookup"><span data-stu-id="06df7-108">boolean</span></span>|<span data-ttu-id="06df7-109">Representa si la ordenación se realiza en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="06df7-109">Represents whether the sorting is done in an ascending fashion.</span></span>|
|<span data-ttu-id="06df7-110">color</span><span class="sxs-lookup"><span data-stu-id="06df7-110">color</span></span>|<span data-ttu-id="06df7-111">cadena</span><span class="sxs-lookup"><span data-stu-id="06df7-111">string</span></span>|<span data-ttu-id="06df7-112">Representa el color que es el destino de la condición si la ordenación se realiza según la fuente o el color de celda.</span><span class="sxs-lookup"><span data-stu-id="06df7-112">Represents the color that is the target of the condition if the sorting is on font or cell color.</span></span>|
|<span data-ttu-id="06df7-113">dataOption</span><span class="sxs-lookup"><span data-stu-id="06df7-113">dataOption</span></span>|<span data-ttu-id="06df7-114">cadena</span><span class="sxs-lookup"><span data-stu-id="06df7-114">string</span></span>|<span data-ttu-id="06df7-115">Representa las opciones de ordenación adicionales para este campo.</span><span class="sxs-lookup"><span data-stu-id="06df7-115">Represents additional sorting options for this field. Possible values are: , .</span></span> <span data-ttu-id="06df7-116">Los valores posibles son: `Normal`, `TextAsNumber`.</span><span class="sxs-lookup"><span data-stu-id="06df7-116">The possible values are:</span></span>|
|<span data-ttu-id="06df7-117">key</span><span class="sxs-lookup"><span data-stu-id="06df7-117">key</span></span>|<span data-ttu-id="06df7-118">entero</span><span class="sxs-lookup"><span data-stu-id="06df7-118">int</span></span>|<span data-ttu-id="06df7-p102">Representa la columna (o fila, según la orientación de ordenación) en que se encuentra la condición. Se representa como un desplazamiento de la primera columna (o fila).</span><span class="sxs-lookup"><span data-stu-id="06df7-p102">Represents the column (or row, depending on the sort orientation) that the condition is on. Represented as an offset from the first column (or row).</span></span>|
|<span data-ttu-id="06df7-121">sortOn</span><span class="sxs-lookup"><span data-stu-id="06df7-121">sortOn</span></span>|<span data-ttu-id="06df7-122">cadena</span><span class="sxs-lookup"><span data-stu-id="06df7-122">string</span></span>|<span data-ttu-id="06df7-123">Representa el tipo de ordenación de esta condición.</span><span class="sxs-lookup"><span data-stu-id="06df7-123">Represents the type of sorting of this condition. Possible values are: , , , .</span></span> <span data-ttu-id="06df7-124">Los valores posibles son: `Value`, `CellColor`, `FontColor` y `Icon`.</span><span class="sxs-lookup"><span data-stu-id="06df7-124">The possible values are `Value`, `CellColor`, `FontColor`, `Icon`, , , , , , , , or .</span></span>|
|<span data-ttu-id="06df7-125">icon</span><span class="sxs-lookup"><span data-stu-id="06df7-125">icon</span></span>|[<span data-ttu-id="06df7-126">WorkbookIcon</span><span class="sxs-lookup"><span data-stu-id="06df7-126">WorkbookIcon</span></span>](icon.md)|<span data-ttu-id="06df7-127">Representa el icono que es el destino de la condición si la ordenación se realiza según el icono de la celda.</span><span class="sxs-lookup"><span data-stu-id="06df7-127">Represents the icon that is the target of the condition if the sorting is on the cell's icon.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="06df7-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="06df7-128">JSON representation</span></span>

<span data-ttu-id="06df7-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="06df7-129">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookSortField"
}-->

```json
{
  "ascending": true,
  "color": "string",
  "dataOption": "string",
  "key": 1024,
  "sortOn": "string",
  "icon": { "@odata.type": "microsoft.graph.workbookIcon" }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "SortField resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->