# <a name="nameditem-resource-type"></a><span data-ttu-id="d7200-101">Tipo de recurso NamedItem</span><span class="sxs-lookup"><span data-stu-id="d7200-101">NamedItem resource type</span></span>

<span data-ttu-id="d7200-p101">Representa un nombre definido para un rango de celdas o un valor. Los nombres pueden ser objetos primitivos con nombre (como puede verse en el tipo siguiente), un objeto de rango o una referencia a un rango. Este objeto puede usarse para obtener un objeto de rango asociado a nombres.</span><span class="sxs-lookup"><span data-stu-id="d7200-p101">Represents a defined name for a range of cells or value. Names can be primitive named objects (as seen in the type below), range object, reference to a range. This object can be used to obtain range object associated with names.</span></span>


## <a name="methods"></a><span data-ttu-id="d7200-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7200-105">Methods</span></span>

| <span data-ttu-id="d7200-106">Método</span><span class="sxs-lookup"><span data-stu-id="d7200-106">Method</span></span>           | <span data-ttu-id="d7200-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7200-107">Return Type</span></span>    |<span data-ttu-id="d7200-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7200-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d7200-109">Add</span><span class="sxs-lookup"><span data-stu-id="d7200-109">Add</span></span>](../api/nameditem_add.md)|[<span data-ttu-id="d7200-110">NamedItem</span><span class="sxs-lookup"><span data-stu-id="d7200-110">NamedItem</span></span>](nameditem.md)|<span data-ttu-id="d7200-111">Agrega un nuevo nombre a la colección del ámbito especificado.</span><span class="sxs-lookup"><span data-stu-id="d7200-111">Adds a new name to the collection of the given scope.</span></span>|
|[<span data-ttu-id="d7200-112">AddFormulaLocal</span><span class="sxs-lookup"><span data-stu-id="d7200-112">AddFormulaLocal</span></span>](../api/nameditem_addformulalocal.md)|[<span data-ttu-id="d7200-113">NamedItem</span><span class="sxs-lookup"><span data-stu-id="d7200-113">NamedItem</span></span>](nameditem.md)|<span data-ttu-id="d7200-114">Agrega un nuevo nombre a la colección del ámbito especificado empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="d7200-114">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>|
|[<span data-ttu-id="d7200-115">Get NamedItem</span><span class="sxs-lookup"><span data-stu-id="d7200-115">Get NamedItem</span></span>](../api/nameditem_get.md) | [<span data-ttu-id="d7200-116">NamedItem</span><span class="sxs-lookup"><span data-stu-id="d7200-116">NamedItem</span></span>](nameditem.md) |<span data-ttu-id="d7200-117">Lee las propiedades y relaciones del objeto namedItem.</span><span class="sxs-lookup"><span data-stu-id="d7200-117">Read properties and relationships of namedItem object.</span></span>|
|[<span data-ttu-id="d7200-118">Update</span><span class="sxs-lookup"><span data-stu-id="d7200-118">Update</span></span>](../api/nameditem_update.md) | [<span data-ttu-id="d7200-119">NamedItem</span><span class="sxs-lookup"><span data-stu-id="d7200-119">NamedItem</span></span>](nameditem.md)   |<span data-ttu-id="d7200-120">Actualiza el objeto NamedItem.</span><span class="sxs-lookup"><span data-stu-id="d7200-120">Update NamedItem object.</span></span> |
|[<span data-ttu-id="d7200-121">Range</span><span class="sxs-lookup"><span data-stu-id="d7200-121">Range</span></span>](../api/nameditem_range.md)|[<span data-ttu-id="d7200-122">Range</span><span class="sxs-lookup"><span data-stu-id="d7200-122">Range</span></span>](range.md)|<span data-ttu-id="d7200-p102">Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un rango.</span><span class="sxs-lookup"><span data-stu-id="d7200-p102">Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.</span></span>|
|[<span data-ttu-id="d7200-125">List</span><span class="sxs-lookup"><span data-stu-id="d7200-125">List</span></span>](../api/nameditem_list.md) | <span data-ttu-id="d7200-126">Colección [NamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="d7200-126">[NamedItem](nameditem.md) collection</span></span> |<span data-ttu-id="d7200-127">Obtiene la colección de objetos namedItem.</span><span class="sxs-lookup"><span data-stu-id="d7200-127">Get namedItem object collection.</span></span> |

## <a name="properties"></a><span data-ttu-id="d7200-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7200-128">Properties</span></span>
| <span data-ttu-id="d7200-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7200-129">Property</span></span>     | <span data-ttu-id="d7200-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7200-130">Type</span></span>   |<span data-ttu-id="d7200-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7200-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d7200-132">name</span><span class="sxs-lookup"><span data-stu-id="d7200-132">name</span></span>|<span data-ttu-id="d7200-133">string</span><span class="sxs-lookup"><span data-stu-id="d7200-133">string</span></span>|<span data-ttu-id="d7200-p103">Nombre del objeto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7200-p103">The name of the object. Read-only.</span></span>|
|<span data-ttu-id="d7200-136">comment</span><span class="sxs-lookup"><span data-stu-id="d7200-136">comment</span></span>|<span data-ttu-id="d7200-137">string</span><span class="sxs-lookup"><span data-stu-id="d7200-137">string</span></span>|<span data-ttu-id="d7200-138">Representa el comentario asociado a este nombre.</span><span class="sxs-lookup"><span data-stu-id="d7200-138">Represents the comment associated with this name.</span></span>|
|<span data-ttu-id="d7200-139">scope</span><span class="sxs-lookup"><span data-stu-id="d7200-139">scope</span></span>|<span data-ttu-id="d7200-140">string</span><span class="sxs-lookup"><span data-stu-id="d7200-140">string</span></span>|<span data-ttu-id="d7200-p104">Indica si el nombre está en el ámbito del libro o de una hoja de cálculo específica. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7200-p104">Indicates whether the name is scoped to the workbook or to a specific worksheet. Read-only.</span></span>|
|<span data-ttu-id="d7200-143">type</span><span class="sxs-lookup"><span data-stu-id="d7200-143">type</span></span>|<span data-ttu-id="d7200-144">string</span><span class="sxs-lookup"><span data-stu-id="d7200-144">string</span></span>|<span data-ttu-id="d7200-p105">Indica el tipo de referencia que está asociado al nombre. Valores posibles: `String`, `Integer`, `Double`, `Boolean`, `Range`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7200-p105">Indicates what type of reference is associated with the name. Possible values are: `String`, `Integer`, `Double`, `Boolean`, `Range`. Read-only.</span></span>|
|<span data-ttu-id="d7200-148">value</span><span class="sxs-lookup"><span data-stu-id="d7200-148">value</span></span>|<span data-ttu-id="d7200-149">object</span><span class="sxs-lookup"><span data-stu-id="d7200-149">object</span></span>|<span data-ttu-id="d7200-p106">Representa la fórmula a la que debe hacer referencia el nombre, según su definición. Por ejemplo =Sheet14!$B$2:$H$12, =4.75, etc. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7200-p106">Represents the formula that the name is defined to refer to. E.g. =Sheet14!$B$2:$H$12, =4.75, etc. Read-only.</span></span>|
|<span data-ttu-id="d7200-153">visible</span><span class="sxs-lookup"><span data-stu-id="d7200-153">visible</span></span>|<span data-ttu-id="d7200-154">boolean</span><span class="sxs-lookup"><span data-stu-id="d7200-154">boolean</span></span>|<span data-ttu-id="d7200-155">Especifica si el objeto está visible o no.</span><span class="sxs-lookup"><span data-stu-id="d7200-155">Specifies whether the object is visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d7200-156">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d7200-156">Relationships</span></span>
| <span data-ttu-id="d7200-157">Relación</span><span class="sxs-lookup"><span data-stu-id="d7200-157">Relationship</span></span>     | <span data-ttu-id="d7200-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7200-158">Type</span></span>   |<span data-ttu-id="d7200-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7200-159">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d7200-160">worksheet</span><span class="sxs-lookup"><span data-stu-id="d7200-160">worksheet</span></span>|[<span data-ttu-id="d7200-161">worksheet</span><span class="sxs-lookup"><span data-stu-id="d7200-161">worksheet</span></span>](worksheet.md)|<span data-ttu-id="d7200-p107">Devuelve la hoja de cálculo que tiene como ámbito el elemento con nombre. Solo está disponible si el elemento tiene como ámbito la hoja de cálculo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7200-p107">Returns the worksheet on which the named item is scoped to. Available only if the item is scoped to the worksheet. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d7200-165">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d7200-165">JSON representation</span></span>

<span data-ttu-id="d7200-166">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d7200-166">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.namedItem"
}-->

```json
{
  "name": "string",
  "comment": "string",
  "scope": "string",
  "type": "string",
  "value": {"@odata.type": "microsoft.graph.range"},
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
