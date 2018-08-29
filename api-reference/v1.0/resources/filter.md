# <a name="filter-resource-type"></a><span data-ttu-id="8c46b-101">Tipo de recurso Filter</span><span class="sxs-lookup"><span data-stu-id="8c46b-101">Filter resource type</span></span>

<span data-ttu-id="8c46b-102">Administra el filtrado de la columna de una tabla.</span><span class="sxs-lookup"><span data-stu-id="8c46b-102">Manages the filtering of a table's column.</span></span>


## <a name="methods"></a><span data-ttu-id="8c46b-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="8c46b-103">Methods</span></span>

| <span data-ttu-id="8c46b-104">Método</span><span class="sxs-lookup"><span data-stu-id="8c46b-104">Method</span></span>           | <span data-ttu-id="8c46b-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c46b-105">Return Type</span></span>    |<span data-ttu-id="8c46b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c46b-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="8c46b-107">Apply</span><span class="sxs-lookup"><span data-stu-id="8c46b-107">Apply</span></span>](../api/filter_apply.md)|<span data-ttu-id="8c46b-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8c46b-108">None</span></span>|<span data-ttu-id="8c46b-109">Aplica los criterios de filtro especificados en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="8c46b-109">Apply the given filter criteria on the given column.</span></span>|
|[<span data-ttu-id="8c46b-110">Clear</span><span class="sxs-lookup"><span data-stu-id="8c46b-110">Clear</span></span>](../api/filter_clear.md)|<span data-ttu-id="8c46b-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8c46b-111">None</span></span>|<span data-ttu-id="8c46b-112">Borra el filtro de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="8c46b-112">Clear the filter on the given column.</span></span>|

## <a name="properties"></a><span data-ttu-id="8c46b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c46b-113">Properties</span></span>

| <span data-ttu-id="8c46b-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="8c46b-114">Name</span></span> | <span data-ttu-id="8c46b-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c46b-115">Type</span></span>   |<span data-ttu-id="8c46b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c46b-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8c46b-117">criteria</span><span class="sxs-lookup"><span data-stu-id="8c46b-117">criteria</span></span>|[<span data-ttu-id="8c46b-118">WorkbookFilterCriteria</span><span class="sxs-lookup"><span data-stu-id="8c46b-118">WorkbookFilterCriteria</span></span>](filtercriteria.md)|<span data-ttu-id="8c46b-p101">Filtro aplicado actualmente en la columna especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8c46b-p101">The currently applied filter on the given column. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8c46b-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8c46b-121">JSON representation</span></span>

<span data-ttu-id="8c46b-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8c46b-122">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilter"
}-->

```json
{
  "criteria": {"@odata.type": "microsoft.graph.workbookFilterCriteria" }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Filter resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->