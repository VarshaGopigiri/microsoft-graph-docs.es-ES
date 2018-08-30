# <a name="tablesort-resource-type"></a><span data-ttu-id="e1490-101">Tipo de recurso TableSort</span><span class="sxs-lookup"><span data-stu-id="e1490-101">TableSort resource type</span></span>

<span data-ttu-id="e1490-102">Administra operaciones de ordenación en objetos Table.</span><span class="sxs-lookup"><span data-stu-id="e1490-102">Manages sorting operations on Table objects.</span></span>


## <a name="methods"></a><span data-ttu-id="e1490-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1490-103">Methods</span></span>

| <span data-ttu-id="e1490-104">Método</span><span class="sxs-lookup"><span data-stu-id="e1490-104">Method</span></span>           | <span data-ttu-id="e1490-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1490-105">Return Type</span></span>    |<span data-ttu-id="e1490-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1490-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e1490-107">Get TableSort</span><span class="sxs-lookup"><span data-stu-id="e1490-107">Get TableSort</span></span>](../api/tablesort_get.md) | [<span data-ttu-id="e1490-108">WorkbookTableSort</span><span class="sxs-lookup"><span data-stu-id="e1490-108">WorkbookTableSort</span></span>](tablesort.md) |<span data-ttu-id="e1490-109">Lee las propiedades y relaciones del objeto tableSort.</span><span class="sxs-lookup"><span data-stu-id="e1490-109">Read properties and relationships of tableSort object.</span></span>|
|[<span data-ttu-id="e1490-110">Apply</span><span class="sxs-lookup"><span data-stu-id="e1490-110">Apply</span></span>](../api/tablesort_apply.md)|<span data-ttu-id="e1490-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e1490-111">None</span></span>|<span data-ttu-id="e1490-112">Realiza una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="e1490-112">Perform a sort operation.</span></span>|
|[<span data-ttu-id="e1490-113">Clear</span><span class="sxs-lookup"><span data-stu-id="e1490-113">Clear</span></span>](../api/tablesort_clear.md)|<span data-ttu-id="e1490-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e1490-114">None</span></span>|<span data-ttu-id="e1490-p101">Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e1490-p101">Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.</span></span>|
|[<span data-ttu-id="e1490-117">Reapply</span><span class="sxs-lookup"><span data-stu-id="e1490-117">Reapply</span></span>](../api/tablesort_reapply.md)|<span data-ttu-id="e1490-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e1490-118">None</span></span>|<span data-ttu-id="e1490-119">Vuelve a aplicar los parámetros de ordenación actuales a la tabla.</span><span class="sxs-lookup"><span data-stu-id="e1490-119">Reapplies the current sorting parameters to the table.</span></span>|

## <a name="properties"></a><span data-ttu-id="e1490-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1490-120">Properties</span></span>
| <span data-ttu-id="e1490-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e1490-121">Property</span></span>     | <span data-ttu-id="e1490-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1490-122">Type</span></span>   |<span data-ttu-id="e1490-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1490-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e1490-124">fields</span><span class="sxs-lookup"><span data-stu-id="e1490-124">fields</span></span>|<span data-ttu-id="e1490-125">Colección de [WorkbookSortField](sortfield.md)</span><span class="sxs-lookup"><span data-stu-id="e1490-125">[WorkbookSortField](sortfield.md) collection</span></span>|<span data-ttu-id="e1490-p102">Representa las condiciones actuales que se usaron por última vez para ordenar la tabla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1490-p102">Represents the current conditions used to last sort the table. Read-only.</span></span>|
|<span data-ttu-id="e1490-128">matchCase</span><span class="sxs-lookup"><span data-stu-id="e1490-128">matchCase</span></span>|<span data-ttu-id="e1490-129">booleano</span><span class="sxs-lookup"><span data-stu-id="e1490-129">boolean</span></span>|<span data-ttu-id="e1490-p103">Indica si última ordenación de la tabla distinguía mayúsculas de minúsculas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1490-p103">Represents whether the casing impacted the last sort of the table. Read-only.</span></span>|
|<span data-ttu-id="e1490-132">method</span><span class="sxs-lookup"><span data-stu-id="e1490-132">method</span></span>|<span data-ttu-id="e1490-133">cadena</span><span class="sxs-lookup"><span data-stu-id="e1490-133">string</span></span>|<span data-ttu-id="e1490-134">Representa el método utilizado por última vez para ordenar la tabla de orden de los caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="e1490-134">Represents Chinese character ordering method last used to sort the table. Possible values are: , . Read-only.</span></span> <span data-ttu-id="e1490-135">Los valores posibles son: `PinYin` y `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="e1490-135">The possible values are:</span></span> <span data-ttu-id="e1490-136">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e1490-136">Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e1490-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e1490-137">JSON representation</span></span>

<span data-ttu-id="e1490-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e1490-138">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTableSort"
}-->

```json
{
  "matchCase": true,
  "method": "string",
  "fields": [{ "@odata.type": "microsoft.graph.workbookSortField" }]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableSort resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->