# <a name="directory-resource-type-deleted-items"></a><span data-ttu-id="b4da0-101">Tipo de recurso directory (elementos eliminados)</span><span class="sxs-lookup"><span data-stu-id="b4da0-101">directory resource type (deleted items)</span></span>

<span data-ttu-id="b4da0-102">Representa un elemento eliminado en el directorio.</span><span class="sxs-lookup"><span data-stu-id="b4da0-102">Represents a deleted item in the directory.</span></span> <span data-ttu-id="b4da0-103">Cuando se elimina un elemento, se agrega al "contenedor" de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b4da0-103">When an item is deleted, it is added to the deleted items "container".</span></span> <span data-ttu-id="b4da0-104">Los elementos eliminados seguirán estando disponible para su restauración durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="b4da0-104">Deleted items will remain available to restore for up to 30 days.</span></span> <span data-ttu-id="b4da0-105">Después de 30 días, los elementos se eliminan permanentemente.</span><span class="sxs-lookup"><span data-stu-id="b4da0-105">After 30 days, the items are permanently deleted.</span></span>

<span data-ttu-id="b4da0-106">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los [grupos](group.md) y [usuarios](users.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="b4da0-106">Currently, deleted items functionality is only supported for Office 365 [groups](group.md) and [users](users.md).</span></span>

## <a name="methods"></a><span data-ttu-id="b4da0-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4da0-107">Methods</span></span>

| <span data-ttu-id="b4da0-108">Método</span><span class="sxs-lookup"><span data-stu-id="b4da0-108">Method</span></span>         | <span data-ttu-id="b4da0-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4da0-109">Return Type</span></span> | <span data-ttu-id="b4da0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4da0-110">Description</span></span> |
|:---------------|:------------|:------------|
|[<span data-ttu-id="b4da0-111">Obtener elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="b4da0-111">Get deleted item</span></span>](../api/directory_deleteditems_get.md) | [<span data-ttu-id="b4da0-112">directoryObject</span><span class="sxs-lookup"><span data-stu-id="b4da0-112">directoryObject</span></span>](directoryobject.md) | <span data-ttu-id="b4da0-113">Obtiene las propiedades de un elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="b4da0-113">Gets the properties of a deleted item.</span></span> |
|[<span data-ttu-id="b4da0-114">Restaurar elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="b4da0-114">Restore deleted item</span></span>](../api/directory_deleteditems_restore.md) |[<span data-ttu-id="b4da0-115">directoryObject</span><span class="sxs-lookup"><span data-stu-id="b4da0-115">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="b4da0-116">Restaura un elemento eliminado recientemente.</span><span class="sxs-lookup"><span data-stu-id="b4da0-116">Restores a recently deleted item.</span></span> |
|[<span data-ttu-id="b4da0-117">Enumerar elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="b4da0-117">List deleted items</span></span>](../api/directory_deleteditems_list.md) |<span data-ttu-id="b4da0-118">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="b4da0-118">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="b4da0-119">Obtiene una lista de elementos eliminados recientemente.</span><span class="sxs-lookup"><span data-stu-id="b4da0-119">Gets a list of recently deleted items.</span></span> |
|[<span data-ttu-id="b4da0-120">Eliminar permanentemente un elemento</span><span class="sxs-lookup"><span data-stu-id="b4da0-120">Permanently delete an item</span></span>](../api/directory_deleteditems_delete.md) | <span data-ttu-id="b4da0-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b4da0-121">None</span></span> | <span data-ttu-id="b4da0-122">Elimina permanentemente un elemento.</span><span class="sxs-lookup"><span data-stu-id="b4da0-122">Permanently deletes an item.</span></span> |

## <a name="properties"></a><span data-ttu-id="b4da0-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4da0-123">Properties</span></span>
| <span data-ttu-id="b4da0-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4da0-124">Property</span></span>   | <span data-ttu-id="b4da0-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4da0-125">Type</span></span> |<span data-ttu-id="b4da0-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4da0-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b4da0-127">id</span><span class="sxs-lookup"><span data-stu-id="b4da0-127">id</span></span>|<span data-ttu-id="b4da0-128">String</span><span class="sxs-lookup"><span data-stu-id="b4da0-128">String</span></span>| <span data-ttu-id="b4da0-129">Identificador único del objeto; por ejemplo, 12345678-9abc-def0-1234-56789abcde.</span><span class="sxs-lookup"><span data-stu-id="b4da0-129">A Guid that is the unique identifier for the object; for example, 12345678-9abc-def0-1234-56789abcde. Key. Not nullable. Read-only.</span></span> <span data-ttu-id="b4da0-130">Clave.</span><span class="sxs-lookup"><span data-stu-id="b4da0-130">Key</span></span> <span data-ttu-id="b4da0-131">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="b4da0-131">Not nullable.</span></span> <span data-ttu-id="b4da0-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b4da0-132">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b4da0-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b4da0-133">Relationships</span></span>
| <span data-ttu-id="b4da0-134">Relación</span><span class="sxs-lookup"><span data-stu-id="b4da0-134">Relationship</span></span> | <span data-ttu-id="b4da0-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4da0-135">Type</span></span>   |<span data-ttu-id="b4da0-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4da0-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b4da0-137">deleteditems</span><span class="sxs-lookup"><span data-stu-id="b4da0-137">deleteditems</span></span>|<span data-ttu-id="b4da0-138">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="b4da0-138">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="b4da0-139">Elementos eliminados recientemente</span><span class="sxs-lookup"><span data-stu-id="b4da0-139">Recently deleted items.</span></span> <span data-ttu-id="b4da0-140">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b4da0-140">Read-only.</span></span> <span data-ttu-id="b4da0-141">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="b4da0-141">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b4da0-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b4da0-142">JSON representation</span></span>
<span data-ttu-id="b4da0-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b4da0-143">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
  "id": "String (identifier)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directory resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->