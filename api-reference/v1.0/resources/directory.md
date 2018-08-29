# <a name="directory-resource-type-deleted-items"></a><span data-ttu-id="a2f44-101">Tipo de recurso directory (elementos eliminados)</span><span class="sxs-lookup"><span data-stu-id="a2f44-101">directory resource type (deleted items)</span></span>

<span data-ttu-id="a2f44-102">Representa un elemento eliminado en el directorio.</span><span class="sxs-lookup"><span data-stu-id="a2f44-102">Represents a deleted item in the directory.</span></span> <span data-ttu-id="a2f44-103">Cuando se elimina un elemento, se agrega al "contenedor" de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="a2f44-103">When an item is deleted, it is added to the deleted items "container".</span></span> <span data-ttu-id="a2f44-104">Los elementos eliminados seguirán estando disponible para su restauración durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="a2f44-104">Deleted items will remain available to restore for up to 30 days.</span></span> <span data-ttu-id="a2f44-105">Después de 30 días, los elementos se eliminan permanentemente.</span><span class="sxs-lookup"><span data-stu-id="a2f44-105">After 30 days, the items are permanently deleted.</span></span>

<span data-ttu-id="a2f44-106">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los [grupos](group.md) y [usuarios](users.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="a2f44-106">Currently, deleted items functionality is only supported for Office 365 [groups](group.md) and [users](users.md).</span></span>

## <a name="methods"></a><span data-ttu-id="a2f44-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2f44-107">Methods</span></span>

| <span data-ttu-id="a2f44-108">Método</span><span class="sxs-lookup"><span data-stu-id="a2f44-108">Method</span></span>         | <span data-ttu-id="a2f44-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2f44-109">Return Type</span></span> | <span data-ttu-id="a2f44-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2f44-110">Description</span></span> |
|:---------------|:------------|:------------|
|[<span data-ttu-id="a2f44-111">Obtener elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="a2f44-111">Get deleted item</span></span>](../api/directory_deleteditems_get.md) | [<span data-ttu-id="a2f44-112">directoryObject</span><span class="sxs-lookup"><span data-stu-id="a2f44-112">directoryObject</span></span>](directoryobject.md) | <span data-ttu-id="a2f44-113">Obtiene las propiedades de un elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="a2f44-113">Gets the properties of a deleted item.</span></span> |
|[<span data-ttu-id="a2f44-114">Restaurar elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="a2f44-114">Restore deleted item</span></span>](../api/directory_deleteditems_restore.md) |[<span data-ttu-id="a2f44-115">directoryObject</span><span class="sxs-lookup"><span data-stu-id="a2f44-115">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="a2f44-116">Restaura un elemento eliminado recientemente.</span><span class="sxs-lookup"><span data-stu-id="a2f44-116">Restores a recently deleted item.</span></span> |
|[<span data-ttu-id="a2f44-117">Enumerar elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="a2f44-117">List deleted items</span></span>](../api/directory_deleteditems_list.md) |<span data-ttu-id="a2f44-118">Colección de [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="a2f44-118">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="a2f44-119">Obtiene una lista de elementos eliminados recientemente.</span><span class="sxs-lookup"><span data-stu-id="a2f44-119">Gets a list of recently deleted items.</span></span> |
|[<span data-ttu-id="a2f44-120">Eliminar permanentemente un elemento</span><span class="sxs-lookup"><span data-stu-id="a2f44-120">Permanently delete an item</span></span>](../api/directory_deleteditems_delete.md) | <span data-ttu-id="a2f44-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a2f44-121">None</span></span> | <span data-ttu-id="a2f44-122">Elimina permanentemente un elemento.</span><span class="sxs-lookup"><span data-stu-id="a2f44-122">Permanently deletes an item.</span></span> |
|<span data-ttu-id="a2f44-123">[Lista de los elementos eliminados que pertenecen a un usuario](../api/directory_deleteditems_user_owned.md)</span><span class="sxs-lookup"><span data-stu-id="a2f44-123">Added [List deleted items owned by a user](../api/directory_deleteditems_user_owned.md) action to directory (deleted items) resource</span></span> | <span data-ttu-id="a2f44-124">Colección de [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="a2f44-124">[directoryObject](directoryobject.md) collection</span></span> | <span data-ttu-id="a2f44-125">Se enumeran los elementos del directorio que pertenecen a un usuario.</span><span class="sxs-lookup"><span data-stu-id="a2f44-125">Lists directory items owned by a user.</span></span> |

## <a name="relationships"></a><span data-ttu-id="a2f44-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a2f44-126">Relationships</span></span>
| <span data-ttu-id="a2f44-127">Relación</span><span class="sxs-lookup"><span data-stu-id="a2f44-127">Relationship</span></span> | <span data-ttu-id="a2f44-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2f44-128">Type</span></span>   |<span data-ttu-id="a2f44-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2f44-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a2f44-130">deleteditems</span><span class="sxs-lookup"><span data-stu-id="a2f44-130">deleteditems</span></span>|<span data-ttu-id="a2f44-131">Colección de [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="a2f44-131">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="a2f44-132">Elementos eliminados recientemente</span><span class="sxs-lookup"><span data-stu-id="a2f44-132">Recently deleted items.</span></span> <span data-ttu-id="a2f44-133">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2f44-133">Read-only.</span></span> <span data-ttu-id="a2f44-134">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="a2f44-134">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a2f44-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a2f44-135">JSON representation</span></span>
<span data-ttu-id="a2f44-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a2f44-136">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
}
```

## <a name="example"></a><span data-ttu-id="a2f44-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2f44-137">Example</span></span>

<!--{"blockType": "request"}-->
```http
GET https://graph.microsoft.com/v1.0/directory
```

<!--{"blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.directory"}-->
```json
HTTP/1.1 200 OK
Content-Type: application/json

{
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