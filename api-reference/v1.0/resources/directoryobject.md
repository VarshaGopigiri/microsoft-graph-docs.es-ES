# <a name="directoryobject-resource-type"></a><span data-ttu-id="ef765-101">Tipo de recurso directoryObject</span><span class="sxs-lookup"><span data-stu-id="ef765-101">directoryObject resource type</span></span>

<span data-ttu-id="ef765-p101">Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.</span><span class="sxs-lookup"><span data-stu-id="ef765-p101">Represents an Azure Active Directory object. The **directoryObject** type is the base type for many other directory entity types.</span></span>

## <a name="methods"></a><span data-ttu-id="ef765-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef765-104">Methods</span></span>

| <span data-ttu-id="ef765-105">Método</span><span class="sxs-lookup"><span data-stu-id="ef765-105">Method</span></span>       | <span data-ttu-id="ef765-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef765-106">Return Type</span></span>  |<span data-ttu-id="ef765-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef765-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ef765-108">Get directoryObject</span><span class="sxs-lookup"><span data-stu-id="ef765-108">Get directoryObject</span></span>](../api/directoryobject_get.md) | [<span data-ttu-id="ef765-109">directoryObject</span><span class="sxs-lookup"><span data-stu-id="ef765-109">directoryObject</span></span>](directoryobject.md) |<span data-ttu-id="ef765-110">Lee las propiedades de un objeto directory.</span><span class="sxs-lookup"><span data-stu-id="ef765-110">Read the properties  of a directory object.</span></span>|
|[<span data-ttu-id="ef765-111">Delete directoryObject</span><span class="sxs-lookup"><span data-stu-id="ef765-111">Delete directoryObject</span></span>](../api/directoryobject_delete.md) | <span data-ttu-id="ef765-112">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ef765-112">None</span></span> |<span data-ttu-id="ef765-113">Elimina un objeto directory.</span><span class="sxs-lookup"><span data-stu-id="ef765-113">Delete a directory object.</span></span> |
|[<span data-ttu-id="ef765-114">checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="ef765-114">checkMemberGroups</span></span>](../api/directoryobject_checkmembergroups.md)|<span data-ttu-id="ef765-115">Colección string</span><span class="sxs-lookup"><span data-stu-id="ef765-115">String collection</span></span>|<span data-ttu-id="ef765-p102">Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="ef765-p102">Check for membership in a list of groups. The check is transitive.</span></span>|
|[<span data-ttu-id="ef765-118">getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="ef765-118">getMemberGroups</span></span>](../api/directoryobject_getmembergroups.md)|<span data-ttu-id="ef765-119">Colección string</span><span class="sxs-lookup"><span data-stu-id="ef765-119">String collection</span></span>|<span data-ttu-id="ef765-p103">Devuelve todos los grupos de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="ef765-p103">Return all the groups that the user, group, or directory object is a member of. The check is transitive.</span></span>|
|[<span data-ttu-id="ef765-122">getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="ef765-122">getMemberObjects</span></span>](../api/directoryobject_getmemberobjects.md)|<span data-ttu-id="ef765-123">Colección string</span><span class="sxs-lookup"><span data-stu-id="ef765-123">String collection</span></span>| <span data-ttu-id="ef765-p104">Devuelve todos los grupos y roles de directorio de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="ef765-p104">Return all of the groups and directory roles that the user, group, or directory object is a member of. The check is transitive.</span></span> |
|[<span data-ttu-id="ef765-126">getByIds</span><span class="sxs-lookup"><span data-stu-id="ef765-126">getByIds</span></span>](../api/directoryobject_getbyids.md) | <span data-ttu-id="ef765-127">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="ef765-127">[directoryObject](directoryobject.md) collection</span></span> | <span data-ttu-id="ef765-128">Obtenga un conjunto de objetos de directorio basados en un conjunto de identificadores proporcionados.</span><span class="sxs-lookup"><span data-stu-id="ef765-128">Get a set of directory objects based on a set of supplied ids.</span></span> |

## <a name="properties"></a><span data-ttu-id="ef765-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef765-129">Properties</span></span>

| <span data-ttu-id="ef765-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ef765-130">Property</span></span>   | <span data-ttu-id="ef765-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef765-131">Type</span></span> |<span data-ttu-id="ef765-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef765-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ef765-133">id</span><span class="sxs-lookup"><span data-stu-id="ef765-133">id</span></span>|<span data-ttu-id="ef765-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ef765-134">String</span></span>|<span data-ttu-id="ef765-p105">Guid que es el identificador único para el objeto; por ejemplo, 12345678-9abc-def0-1234-56789abcde. Clave. No admite valores NULL. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ef765-p105">A Guid that is the unique identifier for the object; for example, 12345678-9abc-def0-1234-56789abcde. Key. Not nullable. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ef765-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ef765-139">Relationships</span></span>

<span data-ttu-id="ef765-140">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ef765-140">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="ef765-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ef765-141">JSON representation</span></span>

<span data-ttu-id="ef765-142">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ef765-142">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directoryObject",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
