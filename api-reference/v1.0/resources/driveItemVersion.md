# <a name="driveitemversion-resource-type"></a><span data-ttu-id="48934-101">Tipo de recurso DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="48934-101">DriveItemVersion resource type</span></span>

<span data-ttu-id="48934-102">El recurso **DriveItemVersion** representa una versión específica de un objeto [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="48934-102">The **DriveItemVersion** resource represents a specific version of a [DriveItem](driveitem.md).</span></span>


## <a name="tasks-on-driveitemversion-resources"></a><span data-ttu-id="48934-103">Tareas en recursos DriveItemVersion</span><span class="sxs-lookup"><span data-stu-id="48934-103">Tasks on DriveItemVersion resources</span></span>

<span data-ttu-id="48934-104">Las tareas siguientes están disponibles para los recursos driveItemVersion.</span><span class="sxs-lookup"><span data-stu-id="48934-104">The following tasks are available for driveItemVersion resources.</span></span>

|            <span data-ttu-id="48934-105">Tarea común</span><span class="sxs-lookup"><span data-stu-id="48934-105">Common task</span></span>             |         <span data-ttu-id="48934-106">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="48934-106">HTTP method</span></span>         |
| :--------------------------------- | :-------------------------- |
| <span data-ttu-id="48934-107">[Enumerar versiones][version-list]</span><span class="sxs-lookup"><span data-stu-id="48934-107">[List versions][version-list]</span></span>      | `GET /drive/items/{item-id}/versions`  |
| <span data-ttu-id="48934-108">[Obtener versión][version-get]</span><span class="sxs-lookup"><span data-stu-id="48934-108">[Get version][version-get]</span></span>         | `GET /drive/items/{item-id}/versions/{version-id}`     |
| <span data-ttu-id="48934-109">[Obtener contenido][content-get]</span><span class="sxs-lookup"><span data-stu-id="48934-109">[Get contents][content-get]</span></span>        | `GET /drive/items/{item-id}/versions/{version-id}/content` |
| <span data-ttu-id="48934-110">[Restaurar versión][version-restore]</span><span class="sxs-lookup"><span data-stu-id="48934-110">[Restore version][version-restore]</span></span> | `POST /drive/items/{item-id}/versions/{version-id}/restore` |

[version-list]: ../api/driveitem_list_versions.md
[version-get]: ../api/driveitemversion_get.md
[content-get]: ../api/driveitemversion_get_contents.md
[version-restore]: ../api/driveitemversion_restore.md

<span data-ttu-id="48934-111">En la tabla anterior, los ejemplos usan `/drive`, pero hay varias solicitudes válidas.</span><span class="sxs-lookup"><span data-stu-id="48934-111">In the previous table, the examples use `/drive`, but there are many valid requests.</span></span>

## <a name="json-representation"></a><span data-ttu-id="48934-112">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="48934-112">JSON representation</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItemVersion",
  "@odata.type": "microsoft.graph.driveItemVersion",
  "@type.aka": "oneDrive.driveItemVersion"
}-->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" },
  "size": 12356
}
```

## <a name="properties"></a><span data-ttu-id="48934-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48934-113">Properties</span></span>

|      <span data-ttu-id="48934-114">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="48934-114">Property name</span></span>       |                         <span data-ttu-id="48934-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="48934-115">Type</span></span>                         |                               <span data-ttu-id="48934-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="48934-116">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="48934-117">**id**</span><span class="sxs-lookup"><span data-stu-id="48934-117">**id**</span></span>                   | <span data-ttu-id="48934-118">cadena</span><span class="sxs-lookup"><span data-stu-id="48934-118">string</span></span>                                               | <span data-ttu-id="48934-119">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="48934-119">The ID of the version.</span></span> <span data-ttu-id="48934-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="48934-120">Read-only.</span></span>                                       |
| <span data-ttu-id="48934-121">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="48934-121">**lastModifiedBy**</span></span>       | [<span data-ttu-id="48934-122">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="48934-122">IdentitySet</span></span>](../resources/identitySet.md)           | <span data-ttu-id="48934-123">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="48934-123">Identity of the user which last modified the version.</span></span> <span data-ttu-id="48934-124">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="48934-124">Read-only.</span></span>        |
| <span data-ttu-id="48934-125">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="48934-125">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="48934-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="48934-126">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="48934-127">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="48934-127">Date and time the version was last modified.</span></span> <span data-ttu-id="48934-128">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="48934-128">Read-only.</span></span>                 |
| <span data-ttu-id="48934-129">**publication**</span><span class="sxs-lookup"><span data-stu-id="48934-129">**publication**</span></span>          | [<span data-ttu-id="48934-130">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="48934-130">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="48934-131">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="48934-131">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="48934-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="48934-132">Read-only.</span></span> |
| <span data-ttu-id="48934-133">**size**</span><span class="sxs-lookup"><span data-stu-id="48934-133">**size**</span></span>                 | <span data-ttu-id="48934-134">Int64</span><span class="sxs-lookup"><span data-stu-id="48934-134">Int64</span></span>                                                | <span data-ttu-id="48934-135">Indica el tamaño de la secuencia de contenido para esta versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="48934-135">Indicates the size of the content stream for this version of the item.</span></span>  |
| <span data-ttu-id="48934-136">**content**</span><span class="sxs-lookup"><span data-stu-id="48934-136">**content**</span></span>              | <span data-ttu-id="48934-137">Secuencia</span><span class="sxs-lookup"><span data-stu-id="48934-137">Stream</span></span>                                               | <span data-ttu-id="48934-138">La secuencia de contenido para esta versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="48934-138">Indicates the size of the content stream for this version of the item.</span></span>                        |

<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
