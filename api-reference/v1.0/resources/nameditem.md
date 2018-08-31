# <a name="nameditem-resource-type"></a><span data-ttu-id="bfcfc-101">Tipo de recurso NamedItem</span><span class="sxs-lookup"><span data-stu-id="bfcfc-101">NamedItem resource type</span></span>

<span data-ttu-id="bfcfc-p101">Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-p101">Represents a defined name for a range of cells or value. Names can be primitive named objects (as seen in the type below), range object, reference to a range. This object can be used to obtain range object associated with names.</span></span>


## <a name="methods"></a><span data-ttu-id="bfcfc-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="bfcfc-105">Methods</span></span>

| <span data-ttu-id="bfcfc-106">Método</span><span class="sxs-lookup"><span data-stu-id="bfcfc-106">Method</span></span>           | <span data-ttu-id="bfcfc-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfcfc-107">Return Type</span></span>    |<span data-ttu-id="bfcfc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfcfc-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bfcfc-109">Add</span><span class="sxs-lookup"><span data-stu-id="bfcfc-109">Add</span></span>](../api/nameditem_add.md)|[<span data-ttu-id="bfcfc-110">WorkbookNamedItem</span><span class="sxs-lookup"><span data-stu-id="bfcfc-110">WorkbookNamedItem</span></span>](nameditem.md)|<span data-ttu-id="bfcfc-111">Agrega un nuevo nombre a la colección del ámbito especificado.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-111">Adds a new name to the collection of the given scope.</span></span>|
|[<span data-ttu-id="bfcfc-112">AddFormulaLocal</span><span class="sxs-lookup"><span data-stu-id="bfcfc-112">AddFormulaLocal</span></span>](../api/nameditem_addformulalocal.md)|[<span data-ttu-id="bfcfc-113">WorkbookNamedItem</span><span class="sxs-lookup"><span data-stu-id="bfcfc-113">WorkbookNamedItem</span></span>](nameditem.md)|<span data-ttu-id="bfcfc-114">Agrega un nuevo nombre a la colección del ámbito especificado empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-114">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>|
|[<span data-ttu-id="bfcfc-115">Get NamedItem</span><span class="sxs-lookup"><span data-stu-id="bfcfc-115">Get NamedItem</span></span>](../api/nameditem_get.md) | [<span data-ttu-id="bfcfc-116">WorkbookNamedItem</span><span class="sxs-lookup"><span data-stu-id="bfcfc-116">WorkbookNamedItem</span></span>](nameditem.md) |<span data-ttu-id="bfcfc-117">Lee las propiedades y relaciones del objeto namedItem.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-117">Read properties and relationships of namedItem object.</span></span>|
|[<span data-ttu-id="bfcfc-118">Update</span><span class="sxs-lookup"><span data-stu-id="bfcfc-118">Update</span></span>](../api/nameditem_update.md) | [<span data-ttu-id="bfcfc-119">WorkbookNamedItem</span><span class="sxs-lookup"><span data-stu-id="bfcfc-119">WorkbookNamedItem</span></span>](nameditem.md)   |<span data-ttu-id="bfcfc-120">Actualiza el objeto NamedItem.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-120">Update NamedItem object.</span></span> |
|[<span data-ttu-id="bfcfc-121">Range</span><span class="sxs-lookup"><span data-stu-id="bfcfc-121">Range</span></span>](../api/nameditem_range.md)|[<span data-ttu-id="bfcfc-122">Range</span><span class="sxs-lookup"><span data-stu-id="bfcfc-122">Range</span></span>](range.md)|<span data-ttu-id="bfcfc-p102">Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-p102">Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.</span></span>|
|[<span data-ttu-id="bfcfc-125">List</span><span class="sxs-lookup"><span data-stu-id="bfcfc-125">List</span></span>](../api/nameditem_list.md) | <span data-ttu-id="bfcfc-126">Colección de [WorkbookNamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="bfcfc-126">[WorkbookNamedItem](nameditem.md) collection</span></span> |<span data-ttu-id="bfcfc-127">Obtiene la colección de objetos namedItem.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-127">Get namedItem object collection.</span></span> |

## <a name="properties"></a><span data-ttu-id="bfcfc-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfcfc-128">Properties</span></span>
| <span data-ttu-id="bfcfc-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfcfc-129">Property</span></span>     | <span data-ttu-id="bfcfc-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfcfc-130">Type</span></span>   |<span data-ttu-id="bfcfc-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfcfc-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bfcfc-132">name</span><span class="sxs-lookup"><span data-stu-id="bfcfc-132">name</span></span>|<span data-ttu-id="bfcfc-133">cadena</span><span class="sxs-lookup"><span data-stu-id="bfcfc-133">string</span></span>|<span data-ttu-id="bfcfc-p103">Nombre del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-p103">The name of the object. Read-only.</span></span>|
|<span data-ttu-id="bfcfc-136">comment</span><span class="sxs-lookup"><span data-stu-id="bfcfc-136">comment</span></span>|<span data-ttu-id="bfcfc-137">cadena</span><span class="sxs-lookup"><span data-stu-id="bfcfc-137">string</span></span>|<span data-ttu-id="bfcfc-138">Representa el comentario asociado a este nombre.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-138">Represents the comment associated with this name.</span></span>|
|<span data-ttu-id="bfcfc-139">scope</span><span class="sxs-lookup"><span data-stu-id="bfcfc-139">scope</span></span>|<span data-ttu-id="bfcfc-140">cadena</span><span class="sxs-lookup"><span data-stu-id="bfcfc-140">string</span></span>|<span data-ttu-id="bfcfc-p104">Indica si el nombre está en el ámbito del libro o de una hoja de cálculo específica. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-p104">Indicates whether the name is scoped to the workbook or to a specific worksheet. Read-only.</span></span>|
|<span data-ttu-id="bfcfc-143">type</span><span class="sxs-lookup"><span data-stu-id="bfcfc-143">type</span></span>|<span data-ttu-id="bfcfc-144">cadena</span><span class="sxs-lookup"><span data-stu-id="bfcfc-144">string</span></span>|<span data-ttu-id="bfcfc-145">Indica qué tipo de referencia está asociado con el nombre.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-145">Indicates what type of reference is associated with the name. Possible values are: , , , , . Read-only.</span></span> <span data-ttu-id="bfcfc-146">Los valores posibles son: `String`, `Integer`, `Double`, `Boolean` y `Range`.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-146">The possible values are `String`, `Integer`, `Double`, `Boolean`, `Range`, , , , , , , or .</span></span> <span data-ttu-id="bfcfc-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-147">Read-only.</span></span>|
|<span data-ttu-id="bfcfc-148">value</span><span class="sxs-lookup"><span data-stu-id="bfcfc-148">value</span></span>|<span data-ttu-id="bfcfc-149">Json</span><span class="sxs-lookup"><span data-stu-id="bfcfc-149">Json</span></span>|<span data-ttu-id="bfcfc-p106">Representa la fórmula a la que debe hacer referencia el nombre, según su definición. Por ejemplo =Sheet14!$B$2:$H$12, =4.75, etc. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-p106">Represents the formula that the name is defined to refer to. E.g. =Sheet14!$B$2:$H$12, =4.75, etc. Read-only.</span></span>|
|<span data-ttu-id="bfcfc-153">visible</span><span class="sxs-lookup"><span data-stu-id="bfcfc-153">visible</span></span>|<span data-ttu-id="bfcfc-154">booleano</span><span class="sxs-lookup"><span data-stu-id="bfcfc-154">boolean</span></span>|<span data-ttu-id="bfcfc-155">Especifica si el objeto está visible o no.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-155">Specifies whether the object is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bfcfc-156">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bfcfc-156">Relationships</span></span>
| <span data-ttu-id="bfcfc-157">Relación</span><span class="sxs-lookup"><span data-stu-id="bfcfc-157">Relationship</span></span>     | <span data-ttu-id="bfcfc-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfcfc-158">Type</span></span>   |<span data-ttu-id="bfcfc-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfcfc-159">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bfcfc-160">worksheet</span><span class="sxs-lookup"><span data-stu-id="bfcfc-160">worksheet</span></span>|[<span data-ttu-id="bfcfc-161">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="bfcfc-161">WorkbookWorksheet</span></span>](worksheet.md)|<span data-ttu-id="bfcfc-p107">Devuelve la hoja de cálculo que tiene como ámbito el elemento con nombre. Solo está disponible si el elemento tiene como ámbito la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-p107">Returns the worksheet on which the named item is scoped to. Available only if the item is scoped to the worksheet. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="bfcfc-165">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bfcfc-165">JSON representation</span></span>

<span data-ttu-id="bfcfc-166">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-166">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookNamedItem"
}-->

```json
{
  "name": "string",
  "comment": "string",
  "scope": "string",
  "type": "string",
  "value": {"@odata.type": "microsoft.graph.Json"},
  "visible": true
  
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
