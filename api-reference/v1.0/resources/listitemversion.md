# <a name="listitemversion-resource-type"></a><span data-ttu-id="6d2a7-101">Tipo de recurso ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="6d2a7-101">ListItemVersion resource type</span></span>

<span data-ttu-id="6d2a7-102">El recurso **listItemVersion** representa una versión anterior de un recurso [ListItem](listitem.md).</span><span class="sxs-lookup"><span data-stu-id="6d2a7-102">The **listItemVersion** resource represents a previous version of a [ListItem](listitem.md) resource.</span></span>

## <a name="tasks-on-listitemversion-resources"></a><span data-ttu-id="6d2a7-103">Tareas en recursos ListItemVersion</span><span class="sxs-lookup"><span data-stu-id="6d2a7-103">Tasks on ListItemVersion resources</span></span>

<span data-ttu-id="6d2a7-104">Las tareas siguientes están disponibles para los recursos listItemVersion.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-104">The following tasks are available for listItemVersion resources.</span></span>

|            <span data-ttu-id="6d2a7-105">Tarea común</span><span class="sxs-lookup"><span data-stu-id="6d2a7-105">Common task</span></span>             |         <span data-ttu-id="6d2a7-106">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="6d2a7-106">HTTP method</span></span>         |
| :--------------------------------- | :-------------------------- |
| <span data-ttu-id="6d2a7-107">[Enumerar versiones][version-list]</span><span class="sxs-lookup"><span data-stu-id="6d2a7-107">[List versions][version-list]</span></span>      | `GET /sites/{site-id}/items/{item-id}/versions`  |
| <span data-ttu-id="6d2a7-108">[Obtener versión][version-get]</span><span class="sxs-lookup"><span data-stu-id="6d2a7-108">[Get version][version-get]</span></span>         | `GET /sites/{site-id}/items/{item-id}/versions/{version-id}`     |
| <span data-ttu-id="6d2a7-109">[Restaurar versión][version-restore]</span><span class="sxs-lookup"><span data-stu-id="6d2a7-109">[Restore version][version-restore]</span></span> | `POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/listitem_list_versions.md
[version-get]: ../api/listitemversion_get.md
[version-restore]: ../api/listitemversion_restore.md


## <a name="json-representation"></a><span data-ttu-id="6d2a7-110">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6d2a7-110">JSON representation</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItemVersion",
  "@odata.type": "microsoft.graph.listItemVersion",
  "@type.aka": "oneDrive.baseItemVersion"
}-->

```json
{
  "fields": { "@odata.type": "microsoft.graph.fieldValueSet" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "published": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a><span data-ttu-id="6d2a7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6d2a7-111">Properties</span></span>

|      <span data-ttu-id="6d2a7-112">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d2a7-112">Property name</span></span>       |                         <span data-ttu-id="6d2a7-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d2a7-113">Type</span></span>                         |                               <span data-ttu-id="6d2a7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d2a7-114">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="6d2a7-115">**id**</span><span class="sxs-lookup"><span data-stu-id="6d2a7-115">**id**</span></span>                   | <span data-ttu-id="6d2a7-116">cadena</span><span class="sxs-lookup"><span data-stu-id="6d2a7-116">string</span></span>                                               | <span data-ttu-id="6d2a7-117">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-117">The ID of the version.</span></span> <span data-ttu-id="6d2a7-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-118">Read-only.</span></span>                                       |
| <span data-ttu-id="6d2a7-119">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="6d2a7-119">**lastModifiedBy**</span></span>       | [<span data-ttu-id="6d2a7-120">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="6d2a7-120">IdentitySet</span></span>](../resources/identitySet.md)           | <span data-ttu-id="6d2a7-121">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-121">Identity of the user which last modified the version.</span></span> <span data-ttu-id="6d2a7-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-122">Read-only.</span></span>        |
| <span data-ttu-id="6d2a7-123">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="6d2a7-123">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="6d2a7-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6d2a7-124">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="6d2a7-125">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-125">Date and time the version was last modified.</span></span> <span data-ttu-id="6d2a7-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-126">Read-only.</span></span>                 |
| <span data-ttu-id="6d2a7-127">**published**</span><span class="sxs-lookup"><span data-stu-id="6d2a7-127">**published**</span></span>            | [<span data-ttu-id="6d2a7-128">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="6d2a7-128">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="6d2a7-129">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-129">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="6d2a7-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-130">Read-only.</span></span> |


## <a name="relationships"></a><span data-ttu-id="6d2a7-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6d2a7-131">Relationships</span></span>

<span data-ttu-id="6d2a7-132">En la tabla siguiente, se definen las relaciones que tiene el recurso **driveItemVersion** con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-132">The following table defines the relationships that the **driveItemVersion** resource has to other resources.</span></span>

| <span data-ttu-id="6d2a7-133">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="6d2a7-133">Relationship name</span></span> |                      <span data-ttu-id="6d2a7-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d2a7-134">Type</span></span>                      |                               <span data-ttu-id="6d2a7-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d2a7-135">Description</span></span>                                |
| :---------------- | :--------------------------------------------- | :----------------------------------------------------------------------- |
| <span data-ttu-id="6d2a7-136">**fields**</span><span class="sxs-lookup"><span data-stu-id="6d2a7-136">**fields**</span></span>        | [<span data-ttu-id="6d2a7-137">FieldValueSet</span><span class="sxs-lookup"><span data-stu-id="6d2a7-137">FieldValueSet</span></span>](../resources/fieldvalueset.md) | <span data-ttu-id="6d2a7-138">Una colección de los campos y valores para esta versión del elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="6d2a7-138">A collection of the fields and values for this version of the list item.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
